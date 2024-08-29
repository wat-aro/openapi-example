# OpenAPI example

https://github.com/OpenAPITools/openapi-generator/blob/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml

を元に APIドキュメント、APIクライアント、stubサーバを生成する

## APIドキュメント

``` shell
docker compose up
```

### Redoc

http://localhost:4444

### swagger-ui

http://localhost:4445

## Client

### Go

``` shell
docker run --rm -v $PWD:/local openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g go \
    -o /local/client/go
```

### Ruby

``` shell
docker run --rm -v $PWD:/local openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g ruby \
    -o /local/client/ruby
```

### TypeScript

``` shell
docker run --rm -v $PWD:/local openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g typescript-axios \
    -o /local/client/typescript
```


## Server

### Sinatra

``` shell
docker run --rm -v $PWD:/local openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g ruby-sinatra \
    -o /local/server/ruby
```
