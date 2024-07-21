# snippetbox

```bash
$ go run ./cmd/web
$ go run ./cmd/web >>/tmp/web.log

$ docker compose up -d
$ docker exec -it [container_name_or_id] mysql -u[username] -p

# You might want to consider using `mkcert` to generate the TLS certificates
# it has the advantage that the generated certificates are locally trusted
$ go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost

# Testing embedding
$ go build -o /tmp/web ./cmd/web/
$ cp -r ./tls /tmp/
$ cd /tmp/
$ ./web

# Testing
$ go test -v ./cmd/web
$ go test ./...
$ go test -v -run="^TestPing$" ./cmd/web/
$ go test -v -run="^TestHumanDate$/^UTC$" ./cmd/web
$ go test -v -skip="^TestHumanDate$" ./cmd/web/
$ go test -count=1 ./cmd/web # ignore caching
$ go clean -testcache
$ go test -failfast ./cmd/web # stop on first failure (others packages will continue)
$ go test -parallel=4 ./... # by callying t.Parallel() in the test
$ go test -race ./cmd/web/ # detect race conditions

# Integration Testing (if you have mysql with docker replace localhost with '%')
$ docker exec -it [container_name_or_id] mysql -u root -p
mysql> CREATE DATABASE test_snippetbox CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
mysql> CREATE USER 'test_web'@'localhost';
mysql> GRANT CREATE, DROP, ALTER, INDEX, SELECT, INSERT, UPDATE, DELETE ON test_snippetbox.* TO 'test_web'@'localhost';
mysql> ALTER USER 'test_web'@'localhost' IDENTIFIED BY 'pass';
$ go test -v -short ./... # for skipping long-running tests

$ go test -cover ./...
$ go test -coverprofile=/tmp/profile.out ./...
$ go tool cover -func=/tmp/profile.out # view the coverage profile
$ go tool cover -html=/tmp/profile.out # view the coverage profile in a browser

# To count the number of times each statement is executed use -covermode=count
# or -covermode=atomic if you run test in parallel
$ go test -covermode=count -coverprofile=/tmp/profile.out ./...
$ go tool cover -func=/tmp/profile.out
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

11. Using request context

- How request context works
- Request context for authentication/authorization

12. File embedding

- Embedding static files
- Embedding HTML templates

13. Testing

- Unit testing and sub-tests
- Testing HTTP handlers and middleware
- End-to-end testing
- Customizing how tests run
- Mocking dependencies
- Testing HTML forms
- Integration testing
- Profiling test coverage

16. Guided exercises

- Add an 'About' page to the application
