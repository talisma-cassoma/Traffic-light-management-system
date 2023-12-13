# Use the official Ubuntu image as the base image
FROM ubuntu:latest

# Set the working directory to /app
WORKDIR /app

# Update the package list and install necessary dependencies
RUN apt-get update -y && \
    apt-get install -y \
    cmake \
    make \
    libgl1-mesa-dev 
    # libsfml-dev \
    # libimgui-dev

# Copy the current directory contents into the container at /app
COPY . /app

# Create a build directory
RUN mkdir build

# Set the working directory to /app/build
WORKDIR /app/build

# Generate makefile with CMake
RUN cmake ..

# Build the project
RUN make

# Set the working directory back to /app
WORKDIR /app

# Command to run your application
CMD ["./build/a"]
