# rfsnotify v0.1.0
recursive directory notifications built as a wrapper around fsnotify (golang)

[![GoDoc](https://godoc.org/github.com/dietsche/rfsnotify?status.svg)](https://godoc.org/github.com/dietsche/rfsnotify)

This is a thin wrapper around https://github.com/go-fsnotify/fsnotify instead of only monitoring a top level folder,
it allows you to monitor all folders underneath the folder you specify.

Example:
--------
(error handling omitted to improve readability)
```
import "github.com/dietsche/rfsnotify"
watcher, err := rfsnotify.NewWatcher()

 //rfsnotify works exactly like fsnotify and implements the same API.
 //Rfsnotify implements two new API entry points: 
watcher.AddRecursive("/tmp/")
watcher.RemoveRecursive("/tmp/")

 //from this point forward, refer to the fsnotify documentation
 
```
