# Schema Parser

## Prerequisites

* A Python installation ($\ge$ v3) 
* Install script specific python modules `jsonschema` & `PyYaml` .  Can be install using `pip install -r requirements.txt`

## Usage Examples

### Header file generation

Builds a set of header files, placing them in default directory `./output`

`python3 parser.py ./test_data/simple.rvm-csi.yaml`

### Adoc file generation

Builds a set of header files, placing them in default directory `./adoc_output`

`python3 parser.py --generate-docs ./test_data/simple.rvm-csi.yaml`

Linked HTML docs can be generated from the .adoc files e.g.

`cd ./adoc_output`
`asciidoctor *.adoc`

## Testing

*NB incomplete*

Top level parser tests:

`python3 parser_test.py`

Header generation tests:

`python3 header_gen_test.py`