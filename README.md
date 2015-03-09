# Client generator

Docker images for generating client libraries from discovery documents.

## Go example

Default working directory inside the image is `/client_gen`. Mount the current
working directory as a volume to access the discovery document and to write the
generated client source code.

    $ docker run -v $(pwd):/client_gen -t rlincoln/client_gen:go -api_json_file toyapi.v1.json -gendir ./go

## Dart client library

Default working directory inside the image is `/client_gen`.

    $ docker run -v $(pwd):/client_gen -t rlincoln/client_gen:dart --no-prefix -i toyapi.v1.json -o ./dart
