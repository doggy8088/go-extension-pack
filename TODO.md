# TODO

1. Replace Go built-in snippets

    add more `fmt` snippets

    - `ffv`: print values (`%v`)
    - `ffp`: print values including struct's field names (`%+v`)
    - `ffh`: print Go syntax representation of the value (`%#v`)
    - `fft`: print the type of a value (`%T`)
    - `fft`: print the type of a value (`%T`)
    - `ffd`: print integers, base-10 formatting (`%d`)
    - `ffx`: print integers, base-16 (hex) formatting (`%x`)
    - `ffb`: print integers, base-2 (binary) formatting (`%b`)
    - `ffc`: print character corresponding to the given integer (`%c`)
    - `fff`: print floats, basic decimal formatting (`%f`)
    - `ffe`: print floats, in scientific notation. (`%e` / `%E`)
    - `ffs`: print string (`%s`)
    - `ffq`: print double-quote string (`%q`)
    - `ffpt`: print pointer (`%p`)
    - `fsf`: `fmt.Sprintf`
    - `fsfe`: `fmt.Fprintf(os.Stderr, "error: %s\n", "error")`

2. More custom snippets

    `channel` snippets

    `select` snippets

    `error` snippets

    `time` snippets

    `http` snippets

    `json` snippets

    `number` snippets

    `string` snippets

    `io` snippets

    `base64` snippets

    `sha1` snippets

    `url` snippets

3. Add [go-by-example](https://github.com/doggy8088/go-by-example) snippets

    `ge-*`

4. Add [pprof](https://golang.org/pkg/net/http/pprof/) helpers

5. Keep watching [x/tools/gopls: generate method stubs for a given interface #37537](https://github.com/golang/go/issues/37537) progress.

    <https://vimeo.com/394345925>

    Compare to GoLand:

    1. No Refactoring tool at this time.

        - ~~Extract function~~
        - ~~Extract variable~~
        - ~~Choose interface to implement~~
        - Create method
        - Generate constructor

    2. IntelliSense in a Template
    3. Add Format String in `fmt.Printf` usage
    4. Call snippet by a variable
    5. Surround with
