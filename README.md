# MCP Text Transformation Server

A simple MCP (Model Context Protocol) server that provides a capability to transform text to uppercase.

## Features

- `toUppercase`: Converts any text input to uppercase

## Setup

```bash
# Install dependencies
npm install

# Development (with auto-reload)
npm run dev

# Production build
npm run build
npm start
```

## Usage

The server exposes a single capability that can be called by any MCP client:

```javascript
// Example of using this capability from an MCP client
const result = await client.invoke('toUppercase', {
  text: 'Hello, world!'
});
// result: { text: 'HELLO, WORLD!' }
```

## API

### `toUppercase`

Converts text to uppercase.

**Input:**
- `text` (string): The text to be converted to uppercase

**Output:**
- `text` (string): The uppercase version of the input text

## Error Handling

The server will return an error if:
- The `text` parameter is missing
- The `text` parameter is not a string