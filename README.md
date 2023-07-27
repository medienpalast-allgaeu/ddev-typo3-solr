
# Medienpalast ddev-solr Service <!-- omit in toc -->

## Einrichtung

1. Installieren: `ddev get medienpalast-allgaeu/ddev-typo3-solr`
2. Die Datei `.ddev/config.yaml` um diese Zeilen ergänzen:
   ```shell
   hooks:
     pre-start:
       - exec-host: 'if [ ! -d ".ddev/solr/data" ]; then mkdir .ddev/solr/data ; chmod 777 .ddev/solr/data ; fi'
   ```
3. Solr Konfiguration entweder vom Server oder aus der Extension Solr in das Verzeichnis `.ddev/solr/` kopieren
4. Berechtigungen für alle User setzten: `chmod -R a+rw .ddev/solr/`
5. ddev neu starten: `ddev restart`
