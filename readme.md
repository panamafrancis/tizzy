# Tizzy

An in-memory copy of time.LoadLocation(), nothing original simply a workaround
for when you find your code calling time.LoadLocation() at 1khz which will open
a zip file on disk to unmarshal files containing bindata into a time.Location
struct each time it's called.

The timezone Locations are loaded from $GOROOT/lib/time/zoneinfo.zip, the
default for unix and windows.

Any copyrights belong to the Go authors.


## Usage

```go
    import "github.com/panamafrancis/tizzy"

    ...

    loc, err := tizzy.LoadLocation("Europe/Berlin")
```
