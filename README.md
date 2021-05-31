## Doctolib COVID

This script sends email alerts (using Google SMTP server) when vaccination appointments are available on Doctolib.

My modification lets you select the desired vaccine (from the list in vaccines.txt) via a prompt, works with german 
Doctolib-Servers and constantly retries to find appointments.  
The list of centers still has to be created by hand - the example shows centers that accept first-time visitors for 
vaccination in Hamburg.

## Prerequisites
 
- Python 3

## Download dependencies

`$ pip install -r requirements.txt`

## Execution

- Set the vaccination centers close to your location in [centers.txt](../master/centers.txt)

- Set environment variables
  - DISABLE_EMAIL: set to true to disable email alerts
  - SENDER_EMAIL: the sender email address
  - SENDER_PASSWORD: the associated password
  - RECEIVER_EMAIL : the receiver email address

- Execute command
`$ python doctolib-covid.py`

- Output example
```bash
0. biontech
1. janssen
2. astrazeneca
3. moderna
4. scheissemiterdbeeren
5. alle Impfstoffe
Bitte wählen: (0, 1, 2, 3, 4, 5): 0
0 Termin(e) verfügbar bei Dr. med. Tom Straessle und Frau Dr. Ulrike Niehaus Fachärzte für Allgemeinmedizin, Großneumarkt 20 Hamburg-Mitte, 20459 Hamburg
Hausarztpraxis St. Pauli: bietet keine entsprechenden Impfungen an
0 Termin(e) verfügbar bei Schmerztherapie am Rothenbaum, Heimhuder Straße 38, 20148 Hamburg-Rotherbaum
0 Termin(e) verfügbar bei Anästhesiepraxis Walsrode / Augenpartner Walsrode , Lange Straße 55, 29664 Walsrode
Herr Dr. med. Peter Kühnelt: bietet keine entsprechenden Impfungen an
Hausarzt Forum Winterhude: bietet keine entsprechenden Impfungen an
Nächster Versuch in 5 Minuten

```