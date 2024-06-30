# snippetbox

```bash
$ go run ./cmd/web
$ go run ./cmd/web >>/tmp/web.log

$ docker compose up -d
$ docker exec -it [container_name_or_id] mysql -u[username] -p
```

Let's Go

2. Foundations I, II

- Project setup and creating a module
- Web application basics
- Routing requests
- Wildcard route patterns
- Method-based routing
- Customizing responses
- Project structure and organization
- HTML templating and inheritance
- Serving static files
- The http.Handler interface

3. Configuration and error handling

- Managing configuration settings
- Structured logging
- Dependency injection
- Centralized error handling
- Isolating the application routes

4. Database-driven responses

- Setting up MySQL
- Installing a database driver
- Modules and reproducible builds
- Creating a database connection pool
- Designing a database model
- Executing SQL statements
- Single-record SQL queries
- Multiple-record SQL queries
- Transactions and other details

5. Dynamic HTML templates

- Displaying dynamic data
- Template actions and functions
- Caching templates
- Catching runtime errors
- Common dynamic data
- Custom template functions

6. Middleware

- How middleware works
- Setting common headers
- Request logging
- Panic recovery
- Composable middleware chains

7. Processing forms

- Setting up an HTML form
- Parsing form data
- Validating form data
- Displaying errors and repopulating fields
- Creating validation helpers
- Automatic form parsing
