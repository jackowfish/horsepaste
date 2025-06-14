# horsepaste

[![GoDoc](https://godoc.org/github.com/jbowens/horsepaste?status.svg)](https://godoc.org/github.com/jbowens/horsepaste)

Horsepaste is a word-guessing game. Generated boards are shareable and sync. The board can be viewed either as a clue giver or a word guesser.

A hosted version of the app is available at [www.horsepaste.com](https://www.horsepaste.com).

![Clue giver view of board](https://raw.githubusercontent.com/jbowens/horsepaste/master/screenshot.png)

## Building

The app requires a [Go](https://golang.org/) toolchain, node.js and [parcel](https://parceljs.org/) to build. Once you have those setup, build the application Go binary with:

```
go install github.com/jbowens/horsepaste/cmd/horsepaste
```

Then from the frontend directory, install the node modules:

```
npm install
```

and start the app (listens to changes)

```
npm start
```

or build the app

```
npm run build
```

### Docker

Alternatively, the repository includes a Dockerfile for building a docker image of this app.

```
docker build . -t horsepaste:latest
```

The following command will launch the docker image:

```
docker run --name horsepaste_server --rm -p 9091:9091 -d horsepaste
```

The following command will kill the docker instance:

```
docker stop horsepaste_server
```
