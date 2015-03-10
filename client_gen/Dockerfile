FROM python:2.7
#FROM google/python

WORKDIR /app
RUN virtualenv /env

#RUN git clone https://code.google.com/p/google-apis-client-generator /app

RUN git clone https://github.com/rwl/google-apis-client-generator.git /app
RUN /env/bin/pip install .
RUN export PYTHONPATH=/app/src:$PYTHONPATH

#RUN pip install google-apis-client-generator

#RUN $(/bin/pwd)/googleapis/codegen/generate_library.py \
#  --input=api_json_file.json --api_name=toyapi --api_version=v1 \
#  --language=java --output_dir=/root/gen

WORKDIR /client_gen

ENTRYPOINT ["/env/bin/python", "/app/src/googleapis/codegen/generate_library.py"]
#ENTRYPOINT ["generate_library"]

# input: A discovery document captured from a discovery service. You can specify either input or api_name/api_version, but not both.
# language: <java|gwt|php>: Target language for the generated library (default: 'java')
# language_variant: which option of "language" to generate for. (default: 'default')
# output_dir: A path to a directory where the generated files will be created.
# output_file: An output file path to contain the archive for the generated library.

#generate_library \
#--input=src/googleapis/codegen/testdata/moderator.v1.json \
#--language=java \
#--output_dir=/tmp/generated
