# node-tiny-mocha-HTTP-unittest

[![CI](https://github.com/osisdie/node-tiny-mocha-HTTP-unittest/actions/workflows/ci.yml/badge.svg)](https://github.com/osisdie/node-tiny-mocha-HTTP-unittest/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/osisdie/node-tiny-mocha-HTTP-unittest)](LICENSE)
[![Node](https://img.shields.io/badge/node-%3E%3D14-brightgreen)](https://nodejs.org/)

A minimal Node.js application that reads endpoint configurations from a JSON file and runs HTTP tests using [Mocha](https://mochajs.org/) + [Axios](https://axios-http.com/). A single `forEach` loop drives the entire test scenario -- use it as a template for your own HTTP integration tests.

*series of code_for_fun*

## Requirements

- Node.js >= 14

## Quick Start

```sh
# Clone the repository
git clone https://github.com/osisdie/node-tiny-mocha-HTTP-unittest.git
cd node-tiny-mocha-HTTP-unittest

# Install dependencies
npm install

# Run tests
npm test
```

## Configuration

Edit `conf/config.json` to define the endpoints you want to test.

Each host group contains an array of request objects:

```json
{
  "url": "https://httpbin.org/get",
  "method": "GET",
  "body": null,
  "headers": {}
}
```

Groups named `example` are automatically skipped during test runs.

## Project Structure

```
.
├── app.js              # Entry point (prints startup message)
├── conf/
│   └── config.json     # Endpoint definitions
├── lib/
│   └── util.js         # HTTP request helper & utilities
├── test/
│   └── http_test.js    # Mocha test suite
└── package.json
```

## License

[BSD-3-Clause](LICENSE) &copy; Kevin Wu
