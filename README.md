# npm-install-star

Very simple node.js utility to install the freshest versions of all the dependencies
in your `package.json` marked as `"*"` or `"latest"`, without mutating `package.js`.
If exists, `package.lock` will be updated to reflect the latest versions installed.

```
npm i -g npm-install-star
```

This will create executable `npmstar`.

So when you run

```bash
$ npmstar
```

in a project with `package.json` like this:

```
{
  "dependencies": {
    "a": "*",
    "b": "^1.0.0",
    "c": "latest"
  }
}
```

it will run (more or less):

```
npm install --latest --no-save a c
```

That's it, super simple.
