THE MAINTENANCE MINDER — free from "Build It With AI" (EP26)
=============================================================

WHAT THIS IS
A single-file service board for vehicles and equipment. Paste your asset
list, your service rules, and your service history (CSV from any
spreadsheet). It shows what is OVERDUE, what is DUE SOON at the rate you
are actually using each machine, what NEEDS A METER READING before it can
say anything, and what breakdowns cost you against planned service. It
runs entirely on the page: no account, no server, nothing uploaded.

FILES
  Maintenance_Minder.html ... THE TOOL. Open it in any browser. Start with
                              "Load the sample fleet".
  sample/assets.csv ......... the sample fleet (fictional — Tillbrook
  sample/schedule.csv         Landscape & Snow, all @example.com)
  sample/history.csv
  PROMPTS.txt ............... the three prompts from the episode, verbatim
  checker.py ................ the independent second opinion (Python). Run:
                              python3 checker.py assets.csv schedule.csv history.csv
  engine_v1.js .............. FIRST DRAFT from the episode — NOT THE TOOL.
  engine_v2.js .............. SECOND DRAFT from the episode — NOT THE TOOL.
                              Both kept so you can see the wrong builds.

HOW TO USE YOUR OWN DATA
Export three sheets as CSV with these headers:
  Assets:   Asset, Name, Unit, Current Meter, Meter Date, In Service, Meter At Start
            (Unit is miles, hours, or none)
  Rules:    Asset, Task, Every Days, Every Meter   (either or both; both =
            whichever comes first)
  History:  Date, Asset, Task, Meter, Cost, Notes  (Meter optional — a
            service logged without a reading still counts)
Type the "as of" date — the board never reads your computer's clock.

WHAT IT WILL NOT DO
It does not connect to your truck, your telematics, or your calendar. It
does not know about recalls or warranties. It is not a mechanic. It sorts
the records you already keep and refuses to guess about the ones it cannot
read. If its own audit fails, it says DO NOT TRUST THIS SERVICE BOARD and means it.

Sample data is fictional. Verified suite results for this exact build:
209 paired runs vs the independent checker, 59,914 fields, 0 disagreements;
34/34 functional checks; 4/4 settings sweep.
