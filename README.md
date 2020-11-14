# static

**Very simple** static website handler for Go.

## Example

```go
package main

import (
    "http"
    "log"
    "github.com/tidwall/static"
)

func main() {
    vars := map[string]string{
        "MySpecialVar": "rainbows wow!",
    }
    http.HandleFunc("/", static.HandleFunc("static_files", vars))
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```

