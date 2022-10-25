# Sheet

Boilerplate for writing Cloud Functions in Go on Google Cloud Platform. Based on <https://github.com/GoogleCloudPlatform/functions-framework-go#functions-framework-for-go>

## Structure

Each folder in this project will have one function, as per Google instructions: _"Where possible, we recommend splitting up large multi-function codebases and putting each function in its own top-level directory as shown above, with its own source and project configuration files. This approach minimizes the number of dependencies required for a particular function, which in turn reduces the amount of memory your function needs."_
<https://cloud.google.com/functions/docs/writing#directory-structure-go>

Each function will have its own `cmd/main.go` file, for local testing. When deploying, only the function as described in the init of the package will be used.

## How to add your own function

- Replicate the example folder, having a `go.mod` file and `.go` files for your functionality.
- Run with possible `cmd/main.go` file: `FUNCTION_TARGET=HelloWorld go run cmd/main.go`
- You could add the function to the `.vscode/launch.json` file for easy launching/devving

_...Where HelloWorld is your own function name._

## How to deploy your own function

From within the function directory:

```shell
gcloud functions deploy HelloWorld --runtime go116 --trigger-http
```
