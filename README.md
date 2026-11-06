# Richtprijs calculator – Energie De Kempen

Eén statische pagina (`index.html`) waarin een prospect kiest tussen **zonnepanelen**, een **thuisbatterij** of **airco**, een paar vragen beantwoordt en meteen een richtprijs krijgt. Er worden geen contactgegevens gevraagd en er gaat niets naar een server.

## Lokaal bekijken

```
python3 -m http.server 8765
```

Open daarna http://localhost:8765. Je kunt `index.html` ook gewoon dubbelklikken.

## Prijzen aanpassen

Bovenaan het `<script>`-blok in `index.html`:

- `SOLAR_PRICES` – prijsband per totaal vermogen (Wp)
- `BATTERY_PRICES` – prijs per batterijcapaciteit (5 / 10 / 15 kWh)
- `AIRCO_PRICES` – single-split per ruimte, multi-split buitenunit + prijs per binnenunit
- `AIRCO_W_PER_M2` – benodigd vermogen per m² volgens isolatie
- `PANEL_WP`, `PANEL_M2`, `KWH_PER_KWP`, `EUR_PER_KWH` – rekenaannames

## Inbouwen op de website

Host `index.html` en plaats hem met een iframe op de pagina, bv.:

```html
<iframe src="https://JOUW-DOMEIN/calculator/" style="width:100%;height:900px;border:0"></iframe>
```

Logo en lettertypes worden van energiedekempen.be geladen.
