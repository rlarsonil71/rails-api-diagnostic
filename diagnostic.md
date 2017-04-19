# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
A backend allows multiple users hitting the same web app to interact with each other.
A backend also allows for data persistence storing app data so that users of
the web app can access the app's data over time.  Without a backend, none of
this would be possible.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
Model layer
```

Which layer in the MVC pattern communicates with the model?

```md
Controller layer
```

Why don't we use views in our interpretation of the MVC pattern?

```md
Views are user specific are written in front end languages such as HTML, CSS, JQuery,
etc.
```

What does C.R.U.D stand for?

```md
Create
Read
Update
Destroy
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
Controller layer
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
Index -- READ
Show  -- READ
Create -- CREATE
Update -- UPDATE
Destroy -- DESTROY
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
- Client makes a GET request to a particular URL (`/people/1`) to the server.
- The server receives the incoming GET request from the front-end client and
executes specific behaviors in response to this request.
- The server triggers the appropriate `people` controller using routes to
retrieve the `id = 1` data record through some kind of data storage system.
- The specific `people` controller that is triggered by the server will use
the appropriate `people` model to access the requested data from the database
and that specific model will return the requested data from the database as well
as a success or failure response.
- The `people` controller will then construct a VIEW with the requested content
back to the original client.
```

What is the command to generate a new rails-api app?

```bash
rails new my_api --api
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
bin/rake db:drop
bin/rake db:create
bin/rake db:migrate
bin/rake db:seed
bin/rake db:examples
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate scaffold pet name:string age:integer
```
