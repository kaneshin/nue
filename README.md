# Nue
Fast router.

## usage

```go
package main

import (
	"net/http"
	
	"github.com/gotokatsuya/nue"
)

func main() {
	handler := nue.New()
	handler.Add("/user", "/hello", func(r http.ResponseWriter, r *http.Request) {
		r.Write([]byte("hello world"))
	})
	http.ListenAndServe(":8080", handler)
}
```
