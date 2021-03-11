FROM mcr.microsoft.com/dotnet/core/sdk:3.1
COPY . /myapp
WORKDIR /myapp

RUN dotnet restore
RUN dotnet build

EXPOSE 5000/tcp
ENV ASPNETCORE_URLS http://*:5000
ENV ASPNETCORE_ENVIRONMENT docker

ENTRYPOINT dotnet run
