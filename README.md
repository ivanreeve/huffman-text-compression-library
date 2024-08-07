# Huffman Text Compression Library

This C++ library is my own implementation of Huffman compression and decompression algorithm. Only works for text files.

This project was made as a part of my sophomore year 1st semester final project in Data Structures and Algorithms. The project initially consisted of two separate files and was later combined into a single library.

## Features

### Supports Large Files

The library can handle large files (tested with 10,000,000+ characters).

Larger files may take longer time to finish. 

### Up to 50% Compression Ratio

The Huffman text compression algorithm employed by this library aims to achieve significant reduction in file size while maintaining lossless data compression. While the actual compression ratio may vary depending on factors such as the content and structure of the input text files, tests have shown that the compression ratio can reach up to 50%.

![sample](sample.png)

## Getting Started

To use this library in your C++ project, follow these steps:

1. Clone the repository or download the source code.
2. Include the necessary files in your project. Make sure that the header file is in the appropriate folder location.
3. Use the provided functions for compression and decompression.

## Interface

### Compression

```cpp
bool huffmanlib::compress(string& filename): <filename>.compressed.huffman
```

Takes a string ```filename``` as a parameter. Returns true if the compression is successful. 

Assumes that the filename has ```.txt``` file extension omitted. For example, if the file name is ```sample.txt```, the input should be ```sample```. 

Appends ```.compressed.huffman``` file extension to the compressed file.


### Decompression

```cpp
bool huffmanlib::decompress(string& filename): <filename>.decompressed.txt
```

Takes a string ```filename``` as a parameter. Returns true if the decompression is successful. 

Assumes that the filename has ```.huffman``` file extension omitted. For example, if the file name is ```sample.txt.compressed.huffman```, the input should be ```sample.txt.compressed```. 

Appends ```.decompressed.txt``` file extension to the decompressed file.

## Usage

```cpp
#include <iostream>
#include "huffmanlib.h" // Import the library

using namespace std;
using namespace huffmanlib;

int main() {
    // Compress a text file
    compress("input");

    // Decompress a compressed file
    decompress("compressed");

    return 0;
}
```

## Additional Notes

📝 What is [Huffman Encoding](https://en.wikipedia.org/wiki/Huffman_coding)?.

📝 [storage format](https://stackoverflow.com/questions/759707/efficient-way-of-storing-huffman-tree?fbclid=IwAR0QrUItpdWaI34hHisM8a8z5jzmsLLJYfdOQWALTJpEvINvc8ZGByCE-lU).

## License
This project is licensed under the [MIT License](LICENSE).
