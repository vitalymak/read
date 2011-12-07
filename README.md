For reading user input from stdin.

## USAGE

```javascript
var read = require("read")
read(options, callback)
```

The callback gets called with either the user input, or the default
specified, or an error, in the traditional `callback(error, result)`
node style.

## OPTIONS

Every option is optional.

* `prompt` What to write to stdout before reading input.
* `silent` Don't echo the output as the user types it.
* `num` Max number of chars to read from terminal.
* `delim` The char that means we're done.  Default: `"\n"`
* `timeout` Number of ms to wait for user input before giving up.

If silent is true, or num is set, or delim is something other than
`"\n"`, then read will set raw mode, and read character by character.

At this time, backspace and arrow keys are not supported in raw mode.
It's probably not too hard to add support for this, perhaps using node's
built-in readline module.

## CONTRIBUTING

Patches welcome.
