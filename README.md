# Middleman im Docker-Container

Image erstellen: `docker build -t nobodyfrm/middleman .`

Start eines Containers mit dem Image: `docker run -p LOCALPORT:4567 -it --name CONTAINERNAME -v /middleman nobodyfrm/middleman  /bin/bash`

Ersetze LOCALPORT mit dem Port, unter welchem der Container auf dem Host zugänglich sein soll. CONTAINERNAME ist ein frei wählbarer Name, um später auf diesen besser zugreifen zu können. Wenn man den Parameter weglässt, wird automatisch einer zugewiesen.

Beim Start des Containers wird automatisch der Middleman-Server gestartet. Um Änderungen vorzunehmen oder ein Build zu erstellen, kann man in einem 2. Terminalfester mit `docker exec -it CONTAINERNAME bash` auf den Container zugreifen.

Alternativ kann man vor dem Erstellen des Image in der Dockerfile die letze Zeile entfernen (ENTRYPOINT). Dadurch wird der Server nicht automatisch gestartet.
