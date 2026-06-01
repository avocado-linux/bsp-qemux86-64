# bsp-qemux86-64

Board support for QEMU x86-64 virtual machine

## Using this extension

`bsp-qemux86-64` is an [Avocado](https://avocadolinux.org) extension — a reusable fragment of
build- and runtime-configuration that you compose into your own Avocado project. To use it,
declare it as a package-sourced extension in your `avocado.yaml` and add it to a runtime:

```yaml
extensions:
  avocado-bsp-qemux86-64:
    source:
      type: package
      version: "*"        # or pin an exact version

runtimes:
  my-runtime:
    extensions:
      - avocado-bsp-qemux86-64
```

Then `avocado build`. The extension's config is fetched from your target's package feed
and merged into your project at build time.
