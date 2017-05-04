# docker-ng-cli

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

## Development

### Build container

```bash
$> docker build -t ipunktbs/docker-ng-cli .
```
Or with different ng cli version

```bash
$> docker build --build-arg NG_CLI_VERSION=v1.0.1 -t ipunktbs/docker-ng-cli .
```
