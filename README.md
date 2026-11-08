# Hearthbound Guilds — TTS asset upload pack

The Tabletop Simulator save (`TS_Save_7001.json`) loads every image from a
public GitHub repo. The connector cannot push binary files, so this one
upload is done by hand — it takes about two minutes.

## Step 1 — create the repo (once)

On github.com, create a **public** repository named exactly:

    hearthbound-guilds

(owner: NommerTay — the save's URLs assume `NommerTay/hearthbound-guilds`,
branch `main`.)

> Note: Muse already tried to create it through the GitHub app and got
> "403 Resource not accessible by integration" — the app can't create
> repos, so this click is yours.

## Step 2 — upload these files to the repo ROOT

Drag every file in this folder (except this README) into the repo root —
names must land byte-for-byte as listed. Each becomes:

    https://raw.githubusercontent.com/NommerTay/hearthbound-guilds/main/<filename>

| File | Used for |
|---|---|
| town-board.jpg | Town board (24×16) |
| player-board.jpg | Player tavern boards ×6 |
| quest-sheet-1.jpg | Quest cards 1–70 (10×7 sheet) |
| quest-sheet-2.jpg | Quest cards 71–72 |
| quest-back.jpg | Quest card back |
| patron-sheet-1.jpg | Patron cards 1–70 |
| patron-sheet-2.jpg | Patron cards 71–72 |
| patron-back.jpg | Patron card back |
| recipe-sheet-1.jpg | Recipe/Brew cards 1–48 |
| recipe-back.jpg | Recipe card back |
| hire-sheet-1.jpg | Hire cards 1–48 |
| hire-back.jpg | Hire card back |
| event-sheet-1.jpg | Season Event cards 1–16 |
| rumor-sheet-1.jpg | Held Rumor cards 1–32 |
| rumor-back.jpg | Rumor/Event card back |
| room-bards-corner-stage.jpg | Room tile |
| room-brewery-loft.jpg | Room tile |
| room-cellar.jpg | Room tile |
| room-guest-baths.jpg | Room tile |
| room-guest-room.jpg | Room tile |
| room-landlords-office.jpg | Room tile |
| room-larger-kitchen.jpg | Room tile |
| room-physic-corner.jpg | Room tile |
| room-private-booths.jpg | Room tile |
| room-rumor-nook.jpg | Room tile |
| room-spice-rack-wall.jpg | Room tile |
| room-storehouse.jpg | Room tile |
| room-training-yard.jpg | Room tile |
| room-trophy-wall.jpg | Room tile |
| quest-die-chart.jpg | Quest Die reference chart tile |
| spot-cover.jpg | CLOSED spot-cover tiles |
| token-gold.jpg | Gold counter chips |
| token-provisions.jpg | Provisions counter chips |
| token-ale.jpg | Ale counter chips |
| token-materials.jpg | Materials counter chips |
| token-renown.jpg | Renown counter chips, worker discs, plaque |
| box-cover.jpg | Not referenced by the save — box art for the Workshop page / thumbnail |

## Step 3 — install the save

Copy `TS_Save_7001.json` (in `../`, the build folder) into your TTS saves
folder (`Documents/My Games/Tabletop Simulator/Saves/`) and load it in-game.

**First-load checklist:** the town and boards should show the painted art,
decks should show their card backs, and the chat should print
"Hearthbound Guilds loaded…". Then click **4P** on the SETUP PLAQUE
(west side of the table) — displays should fill, two town spots get CLOSED
covers, counters should read 6/4/1/2/0, and a Season Event should be
announced. If anything errors, copy the red error text from chat — it names
the exact object and line.
