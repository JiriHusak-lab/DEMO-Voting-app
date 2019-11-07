FROM microsoft/dotnet:2.0.0-sdk

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

CMD dotnet src/Worker/Worker.dll
#CMD exec /bin/sh -c "trap : TERM INT; (while true; do sleep 1000; done) & wait" 
