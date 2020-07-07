

```bash
#create
dotnet new webapi -o helloworld --no-https

#open
code .

#click debug icon & run
localhost:5000/weatherforcast

#run in postman

#add docker extensions for vs code
Search for extensions: docker (first)

#add docker file
toolbar/view/command pallette/
type docker:add docker files to workspace
select: ASP Net Core
linux
port: 80

in docker file (build) remove 
Workdir "/src/."

#.dockerignore
to ignores  files & directories from final image

#docker build & tag (fromroot)
#. means current location is the context of the docker build command 
docker build -t helloworld:v1 .

#verify
docker images
docker images --filter reference=helloworld

#run: rm-> remove docker container after we finishing running the container inside the image
#external: internal

docker run -it --rm -p 8080:80 helloworld:v1 

http://localhost:8080/WeatherForecast

# stop: discard container, keep image
ctrl-c
```

