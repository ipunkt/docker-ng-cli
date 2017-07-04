# docker-ng-cli

[![](https://images.microbadger.com/badges/image/ipunktbs/docker-ng-cli.svg)](https://microbadger.com/images/ipunktbs/docker-ng-cli "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/ipunktbs/docker-ng-cli.svg)](https://microbadger.com/images/ipunktbs/docker-ng-cli "Get your own version badge on microbadger.com")

## Usage

Running ng console
```bash
$> docker run -u $(id -u) --rm -v "$PWD":/app ipunktbs/docker-ng-cli ng
```

Create new app
```bash
$> docker run -u $(id -u) --rm -v "$PWD":/app ipunktbs/docker-ng-cli ng new MyApp
```

Build app
```bash
$> docker run -u $(id -u) --rm -v "$PWD":/app ipunktbs/docker-ng-cli ng build
```

Serving ng app
```bash
$> docker run -u $(id -u) --rm -p 4200:4200 -v "$PWD":/app ipunktbs/docker-ng-cli ng serve -host 0.0.0.0
```

### Alias

Add following alias to your `~.bash_aliases` file:
```bash
WAI='$PWD'
alias ng="docker run -u $(id -u) --rm -p 4200:4200 -v "$WAI":/app ipunktbs/docker-ng-cli:latest ng"
```

So you can use
```bash
$> ng
```

## Development

### Build container

```bash
$> docker build -t ipunktbs/docker-ng-cli .
```
Or with different ng cli version

```bash
$> docker build --build-arg NG_CLI_VERSION=v1.0.1 -t ipunktbs/docker-ng-cli .
```
