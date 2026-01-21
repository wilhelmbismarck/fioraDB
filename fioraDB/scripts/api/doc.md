FioraDB API
===========

## GET

### ROOT

`/`

API root. Runtime information.

### GROUP

`/group/`

List of `Group.id`.

`/group/{id}/`

- `group/{id}/latest_topic/` + `amount` (max 20)

- `group/{id}/latest_post/` + `amount` (max 20)

### SECTIONS

`/section/`

List of `Sections.id`.

`/section/{id}/`

- `section/{id}/latest_topic/` + `amount`

- `section/{id}/latest_post/` + `amount`

### USER

`/user/{id}/`

- `/user/{id}/topics/` + `offset` + `limit` + (`group` | `section`) + `before` + `after`

  - `/user/{id}/topics/count/` + (`group` | `section`) + `before` + `after`

- `/user/{id}/posts/` + `offset` + `limit` + (`group` | `section`) + `before` + `after`

  - `/user/{id}/posts/count/` + (`group` | `section`) + `before` + `after`
 
    - `/user/{id}/posts/count/last_year/` + *same*
   
    - `/user/{id}/posts/count/last_month/` + *same*
 
- `user/{id}/posted/` + (`group` | `section`) + `before` + `after`
  User has posted on forum (if specified, group or section) (if specified, before or/and after a date)

- `user/{id}/first_post/` + (`group` | `section`)

- `user/{id}/lastest_post/` + (`group` | `section`) + `amount` (max 20)
 
### TOPIC

`topic/latest/` + `amount` (max 20)

`topic/{id}/`

- `topic/{id}/first_post/` same as `topic/{id}/root`

- `topic/{id}/posts/` + (`page` | (`offset` + `limit`))

### POST

`post/latest/` + `amount` (max 20)

`post/{id}/`
