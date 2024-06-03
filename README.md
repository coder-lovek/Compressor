# Pro Zipper

Pro Zipper is a Python-based algorithm project designed to efficiently compress and decompress files. This project demonstrates various compression techniques and provides a command-line interface for easy file compression and decompression.

## Features

- Efficient file compression and decompression
- Support for multiple file formats
- Command-line interface (CLI) for ease of use
- Error handling and validation
- Extensible architecture for adding new compression algorithms

## Initialization
__init__(self, path): Initializes the object with the given file path and sets up initial variables like heap, codes, and reverse_mapping.

## Inner Class HeapNode
Represents nodes in the Huffman tree. Each node contains a character and its frequency, along with left and right children.
Comparison operators (__lt__ and __eq__) are defined to facilitate heap operations.

## Frequency Dictionary
make_frequency_dict(self, text): Creates a frequency dictionary from the input text.

## Heap Operations
make_heap(self, frequency): Builds a heap from the frequency dictionary.
merge_nodes(self): Merges nodes to build the Huffman tree.

## Generating Huffman Codes
make_codes_helper(self, root, current_code): Recursively generates codes for each character.
make_codes(self): Initiates the code generation process starting from the root of the Huffman tree.

## Encoding and Padding
get_encoded_text(self, text): Encodes the input text using the generated Huffman codes.
pad_encoded_text(self, encoded_text): Pads the encoded text to ensure it fits into an 8-bit structure.

## Byte Array Conversion
get_byte_array(self, padded_encoded_text): Converts the padded encoded text into a byte array.

## Compression
compress(self): Orchestrates the compression process and writes the compressed data to a binary file.

## Decompression
remove_padding(self, padded_encoded_text): Removes the padding from the encoded text.
decode_text(self, encoded_text): Decodes the encoded text back to the original text using the reverse mapping.
decompress(self, input_path): Orchestrates the decompression process and writes the decompressed data to a text file.
