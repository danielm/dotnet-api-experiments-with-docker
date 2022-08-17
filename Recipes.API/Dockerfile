# Build Stage
FROM mcr.microsoft.com/dotnet/sdk:6.0-alpine AS build
WORKDIR /src
COPY Recipes.API.csproj .
RUN dotnet restore
# --disable-parallel
COPY . .
RUN dotnet publish -c release -o /app
# --no-restore

# Serve Stage
FROM mcr.microsoft.com/dotnet/aspnet:6.0-alpine
WORKDIR /app
EXPOSE 80
EXPOSE 443
COPY --from=build /app .
ENTRYPOINT ["dotnet", "Recipes.API.dll"]
