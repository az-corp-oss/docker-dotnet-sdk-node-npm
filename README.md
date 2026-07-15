# dotnet-sdk-node-npm

Docker image that adds the latest Node LTS version (at time of build) and npm to
[microsoft-dotnet-sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/).

## Supported .NET Versions

| .NET Version | Tags | Node Version |
|:------------:|:----:|:------------:|
| .NET 10 | `10.0`, `latest` | 20.x |
| .NET 8 | `8.0` | 20.x |

## Usage

```bash
# Build for .NET 10 (default)
docker build -t dotnet-sdk-node-npm:10.0 .

# Build for .NET 8
docker build --build-arg TAG=8.0 -t dotnet-sdk-node-npm:8.0 .
```

## Tag Listing

| Tags | OS Version | Node Version | Last Modified |
| ---- |:----------:|:------------:|:-------------:|
| 10.0, latest | Debian 12 | 20.x | 2026-07-15 |
| 8.0 | Debian 12 | 20.x | 2026-07-15 |

## Credits
- @dstockhammer - Original source code
- @azhe403 - Updated .NET SDK & Node versions