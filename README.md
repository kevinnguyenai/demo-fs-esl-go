# Golang Microservices Boilerplate

[![issues](https://img.shields.io/github/issues/kevinnguyenai/demo-fs-esl-go)](https://github.com/kevinnguyenai/demo-fs-esl-go/tree/master/.github/ISSUE_TEMPLATE)
[![forks](https://img.shields.io/github/forks/kevinnguyenai/demo-fs-esl-go)](https://github.com/kevinnguyenai/demo-fs-esl-go/network/members)
[![stars](https://img.shields.io/github/stars/kevinnguyenai/demo-fs-esl-go)](https://github.com/kevinnguyenai/demo-fs-esl-go/stargazers)
[![license](https://img.shields.io/github/license/kevinnguyenai/demo-fs-esl-go)](https://github.com/kevinnguyenai/demo-fs-esl-go/tree/master/LICENSE)
[![CodeFactor](https://www.codefactor.io/repository/github/kevinnguyenai/demo-fs-esl-go/badge)](https://www.codefactor.io/repository/github/kevinnguyenai/demo-fs-esl-go)

Example structure to start a microservices project with golang. Using a MySQL databaseSQL.

## Manual Installation

If you would still prefer to do the installation manually, follow these steps:

Clone the repo:

```bash
git clone https://github.com/gbrayhan/microservices-go
```

If you need, configure the environment variables in file config.json, if you use docker-compose leave the variables set
in the file config.json.example

```bash 
cp config.json.example config.json
```

**TL;DR command list**

    git clone https://github.com/gbrayhan/microservices-go
    cd microservices-go
    cp config.json.example config.json
    docker-compose up  --build  -d


## Table of Contents

- [Golang Microservices Boilerplate](#golang-microservices-boilerplate)
  - [Manual Installation](#manual-installation)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Commands](#commands)
    - [Build and run image of docker](#build-and-run-image-of-docker)
    - [Swagger Implementation](#swagger-implementation)
    - [Unit test command](#unit-test-command)
    - [Lint inspection of go](#lint-inspection-of-go)

## Features

- **Golang v1.14**: Stable version of go
- **Framework**: A stable version of [gin-go](https://github.com/gin-gonic/gin)
- **SQL databaseSQL**: [MariaDB](https://mariadb.org/) using internal sql package of
  go [sql](https://golang.org/pkg/databaseSQL/sql/)
- **Testing**: unit and integration tests using package of go [testing](https://golang.org/pkg/testing/)
- **API documentation**: with [swaggo](https://github.com/swaggo/swag) a go implementation
  of [swagger](https://swagger.io/)
- **Dependency management**: with [go modules](https://golang.org/ref/mod)
- **Environment variables**: using [viper](https://github.com/spf13/viper)
- **Docker support**
- **Code quality**: with [CodeFactor](https://www.codefactor.io/)
- **Linting**: with [ESLint](https://eslint.org)

## Commands

### Build and run image of docker

```bash
docker-compose up  --build  -d
```

### Swagger Implementation

```bash
swag init -g routes/ApplicationV1.go
```
To visualize the swagger documentation on local use 

http://localhost:8080/v1/swagger/index.html


### Unit test command

```bash
# run recursive test
go test  ./test/unitgo/...
# clean go test results in cache
go clean -testcache
```

### Lint inspection of go

```bash
golangci-lint run ./...
```



