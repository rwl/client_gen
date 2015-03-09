# Client generator

Docker images for generating client libraries from discovery documents.

## Go example

Default working directory inside the image is `/root`. Default discovery
document name is `api_json_file.json`. Default output directory is `go/`.

    $ docker run -v $(pwd):/root -t rlincoln/client_gen:go
