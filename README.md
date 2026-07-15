# dotnet-sdk-node-npm

Docker image that adds the latest Node LTS version (at time of build) and npm to
[microsoft-dotnet-sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/).

## Supported .NET Versions

| .NET Version | Tags | Node Version |
|:------------:|:----:|:------------:|
| .NET 10 | `10.0`, `latest` | 20.x |
| .NET 8 | `8.0` | 20.x |
| .NET 7 | `7.0` | 18.x |
| .NET 5 | `5.0` | 14.x |
| .NET 3.1 | `3.1` | 12.x |

## Usage

```bash
# Build for .NET 10 (default)
docker build -t dotnet-sdk-node-npm:10.0 .

# Build for .NET 8
docker build --build-arg TAG=8.0 -t dotnet-sdk-node-npm:8.0 .

# Build for .NET 7
docker build --build-arg TAG=7.0 -t dotnet-sdk-node-npm:7.0 .
```

## Tag Listing

| Tags | OS Version | Node Version | Last Modified |
| ---- |:----------:|:------------:|:-------------:|
| 10.0, latest | Debian 12 | 20.x | 2026-07-15 |
| 8.0 | Debian 12 | 20.x | 2026-07-15 |
| 7.0.100 | Debian 10 | 18.x | 2023-01-15 |
| 5.0.101, 5.0 | Debian 10 | 14.x | 2020-12-09 |
| 3.1.102-buster, 3.1-buster, 3.1.102, 3.1 | Debian 10 | 12.x | 2020-02-21 |
| 3.1.101-buster, 3.1.101 | Debian 10 | 12.x | 2020-02-21 |
| 3.1.100-buster, 3.1.100 | Debian 10 | 12.x | 2020-02-21 |

## Credits
- @dstockhammer - Original source code
- @azhe403 - Updated .NET SDK & Node versions