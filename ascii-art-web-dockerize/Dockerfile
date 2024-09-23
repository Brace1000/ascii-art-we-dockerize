# Use an official Golang runtime as a parent image
FROM golang:1.22.2-alpine AS builder

# Set the Current Working Directory inside the container
WORKDIR /ascii-art-web-dockerize

# Copy the Go Modules manifests
COPY go.mod ./

# Download all dependencies. Dependencies will be cached if the go.mod and go.sum files are not changed
RUN go mod download

# Copy the source code into the container
COPY . .

# Build the Go app
RUN CGO_ENABLED=0 GOOS=linux go build -o main .

# Metadata as labels
LABEL maintainer="Oiko Brian <oikobrian99@gmail.com>,Shayo Victor <victorshayo92@gmail.com>"
LABEL version="1.0"
LABEL description="An image file for a web server that accepts text as input and displays the output using ASCII characters."
# Expose the port the app runs on
EXPOSE 8082

# Command to run the executable
CMD ["./main"]
