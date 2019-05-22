Modified https://github.com/henryw374/tick-on-shadow-cljs-demo to repro this case.

When using juxt/tick library with shadow-cljs, release is broken for node-script/node-library target, but does work for browser target.

```
shadow-cljs release node --debug
node out/test.js
```

Should result in TypeError: this.$dayOfMonth$ is not a function

Not sure if this is a shadow-cljs issue, or a tick issue.