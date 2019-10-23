# npmstar

Very simple node.js utility to install freshest versions of all the dependencies in your `package.json` marked as "*" without mutating `package.js`.

Basically, for:

```
{
  "dependencies": {
    "a": "*",
    "b": "^1.0.0",
    "c": "*"
  }
}
```

it will run:

```
npm install --latest --no-save a c
```

That's it, super simple.
