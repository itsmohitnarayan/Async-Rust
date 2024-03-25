# Rust HTTP Client 🦀🚀

A simple Rust project showcasing an HTTP client using the reqwest crate, with error handling using the error_chain crate.

## Features 🌟

- **HTTP Request:** Make HTTP GET requests to a specified URL.
- **Status Display:** Print the HTTP status of the response.
- **Header Display:** Print the headers of the HTTP response.
- **Body Display:** Print the body of the HTTP response.

## Error Handling 🚨

- Uses the error_chain crate for convenient and expressive error handling.
- Handles standard I/O errors and reqwest HTTP request errors.

## Usage 🛠️

1. Clone the repository:

   ```bash
   git clone https://github.com/itsmohitnarayan/Async-Rust.git
   ```

2. Navigate to the project directory:

   ```bash
   cd yourproject
   ```

3. Build and run the project:

   ```bash
   cargo run
   ```

## Dependencies 📦

- **reqwest:** A simple HTTP client for Rust.
- **error_chain:** Provides a set of declarative macros for defining custom error types.

## Getting Started 🚀

To get started with the project, simply clone the repository and run the code. Make sure to customize the URL in the code to match your desired endpoint.

```rust
#[tokio::main]
async fn main() -> Result<()> {
    let res = reqwest::get("http://httpbin.org/get").await?;
    println!("Status: {}", res.status());
    println!("Headers:\n{:#?}", res.headers());

    let body = res.text().await?;
    println!("Body:\n{}", body);

    Ok(())
}
```

Feel free to explore and modify the code according to your needs.

## Contributing 🤝

Contributions are welcome! Feel free to open issues or submit pull requests.

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
