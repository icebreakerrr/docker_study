FROM golang:alpine AS builder 

WORKDIR /go/src/app  
COPY main.go .

#초기화작업
RUN go mod init  
RUN go build -o webserver .

CMD ["./webserver"]

# ---- stage 2------
FROM scratch

WORKDIR /app
COPY --from=builder /go/src/app /app/

# EXAMPLE
RUN apt update && apt install -y nginx pkg2
# 위와 같이 하면 하나의 레이어로 뭉칠수 있음. 관리 용이
RUN apt install -y nginx
RUN apt install -y pkg2

CMD ["./webserver"]
