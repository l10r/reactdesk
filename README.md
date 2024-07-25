
# ReactDesk

ReactDesk is an extension of [Dustin Brett's daedalOS](https://github.com/DustinBrett/daedalOS), transforming it into a reusable and portable React component package for building web desktop environments.

## Installation

To get started with ReactDesk, first install the package via npm:

```bash
npm install reactdesk
```

## Usage

Here's an example of how to integrate ReactDesk into your project:

```tsx
import React from "react";
import ReactDOM from "react-dom/client";
import ReactDesk from "reactdesk";
import "./index.css";

const ReactDeskTest = (
  <div
    style={{
      width: "100vw",
      height: "100vh",
      position: "absolute",
      top: 0,
      left: 0,
    }}
  >
    <ReactDesk
      applications={[
        {
          name: "Hello World",
          icon: "",
          windowContent: <h1>Hello World App</h1>,
          taskbarPin: true,
          runOnStart: true,
          windowConfig: {
            maximized: false,
          },
        },
      ]}
    />
  </div>
);

ReactDOM.createRoot(document.getElementById("root")!).render(ReactDeskTest);
```
