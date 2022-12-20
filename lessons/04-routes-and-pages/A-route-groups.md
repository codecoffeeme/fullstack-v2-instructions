The routes for app will be as follows

`/register`
`/signin`
`/home`
`/project/[id]`

The home and project route share the same layout, both being part of the dashboard. Signin and register share the same layout with each other as well. Because all 4 routes are on the same parent segment `/`, they all would share the same layout.

<br>

We don't want this. So we'll use route grouping here. This will allow us to have two root layouts without adding segments to the url.

```bash
(auth)
  layout
  register
    page
  signin
    page
(dashboard)
  layout
  home
    page
  project
    [id]
      page
```