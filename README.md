# The Athletic Build — v1

Offline-first workout logger for iPhone Safari.

## Deploy via GitHub Pages
1. Maak een **public** GitHub-repository, bijvoorbeeld `athletic-build`.
2. Upload **alle bestanden uit deze map** naar de root van de repository (niet de map zelf).
3. Ga naar **Settings → Pages → Build and deployment → Deploy from a branch**; selecteer `main` en `/ (root)`.
4. Open de Pages-URL in Safari op je iPhone, wacht tot de app geladen is en kies **Deel → Zet op beginscherm**.
5. Open de app vanaf het beginscherm. Test offline nadat je de app een keer online hebt geopend.

## Privacy en backups
Trainingsdata worden lokaal in `localStorage` bewaard. GitHub ontvangt geen workoutdata. Maak regelmatig een volledige JSON-backup via REVIEW en bewaar deze in Bestanden/iCloud Drive. Als je de app verwijdert, browserdata wist of van apparaat wisselt, kan de lokale data verdwijnen.

## Belangrijke beperkingen
- V1 is een prototype; test eerst met een paar dummysets.
- Een PWA heeft HTTPS nodig voor offline service-worker caching. `file://` is niet voldoende.
- Gewicht van assisted pull-ups is **assistance**, dus minder kg assist is zwaarder; automatische gewichtsadviezen worden hier nog niet voor gegeven.
- Gewicht van dumbbells is per hand; bij machines is het de getoonde machinebelasting. De app toont nog geen eenheden per oefening.
- Wijzigingen aan `program.json` beïnvloeden nieuwe sessies, niet reeds opgeslagen sessies.
- PWA-updates kunnen na opnieuw openen zichtbaar worden.

## v1.1
Via Progress → Recent Sessions kun je voltooide trainingen openen, sets wijzigen of een training verwijderen. Bij verwijderen wordt de volgende training bepaald door de laatste overgebleven sessie. Maak vooraf een backup.

## V1.2 — Workout Editor
Open TRAIN → EDIT PROGRAM om oefeningen te hernoemen, vervangen, toevoegen, verwijderen of te verplaatsen en sets/reps/rust/gewichten aan te passen. Wijzigingen worden lokaal bewaard en meegenomen in de volledige backup. De standaard Workout B bevat Seated Leg Curl in plaats van RDL. Historische sessies blijven ongewijzigd. Een reeds gestarte training verandert niet tijdens programma-aanpassingen.


## V1.3 — iOS light redesign
Visuele update: iOS-achtige lichte interface, subtiele teal-accenten, compactere workoutkaarten en native-style tabbar. Bestaande localStorage key en backupformaat blijven gelijk. Maak een backup voordat je update.

## V1.4 — iOS White
Pure white UI, neutral iOS grays, subtle system-blue accents, reduced shadows. Functionality and data schema unchanged. Before uploading, export a full backup.
