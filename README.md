# tirex-mirror

Unofficial mirror of [NX-AI/tirex](https://github.com/NX-AI/tirex) for packaging.

## Legal Notice

This is an unofficial mirror of [NX-AI/tirex](https://github.com/NX-AI/tirex).
See [NOTICE.txt](NOTICE.txt) and [LICENSE_MIRROR.txt](LICENSE_MIRROR.txt) for attribution details.
The original project is licensed under the terms in [LICENSE](LICENSE).

## Purpose

This repository automatically mirrors the upstream TiRex project and publishes it to PyPI as `tirex-mirror` for packaging and distribution purposes.

## Development Notes

### Setting up local environment

```bash
# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install build dependencies
pip install build toml twine
```

### Dry run workflow steps locally

Run commands from `publish.yml`.

Test building the package
```bash
python -m build
```

### Manual publishing

```bash
# Check package contents
twine check dist/*

# Test upload to TestPyPI (optional)
twine upload --repository testpypi dist/*

# Real upload to PyPI
twine upload dist/*
```


### Cleanup after testing

