# middleman-docker

Beim Start des Containers wird automatisch der Middleman-Server gestartet. Um Änderungen vorzunehmen oder ein Build zu erstellen, kann man in einem 2. Terminalfester mit `docker exec -it CONTAINERNAME bash` auf den Container zugreifen.

Alternativ kann man vor dem Erstellen des Image in der Dockerfile die letze Zeile entfernen (ENTRYPOINT). Dadurch wird der Server nicht automatisch gestartet.
