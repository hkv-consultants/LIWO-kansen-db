# Loggboek verschillen kansendatabase

## 2026-03-13 15:40

"huidige versie: kansendatabase_huidige.gpkg vs  nieuwe verseie: kansendatabase_nieuw.gpkg

### Check columns and dtypes

[primair_kansen] Columns are different

alleen nieuw: {'test col'}

### Check new rows

[primair_kansen] Verschillende indices:

Nieuwe rijen: {721}

TRAJECT_ID                                                #35-31
TRAJECT_DL                                                036013
DUIDING          Zeer kleine kans: 1/3.000 tot 1/30.000 per jaar
klasse                                                       4.0
KANS                                                       562.0
NORMOG_2050                                                 3000
test col                                                     NaN
geometry       MULTILINESTRING ((134268.03521876037 412893.10...
Name: 721, dtype: object

### Check row differences

[primair_kansen] 1 gewijzigde rijen; kolommen: ['DUIDING', 'KANS', 'NORMOG_2050', 'geometry']

DUIDING_huidig                  Kleine kans: 1/300 tot 1/3.000 per jaar
KANS_huidig                                                       719.0
NORMOG_2050_huidig                                                  300
geometry_huidig       MULTILINESTRING ((109372.49439999834 414781.54...
DUIDING_nieuw                 Kleine kans: 1/3000 tot 1/30.000 per jaar
KANS_nieuw                                                       3210.0
NORMOG_2050_nieuw                                                  3000
geometry_nieuw        MULTILINESTRING ((109372.49439999834 414781.54...
Name: 415, dtype: object

### Check bressen
