# Client generator

[Docker][docker] [images][hub] for generating client [libraries][] from
[discovery documents][discovery].

Default working directory inside the image is `/client_gen`. Mount the current
working directory as a volume to access the discovery document and to write the
generated client source code.

    $ docker run -v $(pwd):/client_gen -t rlincoln/client_gen --input=toyapi.v1.json --output_dir=java/ --language=java

Language may be `csharp`, `dart`, `gwt`, `java`, `php` or `python`.

## Go example

See [`google-api-go-generator`][go]

    $ docker run -v $(pwd):/client_gen -t rlincoln/client_gen:go -api_json_file toyapi.v1.json -gendir ./go

## Dart client library

Generate with [`discovery_api_dart_client_generator`][dart]

    $ docker run -v $(pwd):/client_gen -t rlincoln/client_gen:dart --no-prefix -i toyapi.v1.json -o ./dart

[docker]: https://www.docker.com/
[hub]: https://registry.hub.docker.com/u/rlincoln/client_gen/
[libraries]: https://developers.google.com/discovery/libraries/
[discovery]: https://developers.google.com/discovery/v1/reference/apis/
[go]: https://github.com/google/google-api-go-client/
[dart]: https://github.com/dart-gde/discovery_api_dart_client_generator/
