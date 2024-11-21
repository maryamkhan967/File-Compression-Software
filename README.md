File Compression Software

Overview
This project implements file compression software integrating Huffman Coding and Run-Length Encoding (RLE) to enhance storage and data transmission efficiency. Both algorithms are lossless, reducing resource consumption while maintaining data integrity. The software enables comparative analysis of their performance, efficiency, and suitability for various data types.

Algorithms Used
1. Huffman Coding

Purpose: Variable-length compression for text data with varying character frequencies.
Key Steps:
Build a frequency table for characters.
Construct a binary tree with priority queue-based merging of nodes.
Assign binary codes based on tree traversal.
Efficiency:
Time Complexity: O(n log n) due to tree construction.
Space Complexity: O(n) for tree and frequency table.

3. Run-Length Encoding (RLE)
Purpose: Simplified compression for data with repetitive patterns.
Key Steps:
Encode consecutive characters as the count followed by the character (e.g., AAAABBBCC → 4A3B2C).
Efficient for images or binary files with repeated data.
Efficiency:
Time Complexity: O(n) for sequential processing.
Space Complexity: Minimal, proportional to compressed size.

Implementation

Huffman Coding
Encoding (compression):
Command to compile and run:

g++ -o huffman_program huffman.cpp encode.cpp decode.cpp -std=c++11

g++ encode.cpp huffman.cpp -o main

./main inputFile.txt outputFile.txt

Decoding (decompression):
Command to compile and run:

g++ decode.cpp huffman.cpp -o main

./main outputFile.txt inputFile.txt

Run-Length Encoding (RLE)
Encoding:
Command to compile and run:

g++ encode.cpp -o encode

./encode inputFile.txt outputFile.txt

Decoding:
Command to compile and run:

g++ decode.cpp -o decode

./decode outputFile.txt inputFile.txt

Conclusion
Huffman Coding: Best for text files with varying character frequencies.
RLE: Ideal for files with repetitive data patterns.
Use cases depend on data characteristics, allowing users to optimize storage and transmission.
