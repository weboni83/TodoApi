## dotnet 7 api



### Https 인증서 추가

```bash
dotnet dev-certs https --trust
```



### Package 추가

```bash
dotnet add package Microsoft.EntityFrameworkCore.InMemory
dotnet add package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore

```



### Swagger 추가

```bash
dotnet add TodoApi.csproj package Swashbuckle.AspNetCore -v 6.5.0
```



### 실행

```bash
dotnet run --urls https://localhost:5201
```





### Dockerfile 

```dockerfile
FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
ARG ASPNETCORE_ENVIRONMENT=Production
WORKDIR /src
COPY ["TodoApi.csproj", "."]
RUN dotnet restore "./TodoApi.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "TodoApi.csproj" -c Release -o /app/build /p:Environment=$ASPNETCORE_ENVIRONMENT

FROM build AS publish
RUN dotnet publish "TodoApi.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "TodoApi.dll"]
```



#### 빌드

```bash
docker build -t todoapi:v1 --build-arg ASPNETCORE_ENVIRONMENT=Development .
```

> ASPNETCORE_ENVIRONMENT  지정안해도 상관없다. 개발 DB와 운영 DB를 분리하거나 port 를 분리할 때 사용하자

#### 도커 실행

```bash
docker run --name dot7-todoapi -p 51234:80 --env ASPNETCORE_ENVIRONMENT=Development todoapi:v1
```

> swagger를 확인하고자 하면 `--env ASPNETCORE_ENVIRONMENT=Development` 를 지정한다. 지정하지 않으면 swagger 확인 불가



### docker-compose.yml

```bash
docker-compose up -d
```

