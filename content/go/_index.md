---
title: "Go Packages"
type: "go-import"
layout: "list"
---

This directory contains Go vanity import paths.

To add a new package, create a file like:

```yaml
---
title: "mypackage"
type: "go-import"
module: "mypackage"
repo: "https://github.com/sivchari/mypackage"
---
```

Then you can use `go get sivchari.io/mypackage`.
