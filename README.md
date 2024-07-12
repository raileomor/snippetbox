# snippetbox

```bash
$ go run ./cmd/web
$ go run ./cmd/web >>/tmp/web.log

$ docker compose up -d
$ docker exec -it [container_name_or_id] mysql -u[username] -p

# You might want to consider using `mkcert` to generate the TLS certificates
# it has the advantage that the generated certificates are locally trusted
$ go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost
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

8. Stateful HTTP

- Choosing a session manager
- Setting up the session manager
- Working with session data

9. Server and security improvements

- The http.Server struct
- The server error log
- Generating a self-signed TLS certificate
- Running a HTTPS server
- Configuring HTTPS settings
- Connection timeouts

10. User authentication

- Routes setup
- Creating a users model
- User signup and password encryption
- User login
- User logout
- User authorization
- CSRF protection
