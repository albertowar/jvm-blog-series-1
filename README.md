# jit-vs-aotc

## Slides
To present the slides (requires node.js):

```
cd reveal.js
npm install
cd ..
make present
```

## To run locally
In order to run any of the solutions locally:

```
make compile-cloop
ITERATIONS=1 make run-cloop
```

## To visualize the JIT in action
1. Run script in debug mode: `ITERATIONS=1 make run-cloop-diag`.
2. Open JIT watch.
3. Configure JIT watch to use:
    * The JDK and the root of the repository as **Source locations**.
    * The root of the repository as **Class locations**.

> Increase the number of iterations in order to force different tiers of compilation.

## Notes
For the AOTC execution, it is required to run this in advance:

```
aotc-compile-module
```

This will precompile the java.base module (300 MB) which can be reused across all aotc options.