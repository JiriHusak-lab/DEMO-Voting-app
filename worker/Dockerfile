FROM dotnet

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 


USER 1001

CMD dotnet src/Worker/Worker.dll
