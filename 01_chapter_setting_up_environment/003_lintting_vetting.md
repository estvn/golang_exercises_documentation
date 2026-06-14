# LINTING AND VETTING

## Linting

- `go fmt` is the first step to make and idiomatic code in golang
- lintting was created to ensure your code follows the correct style guidelines.

- golint isnt's perfectly accurate, the most part are recommendations to follow correct standards.
- youren't obligated to make the corrections that golint suggests.

Install golint:

```
go install golang.org/x/lint/golint@latest
```

Run it in the entire project:

```
golint ./...
```

## Vetting

- There is other command to detects other kind of errors, like pass arguments to a functions that's never used

vetting:

```
go vet ./...
```

## Run both in a single command

- Run a lot of tools slows down the building 
- to run these two commands use this tool: golangci-lint

```
go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest
```

```
golangci-lint run
```

> [!DANGER] Problems with golangci-lint
- This tools runs a lot of lints, by default 10, an can enable another 50
- This can make suggests thats againts the way the team is working
- You can enable or disable lints in this tool

> [IMPORTANT] Suggestions
- Use golint in the code review process
- Use go vet in the automated compiling process
- Use golint and go vet to avoid common errors
- If use golangci-lint, make sure to use the appropiate tool for your team

