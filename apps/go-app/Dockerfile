# Start with a base GoLang image
FROM golang:1.20-bullseye

# Set the working directory inside the container
WORKDIR /app

# Copy the Go modules manifests
COPY go.mod ./

# Download and cache Go modules
RUN go mod download

# Copy the rest of the application code
COPY . .

# Build the Go application
RUN go build -o main .

# Expose the port your application listens on
EXPOSE 3030

# Set the command to run the executable
CMD ["./main"]