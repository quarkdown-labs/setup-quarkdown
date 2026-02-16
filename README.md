# setup-quarkdown ![GitHub Tag](https://img.shields.io/github/v/tag/quarkdown-labs/setup-quarkdown?label=version&color=mediumseagreen)

A GitHub Action to install the [Quarkdown](https://github.com/iamgio/quarkdown) CLI.

## Usage

```yaml
steps:
  - uses: quarkdown-labs/setup-quarkdown@v1

  - run: quarkdown c main.qd --pdf
```

### Install a specific version

By default, the latest stable release of Quarkdown is installed.

To install a specific version, use the `quarkdown-version` input:

```yaml
steps:
  - uses: quarkdown-labs/setup-quarkdown@v1
    with:
      quarkdown-version: '1.12.0'
```

Use `devbuild` to use the latest Quarkdown build from the main branch instead (potentially unstable).

## Windows disclaimer

This action supports Windows. Quarkdown is set up via Scoop, resulting in a longer setup time. If a Quarkdown version is specified, it is ignored on Windows, as only the latest Quarkdown version is available on Scoop.