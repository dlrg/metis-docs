Vor dem Starten von **metis**, solltest du einige Systemanforderungen beachten:

!!! warning
    When running metis on a Debian 8 (Jessie) box, you should [switch to kernel 4.9 from Jessie backports](https://packages.debian.org/jessie-backports/linux-image-amd64) to avoid a bug when running Docker containers with *healthchecks*! For more details read: [github.com/docker/docker/issues/30402](https://github.com/docker/docker/issues/30402)

!!! info
    - metis: benötigt [einige Ports](#default-ports) um Verbindungen zu den einzelnen Docker Container herstellen zu können.
    - Stelle sicher, dass deine Firewall diese nicht blockiert.

## Minimum System Resources

Damit metis ideal läuft sollten folgende Ressourcen vorhanden sein:

| Resource                | metis                          |
| ----------------------- | -------------------------------------------- |
| CPU                     | 1 GHz                                        |
| RAM                     | 3 GiB + Swap (besser: 4 GiB und mehr + Swap) |
| Disk                    | 15 GiB                      |
| System Type             | x86_64                                       |


## Firewall & Ports

Stelle bitte sicher, dass die folgenden Ports für offen sind und für metis zur Verfügung stehen:

```
# netstat -tulpn | grep -E -w '3000|9000|80'
```

### Default Ports

Wenn Du eine Firewall hast stelle sicher das die folgenden Ports für Metis zur Verfügung stehen:

| Service             | Protocol | Port   | Container       |
| --------------------|:--------:|:-------|:----------------|
| Metis API           | TCP      | 3000   | metis_api       |
| Metis Client        | TCP      | 80     | metis_client    |