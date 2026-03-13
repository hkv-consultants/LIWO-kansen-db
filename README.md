# LIWO Kansen database

Kansen database (geopackage) om de kansen te beheren.

## Afspraken

- Er komt een geopackage waar zowel data als geometrie in wordt opgeslagen.
- Dit zijn 4 lagen in één geopackage.Deze bestaan uit:
    > - Primaire keringen
    > - Doorbraak locaties primair
    > - Nie primaire keringen
    > - Doorbraak locatie niet primair
- De initële versie (2026) van dit kansen database wordt eenmalig gegenereed met de liwo data, deze is te vinden in `/init_vanuit_liwo`. Hierna wordt dit kansen database altijd de bron.
- In GitHub is versiebeheer aanwezig. Ook wordt een script aangemaakt om versie beheer makkelijker te maken: deze zet de veranderingen om in leesbare bestanden.  
- De kansen database in de hoofdmap altijd actueel.

### aanpassing verwerken kansen database

- Download de huidige versie van de kansen database.
- Voer aanpassingen door.
- Plaats de aangepaste database in `data/input_aanpassingen_db` met naam `kansendatabase_nieuw.gpkg`. Zet de huidige versie uit de hoofd map hier in:`kansendatabase_huidige.gpkg`.
- Run het script in `scripts/verschillen_kansendb_LIWO.py` of interactieve notebook `scripts/verschillen_kansendb_LIWO.ipynb`
    > - Hiervoor is een `uv` environment beschikbaar, gebruik `uv sync --locked` om deze te instaleren.
    > - De belangrijkste dependency is `geopandas`, een python environment waar dit in zit is ook voldoende.
- Het script genereert een logbook, zorgt dat dit mee gaat in versie beheer.
- Laat ook de geojsons die door het script worden gegenereerd staan. Deze helpen in de herleidbaarheid van keuzes.
- zorgt dat `uv run pre-commit` heeft gerund.
