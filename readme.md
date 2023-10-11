The partial within this minimal example splits a slice of pages into a slice of pairs of pages.

This works with Hugo v0.113.0 and earlier but fails with Hugo v0.114.0 up to (at least) v0.119.0
with the following error:

```
execute of template failed: template: _default/list.html:10:16
  executing "main" at <partial "group_in_pairs" $allPages>:
  error calling partial: "/home/me/hugo_issue_slices/layouts/partials/group_in_pairs.html:13:27": 
    execute of template failed: template: partials/group_in_pairs.html:13:27: 
    executing "partials/group_in_pairs.html" at <append (slice $currGroup)>: 
      error calling append: 
      cannot append slice of page.Pages to slice of page.Page
```
