# mocha-http-test-template

[![CI](https://github.com/osisdie/mocha-http-test-template/actions/workflows/ci.yml/badge.svg)](https://github.com/osisdie/mocha-http-test-template/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/osisdie/mocha-http-test-template)](LICENSE)
[![Node](https://img.shields.io/badge/node-%3E%3D14-brightgreen)](https://nodejs.org/)

Minimal Mocha + Axios template for JSON-driven HTTP endpoint testing. Define your endpoints in a config file, and a single `forEach` loop runs the entire test scenario.

*series of code_for_fun*

## Requirements

- Node.js >= 14

## Quick Start

```sh
# Clone the repository
git clone https://github.com/osisdie/mocha-http-test-template.git
cd mocha-http-test-template

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

[MIT](LICENSE)
