FROM google/dart

RUN git clone https://github.com/dart-gde/discovery_api_dart_client_generator /app
WORKDIR /app

#ADD pubspec.* /app/
RUN pub get
#ADD . /app
#RUN pub get --offline
#RUN ln -s /app/packages /app/bin/packages

#RUN cp bin/generate.dart generate.dart
WORKDIR /client_gen
#ADD toyapi.v1.json /client_gen/
#ADD toyapi.rpc.discovery /client_gen/

CMD ["-h"]
ENTRYPOINT ["/usr/bin/dart", "/app/bin/generate.dart"]


#FROM debian:testing

# Clone or fork discovery_api_dart_client_generator
#RUN git clone https://github.com/dart-gde/discovery_api_dart_client_generator
# cd discovery_api_dart_client_generator
# pub install

# Generate your client library:
#RUN URL='https://my-app-id.appspot.com/_ah/api/discovery/v1/apis/greeting/v1/rest'
#RUN curl -s -o greetings.rpc.discovery $URL
#RUN bin/generate.dart --no-prefix -i greetings.rpc.discovery -o ../
