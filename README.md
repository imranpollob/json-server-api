# JSON Sever API
This repo contains `db.json` and `db.example.json` files contains users, posts, comments, photos, albums and todos. The files are same. So, if you modified `db.json` then if you want to reset the API data to its original state you can copy the JSON from the `db.example.json` file into the `db.json` file.

Check the `db.sample.json` to get an overview of the data.

The API has the following endpoints:

- /users
- /users/:id
- /posts
- /posts/:id
- /posts?userId=:id
- /comments
- /comments/:id
- /comments?postId=:id
- /todos
- /todos/:id
- /todos?userId=:id
- /albums
- /albums/:id
- /albums?userId=:id
- /photos
- /photos/:id
- /photos?albumId=:id

JSON Server supports the following routes
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