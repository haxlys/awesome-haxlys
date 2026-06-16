# update-starred-repos

Update the awesome-haxlys README with latest GitHub starred repos and current star counts.

## When to use

- User says "update stars", "sync starred repos", "README 업데이트", "스타 레포 최신화"
- User asks to check for new starred repos
- README header has stale `마지막 업데이트` date

## Workflow

### 1. Fetch all starred repos via GraphQL

```bash
gh api graphql -f query='
query {
  viewer {
    starredRepositories(first: 100, orderBy: {field: STARRED_AT, direction: DESC}) {
      pageInfo { hasNextPage endCursor }
      totalCount
      edges {
        starredAt
        node {
          nameWithOwner
          stargazerCount
          primaryLanguage { name }
          description
        }
      }
    }
  }
}' --jq '
  "total: \(.data.viewer.starredRepositories.totalCount)",
  (.data.viewer.starredRepositories.edges[] |
    "\(.starredAt[0:10]) | \(.node.stargazerCount)⭐ | \(.node.primaryLanguage.name // "-") | \(.node.nameWithOwner)")
'
```

> ⚠️ Use **GraphQL** (`starredAt`). REST `/user/starred` returns `starred_at: null` unless token has `user:star` scope.

If total > 100, paginate with `after` cursor from `pageInfo.endCursor`.

### 2. Find new repos since last update

Check `마지막 업데이트: YYYY-MM-DD` in README header. Filter repos where `starredAt > YYYY-MM-DD` and not already in README.

### 3. Categorize new repos

16 categories with sub-categories (see README `## 빠른 탐색`). Match each repo's description/name to the closest category.

### 4. Update star counts for existing repos

```bash
grep -o 'github\.com/[^)]*' README.md | sed 's|github\.com/||' | sort -u > /tmp/repo_names.txt
awk -F/ '{print "https://api.github.com/repos/"$1"/"$2}' /tmp/repo_names.txt \
  | xargs -P 8 -I{} sh -c 'curl -s -H "Authorization: token $(gh auth token)" "{}" | jq -r "[.full_name, (.stargazers_count|tostring)] | join(\"|\")"' > /tmp/star_counts.txt
```

Then regex-replace `(⭐ [0-9,]+)` with current values.

### 5. Edit README

Entry format (preserve exactly):
```
- YYYY-MM-DD - [owner/repo](https://github.com/owner/repo) (⭐ 123,456) - Language - Korean description
```

Update these:
- **Header**: `마지막 업데이트: YYYY-MM-DD`, total repo count
- **Quick nav**: category counts + anchor links (GitHub generates anchors from header text, e.g. `### Foo (N)` → `#foo-n`)
- **Section headers**: `### Category (N)`
- **Existing entries**: star counts  
- **New entries**: inserted at section start (date descending)
- **README 상단 기준문구**: `2025년 이후 별표 목록은 {N}개이고`

### 6. Verify

```bash
# Total entry count
grep -c 'github\.com/' README.md
# No duplicates
grep -o 'github\.com/[^)]*' README.md | sort | uniq -d
# Section counts match
grep '^### ' README.md
```

## Notes

- `gh auth status` required before running API calls
- All descriptions in Korean
- Star count format: comma-separated thousands (e.g. 123,456)
- Language field omitted when null or "Unknown"
- `.opencode/skills/update-starred-repos/` has the OpenCode-specific variant of this same skill
