FROM golang


RUN go get github.com/google/google-api-go-client/google-api-go-generator
RUN go install github.com/google/google-api-go-client/google-api-go-generator
#RUN ln -s /go/bin/google-api-go-generator /go/bin/gen

WORKDIR /client_gen

#RUN go get code.google.com/p/google-api-go-client/drive/v1
#RUN cd $GOPATH/src/github.com/google/google-api-go-client
#RUN go run google-api-go-generator/gen.go -api_json_file api_json_file.json -gendir /gendir
#RUN go install ./toyapi/v1

# apiToGenerate = String, "api", "*", "The API ID to generate, like 'tasks:v1'. A value of '*' means all."
# useCache = Bool, "cache", true, "Use cache of discovered Google API discovery documents."
# genDir = String, "gendir", "", "Directory to use to write out generated Go files"
# build = Bool, "build", false, "Compile generated packages."
# install = Bool, "install", false, "Install generated packages."
# apisURL = String, "discoveryurl", "https://www.googleapis.com/discovery/v1/apis", "URL to root discovery document"
# publicOnly = Bool, "publiconly", true, "Only build public, released APIs. Only applicable for Google employees."
# jsonFile = String, "api_json_file", "", "If non-empty, the path to a local file on disk containing the API to generate. Exclusive with setting --api."
# output = String, "output", "", "(optional) Path to source output file. If not specified, the API name and version are used to construct an output path (e.g. tasks/v1)."
# googleAPIPkg = String, "googleapi_pkg", "google.golang.org/api/googleapi", "Go package path of the 'googleapi' support package."
# contextPkg = String, "context_pkg", "golang.org/x/net/context", "Go package path of the 'context' support package."

#ENTRYPOINT /go/bin/google-api-go-generator -api_json_file api_json_file.json -gendir ./go
ENTRYPOINT ["/go/bin/google-api-go-generator"]

#CMD ["-api_json_file", "api_json_file.json", "-gendir", "./go"]
CMD ["-help"]
