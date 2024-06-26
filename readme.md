# HTTP/1.1 versus HTTP/2 


This project serves a simple HTML page that dynamically creates a 10x10 grid of images. It measures and displays the total time taken to render the page, including the loading of all images. 

### Setup Instructions

1. **Install dependencies**:
   ```sh
   npm install
   npm run generate-cert // assumes you have openssl installed on your machine,
   ```

2. **Run the Server**:
   - For HTTP/1.1:
     ```sh
     npm run h1
     ```
   - For HTTP/2:
     ```sh
     npm run h2
     ```

### Comparing HTTP/1.1 vs HTTP/2

HTTP/1.1 introduced several improvements over HTTP/1.0, including persistent connections, chunked transfers, and more efficient use of bandwidth. However, it has limitations such as head-of-line blocking and inefficient use of resources due to its text-based nature and lack of multiplexing.

HTTP/2 addresses these issues by introducing features such as multiplexing, header compression, and binary framing. Multiplexing allows multiple requests and responses to be in flight simultaneously over a single connection, reducing latency and improving resource utilization.

### Testing and Results

To test the performance difference between HTTP/1.1 and HTTP/2:
1. Serve the project using HTTP/1.1 (`npm run h1`) and goto `http://localhost:3001`, set the network to fast 3G.
2. Serve the project using HTTP/2 (`npm run h2`) and goto `https://localhost:3002`, set the network to fast 3G.

### Credits

- [How to use HTTP/2 with Express](https://typeofnan.dev/how-to-use-http2-with-express/)
- [How HTTP/2 Works, Performance, Pros & Cons and More - Hussein Nasser](https://www.youtube.com/watch?v=fVKPrDrEwTI)
