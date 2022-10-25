# Example

GO Package having an example function that returns "Hello, World!"

## Dev / Run locally

`FUNCTION_TARGET=HelloWorld go run cmd/main.go` or execute the VSCode task "Launch Sheet Validator"

## Deploy

`gcloud functions deploy HelloWorld --runtime go116 --trigger-http`

## Principles

This is a separate folder, per Google instructions: _"Where possible, we recommend splitting up large multi-function codebases and putting each function in its own top-level directory as shown above, with its own source and project configuration files. This approach minimizes the number of dependencies required for a particular function, which in turn reduces the amount of memory your function needs."_
<https://cloud.google.com/functions/docs/writing#directory-structure-go>
