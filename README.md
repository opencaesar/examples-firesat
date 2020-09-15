# FireSat Example

[![Gitpod](https://img.shields.io/badge/gitpod-open-blue?logo=gitpod)](https://gitpod.io/#https://github.com/opencaesar/firesat-example) 
[![Build Status](https://travis-ci.org/opencaesar/firesat-example.svg?branch=master)](https://travis-ci.org/opencaesar/firesat-example)
[ ![Download](https://api.bintray.com/packages/opencaesar/firesat-example/firesat-example/images/download.svg) ](https://bintray.com/opencaesar/firesat-example/firesat-example/_latestVersion)

This is a description of a FireSat project expressed in [OML](https://github.com/opencaesar/oml)

## Clone
```
  git clone https://github.com/opencaesar/firesat-example.git
  cd firesat-example
```

## Build
Run reasoner, generate docs, and archive sources
```
./gradlew build
```

## Download Dependencies
```
./gradlew omldependencies
```

## Run Reasoner
```
./gradlew owlreason
```

## Load to Fuseki
```
./gradlew owlload
```
Pre-req: A Fuseki server with a firesat dataset must be running at http://localhost:3030/firesat  

## Run SPARQL Queries
```
./gradlew owlquery
```
Pre-req: A Fuseki server with a firesat dataset must be running at http://localhost:3030/firesat  

## Run SHACL Rules
```
./gradlew owlshacl
```
Pre-req: A Fuseki server with a firesat dataset must be running at http://localhost:3030/firesat  

## Generate Docs
You must first have Bikeshed installed from [here](https://tabatkins.github.io/bikeshed/#installing)
```
./gradlew bikeshed2html
```

## Publish to Maven Local
```
./gradlew publishToMavenLocal
```

## Run Fuseki Locally
Download the [Apache Jena Fuseki](https://jena.apache.org/download/index.cgi) distribution and run the server locally using the project's `.fuseki.ttl` configuration.

MacOS/Linux:
```
cd fuseki-distribution-folder
./fuseki-server --config=<path to this project>/.fuseki.ttl
```
Windows:
```
cd fuseki-distribution-folder
fuseki-server.bat --config=<path to this project>\.fuseki.ttl
```
The server should now be running and has a `firesat` dataset accessible at http://localhost:3030/fuseki
