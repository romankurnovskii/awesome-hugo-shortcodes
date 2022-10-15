## reactblock

Use react app at any Hugo post

## path

{theme}/layouts/shortcodes/reactblock.html

## Requirements

Installed react from the root `package.json`

or

import React from CDN in header.html

*Example:*

{theme}/layouts/partials/head.html
```
<html>
...
<script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
...
```

## Parameters

- **src** - full path to js/jsx script
- **divRender** - optional, `div id` where react will render the app 


## Usage

```

{{< reactblock src="full-path-to-script.jsx" >}}

{{< reactblock src="https://romankurnovskii.com/ru/posts/integrate-hugo-react/react-count-example.jsx" divRender="react_count_example">}}

```

### React script example

```jsx
import { useState } from "react";
import { createRoot } from "react-dom/client";

const divRender = "_react_count_example_"; // "__react_block_render__";

const MyCountButton = () => {
  const [count, setCount] = useState(Math.round(Math.random() * 100));
  return (
    <>
      <button onClick={() => setCount(count + 1)}>{count}</button>
    </>
  );
};

const container = document.getElementById(divRender);
const root = createRoot(container);
root.render(<MyCountButton />);
```

## Demo

- [count button](https://github.com/romankurnovskii/romankurnovskii.github.io/blob/main/content/posts/integrate-hugo-react/react-count-example.jsx)

## Author

- [Roman Kurnovskii](https://github.com/romankurnovskii)
