# GO INSTALL COMMAND N REFORMAT CODE

## Go Install Command

```
go install github.com/rakyll/hey@latest
```

example of download:

```
PS C:\Users\User\OneDrive\Desktop\BOOKS_STUDY\GOLANG_IDIOMATIC\chapter_1\001_hello_world> go install github.com/rakyll/hey@latest
go: downloading github.com/rakyll/hey v0.1.5
go: downloading golang.org/x/net v0.48.0
go: downloading golang.org/x/text v0.33.0
```

prooving hey command:

```
hey https://www.golang.org

Summary:
  Total:        2.2949 secs
  Slowest:      0.0000 secs
  Fastest:      0.0000 secs
  Average:       NaN secs
  Requests/sec: 87.1485
  
Response time histogram:

Latency distribution:

Details (average, fastest, slowest):
  DNS+dialup:    NaN secs, 0.0000 secs, 0.0000 secs
  DNS-lookup:    NaN secs, 0.0000 secs, 0.0000 secs
  req write:     NaN secs, 0.0000 secs, 0.0000 secs
  resp wait:     NaN secs, 0.0000 secs, 0.0000 secs
  resp read:     NaN secs, 0.0000 secs, 0.0000 secs

Status code distribution:

Error distribution:
  [200] Get "https://go.dev/": EOF
```

> [!IMPORTANT] Install the newest version
> - Just rerun the install command
> - go install github.com/rakyll/hey@latest

## Commands to Reformate Code

Reformats code to math with the standard format: 

```
go fmt <name of the archive>

go fmt ./...
```

This command orders aphabetically imports, removes unused imports, and attemps to guess any unspecified imports.

```
go install golang.org/x/tools/cmd/goimports@latest
```

```
goimports -l -w .
```

> [!DANGER] 
> Always run go fmt or goimports before compiling your code!