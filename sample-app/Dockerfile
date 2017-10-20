FROM microsoft/dotnet:latest
COPY ./src /app
WORKDIR /app
RUN ["mkdir", "wwwroot/license", "-p"]
RUN echo "Tum haklari saklidir, yersen :)" >> wwwroot/license/license.txt
RUN ["dotnet", "restore"]
RUN ["dotnet", "build", "--configuration", "Release"]
ENV ASPNETCORE_URLS=http://*:1905
EXPOSE 1905
ENTRYPOINT [ "dotnet", "run"]