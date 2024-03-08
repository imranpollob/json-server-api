# JSON Sever API
This repo contains `db.json` and `db.example.json` files contains users, posts, comments, photos, albums and todos. The files are same. So, if you modified `db.json` then if you want to reset the API data to its original state you can copy the JSON from the `db.example.json` file into the `db.json` file.

Check the `db.sample.json` to get an overview of the data.

The API has the following endpoints:

- /users
- /users/:id
- /posts
- /posts/:id
- /posts?userId=:id
- /users/:id/posts
- /comments
- /comments/:id
- /comments?postId=:id
- /posts/:id/comments
- /todos
- /todos/:id
- /todos?userId=:id
- /users/:id/todos
- /albums
- /albums/:id
- /albums?userId=:id
- /users/:id/albums
- /photos
- /photos/:id
- /photos?albumId=:id
- /albums/:id/photos


More options https://www.npmjs.com/package/json-server/v/0.17.4
- Filter: /posts?title=json-server&author=typicode
- Pagination: /posts?_page=7&_limit=20
- Sort: /posts?_sort=views&_order=asc
- Slice: /posts?_start=20&_end=30
- Operators: /posts?views_gte=10&views_lte=20&id_ne=1&title_like=server
- Full-text search: /posts?q=internet
- Relationships:
  - To include children resources: /posts?_embed=comments
  - To include parent resource: /comments?_expand=post
  - To get or create nested resources: /posts/1/comments


JSON Server supports the following HTTP methods
```
GET    /posts
GET    /posts/:id
POST   /posts
PUT    /posts/:id
PATCH  /posts/:id
DELETE /posts/:id

# Same for other properties
```

## Run Command
Simply run 
```bash
npm run dev
```

The original command abstracted behind this command is
```bash
json-server --watch db.json --port 3001 --host 127.0.0.1
```