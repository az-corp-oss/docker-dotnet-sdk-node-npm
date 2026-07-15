ARG TAG="latest"

FROM mcr.microsoft.com/dotnet/aspnet:${TAG}

# Install Node.js 20.x using NodeSource new method
RUN apt-get update && apt-get install -y --no-install-recommends ca-certificates curl gnupg \
 && mkdir -p /etc/apt/keyrings \
 && curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg \
 && echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_20.x nodistro main" | tee /etc/apt/sources.list.d/nodesource.list \
 && apt-get update \
 && apt-get install -y --no-install-recommends nodejs \
 && npm i -g npm pnpm \
 && echo "node version: $(node --version)" \
 && echo "npm version: $(npm --version)" \
 && echo "pnpm version: $(pnpm --version)" \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /app

ENTRYPOINT ["dotnet", "app.dll"]
