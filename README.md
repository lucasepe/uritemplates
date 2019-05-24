# uritemplates

Package uritemplates is a level 4 implementation of RFC 6570 (URI
Template, http://tools.ietf.org/html/rfc6570).

To use uritemplates, parse a template string and expand it with a value
map:

```go
import (
  // ...
  // ...
  "github.com/lucasepe/uritemplates"
)

// ...

template, _ := uritemplates.Parse("https://api.github.com/repos{/user,repo}")
values := make(map[string]interface{})
values["user"] = "lucasepe"
values["repo"] = "uritemplates"
expanded, _ := template.Expand(values)
fmt.Printf(expanded)
```
