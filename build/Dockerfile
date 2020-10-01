FROM golang

COPY . /go/src/app

WORKDIR /go/src/app

# RUN go get ./

COPY go.mod .

# COPY go.sum .

RUN go mod download

COPY . .

WORKDIR /go/src/app/cmd/apirest

RUN go build -o apirest

CMD ./apirest

EXPOSE 5050