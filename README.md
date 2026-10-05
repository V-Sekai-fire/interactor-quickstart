# interactor-quickstart

An Elixir tool that brings up the fabric's orchestration engine and its key-value store as local containers under systemd.

## What it is for

It provisions a local copy of the multiplayer fabric's cluster: it builds the container images, writes the systemd units that run them, starts the key-value store and the orchestration engine, and registers a runner. It uses only the standard library, so it runs before anything else exists. The decisions behind it are the RFDs in `rfd/`.

## Build and run

```sh
mix test
mix run -e 'RivetFabric.CLI.main(["doctor"])'
```

`doctor` checks the prerequisites, and running the CLI with no command lists the others.

## Licence

MIT; see `LICENSE`.
