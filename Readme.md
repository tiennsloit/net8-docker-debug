# Instructions
This project is a Hello World .NET 8 project that can be debugged with Docker using VS Code.

For a detailed video tutorial, visit: [YouTube Video](https://www.youtube.com/watch?v=ds2bud0ZYTY)

## Version 1 - Using Dockerfile Manually
### Build the Image
From root folder of the project run this command:
```sh
docker build -t tiennsloit/net8:1.0.2 .
```
### Run the Image
From root folder of the project run this command:
```sh
docker run -p 5001:8080 -e ASPNETCORE_URLS=http://+:8080 --name mynet8 tiennsloit/net8:1.0.2
```
## Version 2 - Using Docker Compose
### Start the Service
From root folder of the project run this command:
```sh
docker-compose up mynet8
```
### Shutdown the Service
From root folder of the project run this command:
```sh
docker-compose down
```

## Attached and debug
### Attached
From Debug tab
Launch the process with name: ".NET Core Docker Attach", then choose the item with name HelloWorldRazor form the dropdown menu
### Put the debug point and test with the project url: http://localhost:5001

### Note
If you encounter issues with debugging, follow the instructions in this Stack Overflow post to delete ~/.vsdbg on your macOS.
https://stackoverflow.com/questions/72288604/debugging-with-docker-net-core-attach-not-working-anymore