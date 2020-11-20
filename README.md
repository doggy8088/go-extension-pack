# Go Extension Pack

This extension pack include some of the popular (and some of my favorite) Go extensions. If you like it, please leave your `Rating & Review` and share with your friends. If you know any extension that is good for Go development, just let me know by [creating an issue](https://github.com/doggy8088/go-extension-pack/issues).

## Extensions Included

* [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go)
  * This extension provides rich language support for the [Go programming language](https://golang.org/) in VS Code.
  * Usage: There are tons of VSCode commands you can use including IntelliSense, Reactoring, Code Generation, Go to ..., Linting, ... etc.

      > Make sure you already imported packages before you are using these **Reactoring** features.

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
        * `tdt`: table driven test function
        * `tf`: Test function
        * `bf`: Benchmark function
        * `ef`: Example function
      * common api
        * `tl`: t.Log()
        * `tlf`: t.Logf()
        * `tlv`: t.Logf() with variable content

* [Go Doc](https://marketplace.visualstudio.com/items?itemName=msyrus.go-doc)
  * Show documentation of go symbols and packages.
  * Usage: Just move your cursor to any symbol such as `import`'s `"fmt"`, `fmt.Println(i)`'s `Println`, `json.Marshal(true)`'s `Marshal`. Then run `F1` > `Go Doc: Get Definition` command in VSCode. You will see the documentation of that symbol in the OUTPUT pane below.

* [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
  * Usage: Just hit the built-in hotkey to **Run** or **Stop** the code.
    * Run code: `Ctrl+Alt+N`
    * Stop run: `Ctrl+Alt+M`

* [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype)
  * `quicktype` infers types from sample JSON data, then outputs strongly typed models and serializers for working with that data in your desired programming language. For more explanation, read [A first look at quicktype](http://blog.quicktype.io/first-look/).
  * It supports `Go`, `C#`, `C++`, `Java`, `TypeScript`, `Swift`, `Elm`, and `JSON Schema`.  I have to say THIS IS AWESOME! Just try it.
  * Usage: Just copy JSON string to your clipboard, then run `F1` > `Paste JSON as Code` command in VSCode. Enter a top-level symbol name, then hit Enter to complete. It will generate all the JSON-mapped structs and tags.

* [Gremlins tracker for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=nhoizey.gremlins)
  * Reveals some characters that can be harmful because they are invisible or looking like legitimate ones. It could possibly cost you few hours to find out problems.

* [vscode-proto3](https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3)
  * Protobuf 3 support for Visual Studio Code

## Recommended Settings

### Keyboard shortcuts

* Editing
  * `Alt-o`: **Go: Show All Commands...** (`go.show.commands`)
  * `Alt-d`: **Go Doc: Get Definition** (`go-doc.get.def`)
* Testing
  * `Alt-j Alt-j`: **Go: Toggle Test File** (`go.toggle.test.file`)
  * `Alt-j Alt-c`: **Go: Toggle Test Coverage In Current Package** (`go.test.coverage`)
* Code Generation
  * `Alt-g Alt-g`: **Go: Generate Unit Tests For Function** (`go.test.generate.function`)
  * `Alt-g Alt-f`: **Go: Generate Unit Tests For File** (`go.test.generate.file`)
  * `Alt-g Alt-p`: **Go: Generate Unit Tests For Package** (`go.test.generate.package`)
  * `Alt-g Alt-i`: **Go: Generate Interface Stubs** (`go.test.generate.package`)
  * `Alt-g Alt-t`: **Go: Add Tags To Struct FIelds** (`go.add.tags`)
  * `Alt-g Alt-r`: **Go: Add Tags From Struct FIelds** (`go.remove.tags`)

### Visual Studio Code

* [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go)

    In order to use `Rename Symbol` ([gorename](https://pkg.go.dev/golang.org/x/tools/cmd/gorename?tab=doc)) feature, you have to enable `Go: Use Language Server` option. See [this](https://github.com/golang/vscode-go/issues/92#issuecomment-634373662) and [this](https://github.com/microsoft/vscode-go/issues/2074#issuecomment-507117831).

    > [gopls](https://github.com/golang/vscode-go/blob/master/docs/gopls.md) (pronounced: "go please") is the official [language server](https://langserver.org/) for the Go language. Check the [VSCode](https://github.com/golang/tools/blob/master/gopls/doc/vscode.md) page for further information. For complete gopls Settings, please [check here](https://github.com/golang/tools/blob/master/gopls/doc/settings.md).

    ```json
    {
      "go.useLanguageServer": true,
      "go.languageServerExperimentalFeatures": {
        "diagnostics": false,
        "documentLink": true,
      },
      "[go]": {
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true,
        },
      },
      "[go.mod]": {
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true,
        },
      }
    }
    ```

* [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)

    `code-runner.saveAllFilesBeforeRun`: You better save `.go` files before run. So let's save it automatically.

    `code-runner.ignoreSelection`: It's almost impossible to run selected code in Go. So let's ignore it.

    `code-runner.runInTerminal`: Code Runner run code in Output pane by default. I prefer run in Terminal.

    ```json
    {
        "code-runner.saveAllFilesBeforeRun": true,
        "code-runner.ignoreSelection": true,
        "code-runner.runInTerminal": true
    }
    ```

* Editor: Snippet Suggestions

    Show snippet suggestions on top of others to improve coding experiences.

    ```json
    {
      "editor.snippetSuggestions": "top"
    }
    ```

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

* Go Samples
  * `g-cli`: Generate Go CLI sample with [flag](https://golang.org/pkg/flag/) package
  * `g-gin-crud`: Generate [gin](https://github.com/gin-gonic/gin) CRUD sample
  * `g-gorm-crud`: Generate [GORM](https://gorm.io/) CRUD sample
* statements
  * `g-forc`: Snippet for a for loop with custom condition
  * `g-forb`: Snippet for a for loop with a break (infinite loop)
  * `g-forr`: Snippet for a for range loop with better hints
  * `g-iferr`: Snippet for if err != nil with common usage scenario
  * `g-enum` or `g-const-iota`: Generate **enum**-like const
  * `g-trycatch` or `g-recover`: Generate try/catch-like statements
* fmt
  * `fv`: `fmt.Printf()` with variable content
  * `fvv`: `fmt.Printf()` with variable type and content
* builtin
  * `g-make-chan-buffered`: make buffered channel
  * `g-make-chan-unbuffered`: make unbuffered channel
  * `g-make-map`: make map
  * `g-make-slice`: make slice
* log
  * `g-log-new`: `log.New()` with various options
  * `g-log-file`: `log.SetOutput` to a file
  * `g-log-file-console`: `log.SetOutput` to console & file
* math/rand
  * `g-rand`: Generate Random Number snippet
* net/http
  * `g-http-get`: Generate `http.Get` snippet
  * `g-http-post`: Generate `http.Post` snippet
  * `g-http-put`: Generate `http.Put` snippet
  * `g-http-delete`: Generate `http.Delete` snippet
* net/json
  * `g-json-marshal`: Generate `json.Marshal`
  * `g-json-unmarshal`: Generate `json.Unmarshal`
  * `g-json-newdecoder`: Generate `json.NewDecoder`
* ioutil
  * `g-ioutil-writefile`: Generate `ioutil.WriteFile`
  * `g-ioutil-readfile`: Generate `ioutil.ReadFile`
* gin
  * `g-gin-func`: Generate gin func snippet
  * `g-gin-action`: Generate gin action snippet
  * `g-gin-controller`: Generate gin controller snippet
  * `g-gin-binding-tags`: Generate [gin](https://github.com/gin-gonic/gin) binding tags
* swagger
  * `g-swag-main`: Generate swag main snippet
* GORM
  * `g-gorm-open-mysql`: Generate [GORM MySQL](https://gorm.io/docs/connecting_to_the_database.html#MySQL) open
  * `g-gorm-open-sqlite`: Generate [GORM SQLite](https://gorm.io/docs/connecting_to_the_database.html#SQLite) open
  * `g-gorm-open-sqlserver`: Generate [GORM SQL Server](https://gorm.io/docs/connecting_to_the_database.html#SQL-Server) open
  * `g-gorm-open-postgresql`: Generate [GORM PostgreSQL](https://gorm.io/docs/connecting_to_the_database.html#PostgreSQL) open
* Testing
  * `g-test`: Generate `Test_*` func template
  * `g-benchmark`: Generate `Benchmark*` func template

* TODO
  * Add "Comments" to each declaration snippets (`go vet`)

### Dockerfile snippets

* `g-dockerfile`: Multi-stage `Dockerfile` for Go

**Enjoy!**
