# asdf-openscad

[OpenSCAD](https://openscad.org/) plugin for [asdf](https://asdf-vm.com/).

OpenSCAD is a script-based 3D CAD modeler. Useful for managing multiple versions or pinning a specific release per project via `.tool-versions`.

## Requirements

- **macOS**: `hdiutil` (built-in)
- **Linux x86_64**: AppImage support (fuse or `--appimage-extract-and-run`)
- `curl`, `git`

> OpenSCAD only publishes pre-built binaries for macOS and Linux x86_64.
> Linux arm64 is not supported upstream.

## Install

```bash
asdf plugin add openscad https://github.com/<you>/asdf-openscad.git
asdf install openscad 2021.01
asdf set openscad 2021.01
openscad --version
```

## Usage

```bash
asdf list all openscad          # list all versions
asdf install openscad 2021.01   # install specific version
asdf install openscad latest    # install latest stable
asdf set openscad 2021.01       # set version for current project
asdf set -u openscad 2021.01    # set global default
```

## `.tool-versions`

```
openscad 2021.01
```

## Notes

- Binary releases start at `2021.01`. Older versions listed by `asdf list all` only have source tarballs upstream.
- macOS: installs `OpenSCAD.app` bundle + a `bin/openscad` wrapper for CLI use.
- Linux: installs the official AppImage as `openscad` in PATH.
- Set `GITHUB_API_TOKEN` to avoid GitHub API rate limits on `asdf list all`.

## License

MIT
