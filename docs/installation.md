!!! warning
    Lies dir vorher die ["Systemanforderungen"](https://#) durch!


Du benötigst Docker und Docker Compose

**1\.** Installier dir [Docker](https://docs.docker.com/install/) und [Docker Compose](https://docs.docker.com/compose/install/) und 

- Docker
```
curl -sSL https://get.docker.com/ | CHANNEL=stable sh
# After the installation process is finished, you may need to enable the service and make sure it is started (e.g. CentOS 7)
systemctl enable docker.service
systemctl start docker.service
```

- Docker-Compose
```
curl -L https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m) > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

**2\.** Node.js <br/> Als nächstes müssen wir noch [Node.js Version Manager](https://github.com/tj/n) installieren. Dazu benutzen wir einen Version Manager "n" von [tj/n](https://github.com/tj/n)

- für MacOS mit Homebrew
```
brew install n
```

- für Linux und macOS
```
curl -L https://git.io/n-install | bash
```


**3\.** Jetzt kannst du den development branch von metis clonen.
```
git clone https://github.com/dlrg/metis.git
cd metis
```

**4\.** Das Projekt startest du im enstprechenden Verzeichnis mit
```
npm start
```

Done!
