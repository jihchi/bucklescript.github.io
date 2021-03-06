---
id: nodejs-special-variables
title: NodeJS Special Variables
---

NodeJS has several file local variables: `__dirname`, `__filename`, `_module`, and `require`. Their semantics are more like macros instead of functions.

`bs.node` exposes support for these.

```ocaml
let dirname : string option = [%bs.node __dirname]
let filename : string option = [%bs.node __filename]
let _module : Node.node_module option = [%bs.node _module]
let require : Node.node_require option = [%bs.node require]
```

Reason syntax:

```reason
let dirname: option(string) = [%bs.node __dirname];
let filename: option(string) = [%bs.node __filename];
let _module: option(Node.node_module) = [%bs.node _module];
let require: option(Node.node_require) = [%bs.node require];
```
