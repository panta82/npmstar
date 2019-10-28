# npm-install-star

Very simple node.js utility to install freshest versions of all the dependencies in your `package.json` marked as "*" without mutating `package.js`.

```
npm i -g npm-install-star
```

This will create executable `npmstar`.

So when you execute

```bash
$ npmstar
```

in a project with `package.json` like this:

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
npm install --latest --no-save --package-lock-only a c
```

That's it, super simple.
