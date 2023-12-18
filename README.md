# rt37-Checker Docker

rt37-checker ist ein Docker-Container, mit dem man jeden Tag überprüfen kann, ob seine Gewinnzahl gewonnen hat oder nicht.

## Usage
### Docker Command:
```bash
docker run --restart unless-stopped --name rt37-checker -e gewinnZahl=123 -e winner=Mustergewinner -e GOTIFY_SERVER=http://gotify.send -e GOTIFY_APP_TOKEN=abcdefg ghcr.io/nollknolle/rt37-checker
```

### Docker-Compose:
```yml
version: "3"
services:
    rt37-checker:
        restart: unless-stopped
        container_name: rt37-checker
        environment:
            - gewinnZahl=123
            - winner=Mustergewinner
            - GOTIFY_SERVER=http://gotify.send # optional
            - GOTIFY_APP_TOKEN=abcdefg # optional
        image: ghcr.io/nollknolle/rt37-checker
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.
