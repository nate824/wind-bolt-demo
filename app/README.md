# Stud Tracker (v1)

Per-tower tracker for blade stud retrofit work, built from the 2026-11-14 call with Patrick.

Open `index.html` in a browser. Data is stored in that browser only (localStorage).
Hosted over https it also installs as an offline app (`sw.js`, `manifest.webmanifest`).

## What it does
- Towers: add a range (Tower 1 to 40), rename, delete; stud length 610 or 655 per tower.
- Three axes per tower (A1, A2, A3), 92 studs each, one row, numbered clockwise.
- Diagram follows the procedure picture: retro zone red, green zone, stud 1 found by
  counting 5 from the ramp plate edge.
- Per stud: broken, diameter (27/29), length, torque, note. Defaults come from the zone and tower.
- Per axis: status, notes, Add alignment (+49 extra washers to the running tally).
- Tower notes. Washer tally with an order reminder (default 1,000).
- Map: load turbine positions from a CSV (longitude, latitude), then select a dot to link it to a tower.
  Dots show tower status. Road background comes from OpenStreetMap when online.
- Share: read-only snapshot link, CSV summary, backup and restore.
- Optional edit code that locks editing in this browser.

## Assumptions to confirm with Patrick
- Lower retro zone is 23 to 43. The picture labels only 43; 23 is read off the picture and
  cross-checks: 92 - 37 retro - 6 green = 49, the alignment washer count.
- Green zone (44 to 46, 66 to 68): 29 mm and 3,000 N·m assumed. Meaning of green not stated.
- "65 mm" early in the call is taken as a slip for the 610/655 length variants.
All of these are editable under Settings.

## Not in v1
- Live sync. The read-only link is a snapshot; nothing is stored on a server.
- Tower numbers on the map are linked by hand: Dispatch has no export.
- Hub photo in the stud view.
