# Recipes

Just a an on-going project to play with during a .NET 6 course

## Runing the API
```
    $ cd Recipes.API
    $ dotnet run
```
 - Open: https://localhost:7040/swagger/index.html
 - Or: https://localhost:7040/WeatherForecast

## Using docker
```
    $ docker-compose build
    $ docker-compose up
```

Docker makes the app run as Production, so:
- https redirection is borked without configuring actual certificates (you probably want something like a nginx reverse proxy for this anyway also)
- Swagger endpoint ovbiously does not workg in production xD

