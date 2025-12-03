# set environment

```
set GOARCH=amd64
go env -w GOARCH=amd64
set GOOS=linux # linux windows darwin
go env -w GOOS=linux # linux windows darwin
set CGO_ENABLED=0
go env -w CGO_ENABLED=0

set GOARCH=amd64
go env -w GOARCH=amd64
set GOOS=windows # linux windows darwin
go env -w GOOS=windows # linux windows darwin
set CGO_ENABLED=0
go env -w CGO_ENABLED=0

```

# build ws

```
go build -ldflags "-X rehabilitation_circle_api/config.Assets=/home/panel -X rehabilitation_circle_api/config.MqttTcp=1885 -X rehabilitation_circle_api/config.MqttWebsocket=1884"
``` 

# build wss

```
go build -ldflags "-X rehabilitation_circle_api/config.Assets=/home/panel -X rehabilitation_circle_api/config.MqttTcp=1885 -X rehabilitation_circle_api/config.MqttWebsocket=1884 -X rehabilitation_circle_api/config.MqttWssTcp=1887 -X rehabilitation_circle_api/config.MqttWssWebsocket=1886"
``` 

# run ws

```
go run main.go "./loggerData" 1885 1884
```

# run wss

```
go run main.go "./loggerData" 1885 1884 1887 1886
```

# 新工程

```
go mod init "rehabilitation_circle_api"
```
