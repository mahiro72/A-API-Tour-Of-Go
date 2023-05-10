FROM golang:1.19 AS develop

WORKDIR /go/src/github.com/mahiro72/API-Tour-Of-Go

COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY . .

RUN go install github.com/cosmtrek/air@latest

COPY docker/develop/api/.air.toml /air/.air.toml

CMD ["air", "-c", "/air/.air.toml"]
