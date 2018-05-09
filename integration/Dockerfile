# Build stage
FROM microsoft/dotnet:2.1-sdk AS build-env

WORKDIR /integration

# restore
COPY integration.csproj .
RUN dotnet restore

# copy src
COPY . .
ENV TEAMCITY_PROJECT_NAME=fake
ENTRYPOINT ["dotnet", "test"]