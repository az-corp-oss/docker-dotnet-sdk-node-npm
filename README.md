# dotnet-sdk-node-npm & dotnet-runtime-node-npm

Docker images that add the latest Node LTS version (at time of build) and npm to
[microsoft-dotnet-sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/) and
[microsoft-dotnet-aspnet](https://hub.docker.com/_/microsoft-dotnet-aspnet/).

## Images

| Image | Description | Use Case |
|-------|-------------|----------|
| `azhe403/dotnet-sdk-node` | .NET SDK + Node.js + npm | Build & run .NET apps |
| `azhe403/dotnet-runtime-node` | .NET Runtime + Node.js + npm | Run pre-built .NET apps |

## Supported .NET Versions

### SDK Image (`azhe403/dotnet-sdk-node`)

| .NET Version | Tags | Node Version |
|:------------:|:----:|:------------:|
| .NET 10 | `10.0`, `latest` | 20.x |
| .NET 8 | `8.0` | 20.x |

### Runtime Image (`azhe403/dotnet-runtime-node`)

| .NET Version | Tags | Node Version |
|:------------:|:----:|:------------:|
| .NET 10 | `10.0`, `latest` | 20.x |
| .NET 8 | `8.0` | 20.x |

## Usage

### SDK Image

```bash
# Build for .NET 10 (default)
docker build -f sdk/Dockerfile -t dotnet-sdk-node:10.0 .

# Build for .NET 8
docker build --build-arg TAG=8.0 -f sdk/Dockerfile -t dotnet-sdk-node:8.0 .
```

### Runtime Image

```bash
# Build for .NET 10 (default)
docker build -f runtime/Dockerfile -t dotnet-runtime-node:10.0 .

# Build for .NET 8
docker build --build-arg TAG=8.0 -f runtime/Dockerfile -t dotnet-runtime-node:8.0 .
```

## Tag Listing

### SDK Image

| Tags | OS Version | Node Version | Last Modified |
| ---- |:----------:|:------------:|:-------------:|
| 10.0, latest | Debian 12 | 20.x | 2026-07-15 |
| 8.0 | Debian 12 | 20.x | 2026-07-15 |

### Runtime Image

| Tags | OS Version | Node Version | Last Modified |
| ---- |:----------:|:------------:|:-------------:|
| 10.0, latest | Debian 12 | 20.x | 2026-07-15 |
| 8.0 | Debian 12 | 20.x | 2026-07-15 |

## Credits
- @dstockhammer - Original source code
- @azhe403 - Updated .NET SDK & Node versions