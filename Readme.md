# Go App 

## Commands in the Development
```bash 
go mod init app 
go mod tidy
go run main.go
```

## best syntax for docker file and more effectient 
### that is help the container to be  more stable and don't need to rebuild it after each small edit in the other files that is don't need to rebuild the project 

```bash
FROM golang:alpine

WORKDIR /app 

ADD go.sum .
ADD go.mod .

RUN go mod tidy

COPY . .

EXPOSE 3000

CMD [ "go", "run", "main.go" ]
```
# CI => github action 
### create the 
