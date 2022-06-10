FROM alpine:3.10 as builder
RUN apk add --no-cache gcc  libc-dev
RUN mkdir /src
WORKDIR /src
COPY app.c .
RUN gcc -static app.c -o app

# build target image
FROM scratch
COPY --from=builder /src/app /app
ENTRYPOINT ["/app"]
