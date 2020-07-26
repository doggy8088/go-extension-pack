# Go Extension Pack

This extension pack include some of the popular (and some of my favorite) Go extensions. If you like it, please leave your `Rating & Review` and share with your friends. If you know any extension that is good for Go development, just let me know by [creating an issue](https://github.com/doggy8088/go-extension-pack/issues).

## Extensions Included

* [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go)
  * This extension provides rich language support for the [Go programming language](https://golang.org/) in VS Code.
  * Go Snippets
    * code skeleton
      * `pkgm`: package main and main function
      * `helloweb`: sample hello world webapp
    * code patterns
      * `sort`: custom `sort.Sort` interface implementation
    * function/method
      * `func`: `function` declaration
        * `fmain`: main function
        * `finit`: init function
        * `go`: anonymous `goroutine` declaration
        * ~~`ef`: Example function~~
      * `meth`: `method` declaration
    * imports
      * `im`: `import` statement
      * `ims`: `import` block
    * declarations
      * `var`: `variable` declaration
      * `co`: `constant` declaration
      * `cos`: `constant` block declaration
      * `in`: empty `interface`
      * `tyi`: type `interface` declaration
      * `tys`: type `struct` declaration
      * `map`: `map` declaration
      * `gf`: `goroutine` declaration
    * statements
      * `if`: if statement
      * `el`: else statement
      * `ie`: if-else statement
      * `iferr`: if err != nil
      * `switch`: switch statement
        * `cs`: case clause
      * `for`: for statement
      * `forr`: for range statement
      * `sel`: select statement
      * `make`: make statement
      * `new`: new statement
      * `df`: defer statement
      * `ch`: channel
      * `pn`: panic
    * fmt
      * `fp`: fmt.Println()
      * `ff`: fmt.Printf()
    * log
      * `lp`: log.Println()
      * `lf`: log.Printf()
      * `lv`: log.Printf() with variable content
    * net/http
      * `hf`: http.HandleFunc()
        * `hand`: http handler declaration
        * `wr`: http Response
        * `rd`: http.Redirect()
        * `herr`: http.Error()
      * `las`: http.ListenAndServe()
      * `sv`: http.Serve()
    * testing
      * function template
        * `tf`: Test function
        * `bf`: Benchmark function
        * `tdt`: table driven test function
      * common api
        * `tl`: t.Log()
        * `tlf`: t.Logf()
        * `tlv`: t.Logf() with variable content

* [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
  * Run code: `Ctrl+Alt+N`
  * Stop run: `Ctrl+Alt+M`

* [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype)
  * `quicktype` infers types from sample JSON data, then outputs strongly typed models and serializers for working with that data in your desired programming language. For more explanation, read [A first look at quicktype](http://blog.quicktype.io/first-look/).
  * It supports `Go`, `C#`, `C++`, `Java`, `TypeScript`, `Swift`, `Elm`, and `JSON Schema`.  I have to say THIS IS AWESOME! Just try it.

* [Gremlins tracker for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=nhoizey.gremlins)
  * Reveals some characters that can be harmful because they are invisible or looking like legitimate ones. It could possibly cost you few hours to find out problems.

## Recommended Settings

### Keyboard shortcuts

* Editing
  * `Alt-o`: **Go: Show All Commands...**
* Testing
  * `Alt-j Alt-j`: **Go: Toggle Test File** (`go.toggle.test.file`)
  * `Alt-j Alt-c`: **Go: Toggle Test Coverage In Current Package** (`go.test.coverage`)
* Code Generation
  * `Alt-g Alt-g`: **Go: Generate Unit Tests For Function** (`go.test.generate.function`)
  * `Alt-g Alt-f`: **Go: Generate Unit Tests For File** (`go.test.generate.file`)
  * `Alt-g Alt-p`: **Go: Generate Unit Tests For Package** (`go.test.generate.package`)
  * `Alt-g Alt-i`: **Go: Generate Interface Stubs** (`go.test.generate.package`)

### Visual Studio Code

* Configure Tasks

    There are two common/built-in task called `Tasks: Run Build Task` (`Ctrl-Shift-B`) and `Tasks: Run Test Task` (`Ctrl-Shift-/`) in the VSCode. So I usually use these for common Build/Test tasks for Go projects.

    > By default, the `Tasks: Run Test Task` don't have a keyboard shortcut. You must binding this by yourself.

    Just add a `.vscode/tasks.json` file into your workspace with the following content.

    ```json
    {
        // See https://go.microsoft.com/fwlink/?LinkId=733558
        // for the documentation about the tasks.json format
        "version": "2.0.0",
        "tasks": [
            {
                "label": "build",
                "command": "go",
                "type": "shell",
                "args": [
                    "build",
                    "-o",
                    "dist/${workspaceFolderBasename}"
                ],
                "group": {
                    "kind": "build",
                    "isDefault": true
                },
                "presentation": {
                    "reveal": "silent"
                },
                "problemMatcher": "$msCompile"
            },
            {
                "label": "test",
                "command": "go",
                "type": "shell",
                "args": [
                    "test",
                ],
                "group": {
                    "kind": "test",
                    "isDefault": true
                },
                "presentation": {
                    "reveal": "silent"
                },
                "problemMatcher": "$msCompile"
            }
        ]
    }
    ```

    > More info: <https://go.microsoft.com/fwlink/?LinkId=733558>

## Snippets Included

This extension will contains supplementary code snippets to [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go) extension.  Stay tuned.

### Go snippets

* TODO

### Dockerfile snippets

* TODO
  * `docker-go`: Multi-stage Dockerfile for Go

**Enjoy!**
