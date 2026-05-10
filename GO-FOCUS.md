# My Go Learning Path: From Zero to Production

> **Current Status**: Just completed Hello World!
> **Background**: Experienced in Python, C#, and TypeScript.
> **Goal**: Master Go for backend development, system-level scripting, and CLI tooling.

---

## Phase 1: Language Basics & Idioms

### 1.1 Core Syntax & Data Types

- [ ] Variables, Constants, and Zero Values
- [ ] Basic types: `int`, `float64`, `string`, `bool`, `byte`, `rune`
- [ ] Type inference with `:=`
- [ ] Type conversions (explicit vs implicit)
- [ ] Strings, Runes, and UTF-8 handling
- [ ] Arrays, Slices, and Maps
- [ ] Pointers (compared to C# and C)

### 1.2 Control Flow

- [ ] `if`, `else if`, `else` (no parentheses!)
- [ ] `for` loop (the only loop in Go)
- [ ] `range` for iterating over slices, maps, strings
- [ ] `switch` (no fallthrough by default)
- [ ] `defer`, `panic`, `recover`

### 1.3 Functions

- [ ] Multiple return values
- [ ] Named return values
- [ ] Variadic functions
- [ ] First-class functions and closures
- [ ] Recursion

### 1.4 Structs and Methods

- [ ] Defining structs (compared to C# classes/TS objects)
- [ ] Struct tags
- [ ] Methods and receivers (value vs pointer)
- [ ] Embedded structs (inheritance-like behavior)
- [ ] Interface basics

### 1.5 Interfaces & Polymorphism

- [ ] Implicit interface satisfaction (duck typing)
- [ ] Empty interface (`interface{}` or `any`)
- [ ] Interface composition
- [ ] Type assertions and type switches

### 1.6 Error Handling

- [ ] `error` interface and custom errors
- [ ] `fmt.Errorf` and error wrapping
- [ ] `errors.Is` and `errors.As`
- [ ] Panic vs Error handling philosophy

---

## Phase 2: Intermediate Language Features

### 2.1 Concurrency (Go's Superpower!)

- [ ] Goroutines (`go` keyword)
- [ ] Channels (`chan`) for communication
- [ ] Buffered vs Unbuffered channels
- [ ] `select` statement for channel multiplexing
- [ ] `sync` package: `WaitGroup`, `Mutex`, `RWMutex`
- [ ] `context` package for cancellation
- [ ] Worker pools and pipelines
- [ ] Race conditions and `-race` flag
- [ ] `atomic` operations

### 2.2 Advanced Data Structures

- [ ] Custom slices with methods
- [ ] Maps with struct keys
- [ ] Linked lists, stacks, queues (if needed)
- [ ] Generics (Go 1.18+) for reusable data structures

### 2.3 Reflection (Use Sparingly)

- [ ] `reflect` package basics
- [ ] JSON Marshaling/Unmarshaling with tags
- [ ] `interface{}` to struct conversion

---

## Phase 3: Standard Library Mastery

### 3.1 Input/Output

- [ ] `fmt` package (formatting, scanning)
- [ ] `io` and `io/ioutil`
- [ ] `bufio` for buffered I/O
- [ ] `os` package for file operations
- [ ] `path` and `path/filepath`

### 3.2 Text Processing

- [ ] `strings` and `bytes`
- [ ] Regular expressions (`regexp`)
- [ ] `unicode` and `unicode/utf8`
- [ ] `strconv` for string conversions
- [ ] `html` and `html/template`
- [ ] `text/template`

### 3.3 Time & Date

- [ ] `time` package (parsing, formatting, durations)
- [ ] `time.Ticker` and `time.Timer`

### 3.4 Math & Crypto

- [ ] `math`, `math/rand`, `math/big`
- [ ] `crypto`, `crypto/md5`, `crypto/sha256`
- [ ] `encoding/base64`, `encoding/json`, `encoding/xml`

### 3.5 Network Programming

- [ ] `net` package (TCP/UDP sockets)
- [ ] `net/http` (building APIs - precursor to web frameworks)
- [ ] `net/url` for URL parsing
- [ ] TLS/HTTPS configuration

### 3.6 Data Storage

- [ ] `database/sql` (SQL database access)
- [ ] `encoding/csv`, `encoding/json`
- [ ] `archive/zip`, `archive/tar`
- [ ] `compress/gzip`

---

## Phase 4: Testing, Debugging & Quality

### 4.1 Unit Testing

- [ ] `testing` package basics
- [ ] `TestXxx` convention
- [ ] `TestMain` for setup/teardown
- [ ] Table-driven tests (Go's idiomatic style!)
- [ ] Subtests with `t.Run`
- [ ] `testing` helpers: `t.Errorf`, `t.Fatalf`, `t.Skip`
- [ ] Generating test coverage (`go test -cover`)

### 4.2 Benchmarking

- [ ] Writing benchmark functions (`BenchmarkXxx`)
- [ ] `testing.B` and `b.N`
- [ ] Comparing benchmarks (`benchstat`)
- [ ] Memory allocation analysis

### 4.3 Mocking & Test Doubles

- [ ] Hand-written mocks (interfaces)
- [ ] `testify` package (`assert`, `require`, `mock`)
- [ ] `gomock` for automatic mock generation

### 4.4 Debugging

- [ ] `fmt.Println` debugging (it's okay sometimes!)
- [ ] `log` package for structured logging
- [ ] Delve debugger (`dlv`)
- [ ] `runtime` package for profiling
- [ ] `pprof` for CPU and memory profiling
- [ ] Race detector (`go test -race`)
- [ ] `trace` for concurrency debugging

### 4.5 Code Quality

- [ ] `gofmt` and `goimports`
- [ ] `golint` and `revive`
- [ ] `staticcheck` for static analysis
- [ ] `golangci-lint` for comprehensive linting
- [ ] Pre-commit hooks

---

## Phase 5: Common Patterns & Idioms

### 5.1 Design Patterns in Go

- [ ] Factory pattern (functions returning interfaces)
- [ ] Singleton pattern (using `sync.Once`)
- [ ] Builder pattern (fluent API with methods)
- [ ] Strategy pattern (interfaces)
- [ ] Observer pattern (channels!)
- [ ] Decorator pattern (function wrapping)

### 5.2 Go Idioms

- [ ] "Accept interfaces, return structs"
- [ ] "Don't over-engineer"
- [ ] Composition over inheritance
- [ ] Small interfaces (often 1 method)
- [ ] Error handling is explicit
- [ ] `fmt.Sprintf` for string building (or `strings.Builder`)

### 5.3 Clean Architecture

- [ ] Separation of concerns
- [ ] Dependency injection (manual or with libraries like `wire`)
- [ ] Layered architecture (handlers -> services -> repositories)
- [ ] Configuration management (environment variables, flags)

---

## Phase 6: Web Development with Fiber

### 6.1 Fiber Basics

- [ ] Installation and setup
- [ ] Routing (static, dynamic, groups)
- [ ] Middleware (custom and built-in)
- [ ] Request/Response handling
- [ ] JSON parsing and validation
- [ ] Error handling in Fiber

### 6.2 Advanced Fiber

- [ ] Websockets with Fiber
- [ ] Static file serving
- [ ] Template rendering
- [ ] Rate limiting
- [ ] CORS handling
- [ ] Authentication & Authorization (JWT, Sessions)

### 6.3 Building APIs

- [ ] RESTful API design
- [ ] Request validation (`go-playground/validator`)
- [ ] OpenAPI/Swagger documentation (`swaggo`)
- [ ] API versioning strategies
- [ ] Pagination and filtering

---

## Phase 7: CLI Development

### 7.1 Building CLIs

- [ ] `flag` package (built-in)
- [ ] `cobra` framework (industry standard)
- [ ] `viper` for configuration management
- [ ] `urfave/cli` (alternative to cobra)
- [ ] Terminal UI with `bubbletea` (TUI)
- [ ] Progress bars and spinners

### 7.2 Advanced CLI Features

- [ ] Subcommands and command groups
- [ ] Interactive prompts (`promptui`, `survey`)
- [ ] Shell completion generation
- [ ] Help text and documentation generation
- [ ] Building cross-platform binaries

---

## Phase 8: Production & Deployment

### 8.1 Build & Release

- [ ] `go build`, `go install`, `go run`
- [ ] Cross-compilation (`GOOS`, `GOARCH`)
- [ ] Build tags and constraints
- [ ] `goreleaser` for automated releases
- [ ] Dockerization (multi-stage builds)

### 8.2 Performance

- [ ] Profiling with `pprof`
- [ ] Memory optimization
- [ ] Goroutine leak detection
- [ ] GC tuning (rarely needed, but good to know)

### 8.3 Observability

- [ ] Structured logging (`log/slog`, `zap`, `zerolog`)
- [ ] Metrics with `prometheus/client_golang`
- [ ] Tracing with OpenTelemetry
- [ ] Health checks and readiness probes

---

## Resources & Tools

### Recommended Learning Resources

- **Books**:
  - "The Go Programming Language" (Kernighan & Donovan) - The Bible
  - "Let's Go" and "Let's Go Further" (Alex Edwards) - Web dev focus
  - "100 Go Mistakes and How to Avoid Them" (Teiva Harsanyi)
- **Websites**:
  - [Go by Example](https://gobyexample.com/) (Excellent for quick reference!)
  - [Go Tour](https://go.dev/tour/)
  - [Effective Go](https://go.dev/doc/effective_go.html)
  - [Go 101](https://go101.org/)
- **Communities**:
  - r/golang
  - Gophers Slack
  - Go Discord servers

### Development Tools

- **IDE**: VS Code with Go extension, GoLand (JetBrains), Vim with vim-go
- **Formatting**: `gofmt`, `goimports`
- **Linting**: `golangci-lint`
- **Debugging**: Delve (`dlv`)
- **Testing**: Built-in `go test`
- **Documentation**: `godoc`, `pkgsite`

### My Environment

- **Go Version**: 1.24.4 (specified in go.mod)
- **CI/CD**: GitHub Actions (`.github/workflows/go.yml`)
- **Project Structure**: Learning-focused, single module

---

## Learning Strategy

1. **Start Small**: Each concept above gets its own small, focused program.
2. **Write Tests for Everything**: Use `*_test.go` files aggressively to practice testing early.
3. **Read Standard Library Code**: The best way to learn idiomatic Go is to read the source code of the standard library.
4. **Build Projects**:
   - **CLI Tool**: A file organizer, a GitHub stats fetcher, or a local task manager.
   - **API**: A simple REST API for a todo list or a URL shortener.
   - **Web Scraper**: Concurrently fetch and parse web pages.
5. **Contribute to Open Source**: Find beginner-friendly Go projects on GitHub.

---

## Day-to-Day Focus Tracker

| Date | Phase | Topic | Status | Notes |
|------|-------|----------|--------|-------|-------|
|      | 1     | Hello World, Variables   | [x]    |       |
|      | 1     | Functions & Control Flow | [ ]    |       |
|      | 1     | Structs & Interfaces    | [ ]    |       |
|      | 1     | Error Handling & Maps   | [ ]    |       |
|      | 2     | Goroutines & Channels  | [ ]    |       |
|      | 2     | `sync` & `context`    | [ ]    |       |
|      | 3     | Standard Library     | [ ]    |       |
|      | 4     | Unit Tests & Benchmarks| [ ]    |       |
|      | 5     | Patterns & Idioms     | [ ]    |       |
|      | 6     | Fiber Web Framework  | [ ]    |       |
|      | 7     | CLI with Cobra       | [ ]    |       |
|      | 8     | Production Readiness| [ ]    |       |

---

## Next Immediate Steps

1. **Create a new folder** for `phase-01-language-basics`.
2. **Write a program** that declares variables of different types and prints them.
3. **Write a function** that takes a slice of ints and returns the sum and average.
4. **Create a struct** `Person` with `Name` and `Age`, and write methods to greet and have a birthday.
5. **Run tests** with `go test` and check coverage.

---

> **Pro Tip from a Python/C#/TS Developer**:
> - Forget classes and OOP inheritance. Go uses **composition** with structs and interfaces.
> - Explicit is better than implicit. Go's error handling is verbose but clear.
> - Concurrency is not parallelism, but it's your best friend for I/O-bound tasks.
> - Keep it simple. If you find yourself fighting the language, you're probably over-engineering.
