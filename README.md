# Quadtree-Based Image Compression & Decompression System

Welcome to the repository for the Quadtree-Based Image Compression & Decompression System, a Java application designed for image processing. This system leverages the quadtree data structure to compress and decompress images, optimizing storage without significantly compromising on quality.

## Project Overview

The heart of this system lies within the `Utility.java` file, where the "magic" of compression and decompression happens. The application breaks down images into a quadtree, a tree data structure in which each internal node has exactly four children. Quadtrees are particularly efficient for partitioning a two-dimensional space by recursively subdividing it into four quadrants or regions.

## Features

- **Image Compression**: Compress images into a binary quadtree structure, significantly reducing file size.
- **Image Decompression**: Reconstruct images from their quadtree representation, preserving quality.
- **Customizable Compression Levels**: Adjust the compression threshold and minimum size for quadtree division according to your needs.
- **Image Quality Metrics**: Evaluate the quality of compressed images using PSNR, MAE, and MSE calculators.
- **User-Friendly Interface**: Simple and intuitive methods for easy operation.

## How It Works

### Compression

1. The image is represented as a 3D array of pixels (RGB values).
2. The `Compress` function in `Utility.java` initiates the quadtree construction based on a given threshold and minimum size for quadtree division.
3. The quadtree is serialized and saved as a `.bin` file, representing the compressed image.

### Decompression

1. The `.bin` file is deserialized to reconstruct the quadtree structure.
2. The `Decompress` function in `Utility.java` traverses the quadtree to regenerate the image pixel array.
3. The decompressed image is outputted, ready for use and viewing.

## Getting Started

To get started with the Quadtree-Based Image Compression & Decompression System:

1. Clone the repository to your local machine.
2. Navigate to the `src` directory where `Utility.java` is located.
3. Compile the Java files using your preferred Java compiler or IDE.
4. Run the application via the command line or through your IDE.
