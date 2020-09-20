# bundler

<br />
<p align="center">
  <a href="https://github.com/vorteil/bundler">
    <img src="assets/vlogo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">bundler</h3>
  <h5 align="center">tool to create or modify bundles for vorteil.io</h5>
</p>

<hr/>

The bundler tool helps to build, modify, extract or inspect [vorteil](https://github.com/vorteil/vorteil) bundles. It contains only four commands:

### create

Creates a vorteil.io bundle based on the files in the provided toml configuration file.

```sh
bundler create 11.22.3 /path/to/bundle.toml > vorteil-11.22.3
```

### extract

Extracts all files from an existing bundle to the provided folder.

```sh
bundler extract /path/to/kernel-99.99.1 /tmp/folder
```

### inspect

Inspects the bundle and returns all file names and tags in this bundle.

```sh
bundler inspect /path/to/kernel-99.99.1
```

### process

Create a "live" bundle for the tags provided. If run with argument "dry-run" it only shows the files being on the bundle with those tags applied.

```sh
bundler process /path/to/kernel-99.99.1 tcpdump --dry-run
bundler process /path/to/kernel-99.99.1 tcpdump > file
```

## More Information:

* [vorteil.io tools](https://github.com/vorteil/vorteil) - Build vorteil.io micro virtual machines
* [vbundler](https://github.com/vorteil/vbundler) - What are bundles?
* [docs](https://docs.vorteil.io/)

## Building

```sh
go build -o bundler cmd/main.go
```

#### License

Distributed under the Apache 2.0 License. See `LICENSE` for more information.
