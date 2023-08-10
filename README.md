# useHref

`useHref` is a custom React hook that provides functionalities for handling URL parameters.

## Installation

To use `useHref` in your React project, you need to install it as a dependency.

```

npm i use-href

```

## Usage

Import the `useHref` hook in your React component and start using it.

```jsx
import useHref from 'use-href';

function MyComponent() {
  const { addQueryParam, deleteQueryParam, getQueryParam } = useHref();

  // Your component code here

  return (
    // JSX for your component
  );
}

export default MyComponent;
```

## API Reference

### `addQueryParam(paramName: string, value: string): void`

Add a new query parameter to the URL.

- `paramName`: The name of the query parameter.
- `value`: The value of the query parameter.

### `deleteQueryParam(paramName: string): void`

Delete a query parameter from the URL.

- `paramName`: The name of the query parameter to delete.

### `getQueryParam(paramName: string): string | null`

Retrieve the value of a query parameter from the URL.

- `paramName`: The name of the query parameter to retrieve.

## Example

```jsx
import React from "react";
import useHref from "use-href";

function MyComponent() {
  const { addQueryParam, deleteQueryParam, getQueryParam } = useHref();

  const handleAddClick = () => {
    addQueryParam("page", "2");
  };

  const handleDeleteClick = () => {
    deleteQueryParam("page");
  };

  const handleGetClick = () => {
    const pageValue = getQueryParam("page");
    console.log("Page:", pageValue);
  };

  return (
    <div>
      <button onClick={handleAddClick}>Add Query Param</button>
      <button onClick={handleDeleteClick}>Delete Query Param</button>
      <button onClick={handleGetClick}>Get Query Param</button>
    </div>
  );
}

export default MyComponent;
```

## License

This project is licensed under the [ISC License](LICENSE).

## Issues

If you encounter any issues or have questions, please [open an issue](https://github.com/akinkloluwami/use-href/issues) on GitHub.
