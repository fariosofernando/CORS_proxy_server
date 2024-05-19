## CORS Proxy Server

This repository contains a CORS Proxy Server implementation designed to facilitate cross-origin resource sharing by acting as an intermediary between clients and target APIs. It allows developers to bypass CORS restrictions when accessing resources from different origins, making development and testing easier.

### Features

- **Simple Setup**: Easy to configure and deploy.
- **Flexible**: Supports various HTTP methods (GET, POST, etc.).
- **Security**: Handles and forwards headers securely, including authorization tokens.
- **Customizable**: Allows for custom headers and configurations as needed.
- **Hosted on Vercel**: Easily deployable to Vercel for seamless integration and scalability.

### How It Works

The CORS Proxy Server intercepts requests from the client, modifies headers as necessary to comply with CORS policies, and forwards the request to the target API. It then sends the API's response back to the client, ensuring smooth communication without CORS errors.

### Getting Started

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/cors-proxy-server.git
    cd cors-proxy-server
    ```

2. **Install Dependencies**:
    ```bash
    npm install
    ```

3. **Run the Server**:
    ```bash
    npm start
    ```

4. **Deploy to Vercel**:
    - Follow Vercel's deployment guide to deploy your proxy server.

### Configuration

- Modify `config.json` to change the default settings such as port number and allowed origins.
- Add custom headers or modify request handling in `server.js`.

### Usage

Send your requests to the proxy server running at `http://localhost:3000` (or your Vercel URL) with the desired target API URL and method.

### Example

```javascript
fetch('http://localhost:3000/your-api-endpoint', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer your-token',
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    key: 'value',
  }),
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

### Contributions

Contributions are welcome! Feel free to submit issues or pull requests to help improve this project.

### License

This project is licensed under the MIT License.