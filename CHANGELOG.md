# Change Log

All notable changes to the "go-extension-pack" extension pack will be documented in this file.

## 0.11.0 - 2020-11-22

* Remove [Go Doc](https://marketplace.visualstudio.com/items?itemName=msyrus.go-doc) extension
  * The Go Language Server has already did a good job. So there is no need to get doc shown in OUTPUT pane.
* Add `g-json-marshalindent` snippet

## 0.10.0 - 2020-11-21

* Add `g-benchmark` snippet
* Add `g-test` snippet

## 0.9.1 - 2020-11-12

* Bug fixed: `g-json-unmarshal` and `g-json-marshal` snippet

## 0.9.0 - 2020-11-10

* Add `g-dockerfile` snippet: Multi-stage `Dockerfile` for Go

## 0.8.0 - 2020-11-05

* Update `g-json-marshal`, `g-json-unmarshal` and `g-json-newdecoder` snippets
* Update `g-http-get`, `g-http-post`, `g-http-put`, `g-http-delete` snippets
* Add more Go snippets
  * `g-enum` or `g-const-iota`: Generate **enum**-like const
  * `g-trycatch` or `g-recover`: Generate try/catch-like statements

## 0.7.0 - 2020-11-04

* Add more Go snippets
  * log
    * `g-log-new`: `log.New()` with various options
    * `g-log-file`: `log.SetOutput` to a file
    * `g-log-file-console`: `log.SetOutput` to console & file
  * swagger
    * `g-swag-main`: Generate swag main snippet
  * gin
    * `g-gin-func`: Generate gin func snippet
    * `g-gin-action`: Generate gin action snippet
    * `g-gin-controller`: Generate gin controller snippet
  * math/rand
    * `g-rand`: Generate Random Number snippet
  * net/http
    * `g-http-get`: Generate `http.Get` snippet
    * `g-http-post`: Generate `http.Post` snippet
    * `g-http-put`: Generate `http.Put` snippet
    * `g-http-delete`: Generate `http.Delete` snippet

## 0.6.0 - 2020-10-29

* Add `make` snippets
  * `g-make-chan-buffered`: make buffered channel
  * `g-make-chan-unbuffered`: make unbuffered channel
  * `g-make-map`: make map
  * `g-make-slice`: make slice
* Add more statement snippets
  * `fvv`: `fmt.Printf()` with variable type and content
  * `g-forr`: Snippet for a for range loop with better hints
  * `g-iferr`: Snippet for if err != nil with common usage scenario

## 0.5.1 - 2020-10-29

* Update README.md for `gopls` description

## 0.5.0 - 2020-10-29

* Add more Go snippets
  * Go Samples
    * `g-cli`: Generate Go CLI sample with [flag](https://golang.org/pkg/flag/) package
    * `g-gin-crud`: Generate [gin](https://github.com/gin-gonic/gin) CRUD sample
    * `g-gorm-crud`: Generate [GORM](https://gorm.io/) CRUD sample
  * net/json
    * `g-json-marshal`: Generate `json.Marshal`
    * `g-json-unmarshal`: Generate `json.Unmarshal`
    * `g-json-newdecoder`: Generate `json.NewDecoder`
  * ioutil
    * `g-ioutil-writefile`: Generate `ioutil.WriteFile`
    * `g-ioutil-readfile`: Generate `ioutil.ReadFile`
  * gin
    * `g-gin-binding-tags`: Generate [gin](https://github.com/gin-gonic/gin) binding tags
  * GORM
    * `g-gorm-open-mysql`: Generate [GORM MySQL](https://gorm.io/docs/connecting_to_the_database.html#MySQL) open
    * `g-gorm-open-sqlite`: Generate [GORM SQLite](https://gorm.io/docs/connecting_to_the_database.html#SQLite) open
    * `g-gorm-open-sqlserver`: Generate [GORM SQL Server](https://gorm.io/docs/connecting_to_the_database.html#SQL-Server) open
    * `g-gorm-open-postgresql`: Generate [GORM PostgreSQL](https://gorm.io/docs/connecting_to_the_database.html#PostgreSQL) open

## 0.4.2 - 2020-07-30

* Add more [gopls](https://github.com/golang/vscode-go/blob/master/docs/gopls.md) information and settings in the README.md

## 0.4.1 - 2020-07-30

* Add [Go Doc](https://marketplace.visualstudio.com/items?itemName=msyrus.go-doc) extension
* Move all the Visual Studio Code recommended settings together.
* Add **Usage** information for each extensions.

## 0.3.4 - 2020-07-29

* Update README.md

## 0.3.3 - 2020-07-28

* Put some testing function template snippets together.
* Add some recommended keyboard bindings.

## 0.3.1 - 2020-07-27

* change vscode dep. to `^1.41.0`.

## 0.3.0 - 2020-07-27

* Add [vscode-proto3](https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3) extension
* Add recommended settings in README:
  * `"go.useLanguageServer": true`
  * `"editor.snippetSuggestions": "top"`
* Add two statements snippets
  * `forc`: for loop with custom conditions
  * `forb`: for loop with break (infinite loop)

## 0.2.1 - 2020-07-26

* Add a recommended setting  `"code-runner.ignoreSelection": true` to [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner).
* Add custom `fv` snippet: fmt.Printf() with variable content

## 0.2.0 - 2020-07-26

* Update README.md
  * Reorganize `Go Snippets` section for better understanding the context of the snippets
  * Add **Recommended Settings** for [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
  * Add `Recommended Settings` section for fine-tuning Visual Studio Code environment

## 0.1.0 - 2020-07-24

* Initial release
