
#instruction
https://www.youtube.com/watch?v=ds2bud0ZYTY

#version 1 - use dockerfile manually
-build the image 
docker build -t nn1:2 . 
- run the image
docker run -p 5001:8080 -e ASPNETCORE_URLS=http://+:8080 --name mynet8 nn1:2

#version 2 - use docker-compose
run command: docker-compose up mynet8
to shutdown: docker-compose down

#Note
Follow this to delete ~/.vsdbg on your macos to fix issue with debug
https://stackoverflow.com/questions/72288604/debugging-with-docker-net-core-attach-not-working-anymore
