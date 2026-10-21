# Infomobility GTFS Live

Demo di monitoraggio infomobility in stile ITS: fermate reali GTFS, linee animate e
partenze live Viaggiatreno sulla tratta Fano–Ancona.

## Contenuto

| File | Ruolo |
|---|---|
| `gtfs-demo.html` | mappa/animazione delle corse |
| `query-terminal.html` | terminale per interrogare le partenze |
| `mobility-report.html` | report tecnico del progetto |
| `js/gtfs.js`, `js/gtfs-live.js` | rendering fermate e corse |
| `js/query.js` | terminale |
| `api/gtfs.json` | dataset fermate/linee demo |
| `tools/gtfs-to-json.py` | conversione dati GTFS in JSON |
| `tools/viaggiatreno-poll.py` | poll Viaggiatreno → `api/realtime.json` |

## Nota sui dati

Il feed GTFS contiene solo 2 trip: le posizioni animate sono simulate e documentate.
Le partenze reali arrivano da Viaggiatreno e vengono salvate in `api/realtime.json`,
generato dal poller e non versionato.

## Anteprima

```bash
python3 -m http.server 8080
# http://localhost:8080/gtfs-demo.html
```
