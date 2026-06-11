# The Tartaros Cycle — Character Map

*Who's who, grouped by house and faction, with small family trees and relations —
so the whole cast can be seen at a glance. Diagrams are Mermaid; in VS Code use a
Markdown preview (the **Markdown Mermaid** extension from `SETUP.md` renders them).
Detail lives in `../bible/TARTAROS_CYCLE_BIBLE.md`.*

**Legend:** † = deceased · solid line = marriage or parent→child · dotted line =
other relation (service, friendship, mentorship, etc.).

---

## 1. The powers and the Homonoia

```mermaid
graph TD
  HEG["THE HEGEMONY · capital Andra Prime"]
  FED["THE FEDERATION · rival · hub Cairn"]
  HEG -. cover-story war .- FED
  HEG --> HOM["THE HOMONOIA — the conglomerate"]
  HOM --> ARCH["Xerxes · the Architect (Summum)"]
  HOM --> V["The Vendine · defense · black-gray-silver"]
  HOM --> AS["The Asclepi · medical · olive-brass"]
  HOM --> LI["The Limine · frontier · rust-bronze"]
  HOM --> NA["The Narrine · communications · oxblood-pewter"]
  SYN["THE SYNEDRION · 9 seats"]
  ARCH -. consults .- SYN
  V -. centuries-old pairing .- SIS["The Sisters of the Long Patience · Hessa"]
  KER["THE KERIS · exiled house · Korya · slate/ice"]
  RES["The resistance · Sable's Undersiders + Kester"]
  KER -. the real coming war .- ARCH
```

## 2. The Synedrion — nine seats (the Tholos)

```mermaid
graph TD
  SYN["THE SYNEDRION · circular hall: the Tholos · 6 of 8 votes bind"]
  SYN --> S1["Sisters of the Long Patience · Mother Hessa"]
  SYN --> S2["Order of the Just Reading · seat-holder TBD"]
  SYN --> S3["Old Houses · Aurelius (House Corvinus)"]
  SYN --> S4["Healers · Mistress Veliya"]
  SYN --> S5["Universities · TBD"]
  SYN --> S6["Retired Officers · a former Vendine Chair"]
  SYN --> S7["Mercantile Guilds · TBD"]
  SYN --> S8["Frontier Worlds · TBD"]
  SYN --> S9["THE KERIS SEAT · empty 200 years — filled in book three"]
```

---

## 3. House Orrel — senior Vendine house

```mermaid
graph TD
  GFO["Grandfather Orrel † · name TBD · wrote the letter"]
  MAT["Mathilde †"]
  GFO --- MAT
  GFO --> IDR["Idris † · died at birth"]
  GFO --> LYR["Lyra · the renouncer · 80s · keeps the grandfather's papers"]
  GFO --> ALD["Aldric · patriarch · ~80 · dying"]
  MIR["Mireille † · d. Sirenne Insurrection"]
  CAM["Camille · second wife"]
  ALD --- MIR
  ALD --- CAM
  MIR --> BAS["Bastien · the Warden / the saint · runs the Cleanse"]
  CAM --> ROD["Roderic · the favored heir"]
  ROD --> CED["Cedric · small child"]
  GFO -. cadet branch .-> AUR["Aurelan · the internal dissenter"]
  BEA["Beatrice Carnay · household retainer"] -. serves the house .-> ALD
```

## 4. House Aemilius — senior Vendine house

```mermaid
graph TD
  QF["Aemilius elder line"]
  QF --> QUI["Quintus · Council Chair · 76 · ends his own life (bk3)"]
  QF --> BRO["Quintus's brother · Marcus's father"]
  QWF["wife · senior Vendine house"]
  QUI --- QWF
  QUI --> LAV["Lavinia · conventional matriarch"]
  QUI --> OCT["Octavia · the arm's hidden hand · disappears (bk3)"]
  BRO --> MARC["Marcus · the great natural warrior · withdraws (bk3)"]
  SEV["Sevra · fighter wife"]
  MARC --- SEV
  MARC --> LUC["Lucan · 15 · male heir"]
  MARC -. unacknowledged .-> DAU["a daughter · ~19 · Marcus does not know"]
```

## 5. House Caradec — the dissenting Vendine house

```mermaid
graph TD
  TAN["Tancred Caradec · the dissenting house head"]
  YSA["Ysabeau · of House Tarsenne (also dissenting)"]
  TAN --- YSA
  TAN --> JOS["Joscelin · traditional academy"]
  TAN --> GAR["Garin · traditional academy"]
  TAN -. brother .- AUB["Aubin † · served under Bastien on Tartaros · died"]
```

---

## 6. The Keris of Korya — the exiled bloodline

```mermaid
graph TD
  IMI["Imir · grandfather · 80s · dies in book two"]
  IWF["wife † · died during the exile"]
  IMI --- IWF
  IMI --> KAZ["Kazimir · the son · will lead the war"]
  IMI --> SON2["second son † · imprisoned, died"]
  MILA["Milana · Kazimir's wife"]
  KAZ --- MILA
  KAZ --> IVA["Ivana · daughter · fighter · ~7"]
  KAZ --> UNB["unborn son"]
  ASH["Asham · married into the bloodline · Pira's caregiver"]
  ASH -. raises .-> PIR["Pira · outsider child · 6 · carries the archive"]
  PIR --- NAD["Nadya · ordinary Keris child · 9 · best friend"]
  PIR -. fighting friend .- IVA
```

---

## 7. The Narrine (communications) — the Vren family

```mermaid
graph TD
  MARE["Marella Vren · Narrine director · 'the knife and the bandage'"]
  MARE --> CAS["Cassian · editor of The Andra Meridian · the leaker (bk3)"]
  MARE --> SVR["Severine · 46 · Asclepi deputy · disliked by Marella"]
  HUS["husband · the family's anchor"]
  SVR --- HUS
  SVR --> S3["three sons · she schemes to place them in grand houses"]
```

## 8. The Asclepi (medical) and the Limine (frontier)

```mermaid
graph TD
  AEL["Aelia Mardin · Asclepi director · childless"]
  AEL -. grooms as successor .-> SVR2["Severine Vren · deputy"]
  CYR["Professor Cyrus · senior researcher · coerced"]
  SOR["Soraya · wife"]
  CYR --- SOR
  CYR --> NIM["Nimi"]
  CYR --> AMA["Amar"]
  EDR["Edric · Limine coordinator · willful ignorance"]
  EDR --> ESON["son · ~15 · plans to leave"]
  RAK["Raknir Vehl · governor · the bronze city-key"]
  RAK -. disavowed .-> ATT["Atticus Vehl · honorless son"]
```

---

## 9. The Sisters, the Healers, and the Old Houses

```mermaid
graph TD
  SIS["The Sisters of the Long Patience"]
  SIS --> HES["Mother Hessa · 75 · Synedrion seat · embedded with the Vendine"]
  HES -. placed a watcher on .-> CAS2["Cassian Vren"]
  HEAL["The Healers (older medical tradition)"]
  HEAL --> VEL["Mistress Veliya · ~80 · Synedrion seat"]
  VEL -. triggers defection of .-> CYR2["Professor Cyrus"]
  OLD["The Old Houses · House Corvinus"]
  OLD --> AUR2["Aurelius · 70s · Xerxes's cousin · holds the family papers"]
  AUR2 --> LIV["Livia Corvinus · grand-niece · archive heir"]
  AUR2 -. cousins .- XER["Xerxes · the Architect"]
```

---

## 10. The resistance and the fallen (book one)

```mermaid
graph TD
  SAB["Sable Reyek · leader · brother Tomas †"]
  KES["Kester Vaile · the conscience · carries the procurement secret"]
  RESH["Resh · 18 · Sable's protectee"]
  MOU["Mouse · 19 · the prototype · horror-object"]
  DAV["Kell Davour · ex-MP (he)"]
  SAB --- KES
  SAB --- RESH
  SAB --- DAV
  RESH -. recovers .-> MOU
  KES --- MAREN["Maren · separated"]
  KES --> LIR["Lira Vaile · 22 · estranged 11 years"]
  YAR["Yara · the Successor · extracted in book two"]
  SAB -. extracts .-> YAR
  FALL["The fallen of book one: Yenna † · Chayne † · Tev † · Pell † (daughter Iyani) · Aleya †"]
```

---

*Companion files: `../bible/TARTAROS_CYCLE_BIBLE.md` (full canon),
`../bible/TRILOGY_SYNOPSIS.md` (the story and its locked ending),
`../bible/TARTAROS_QUESTIONS.md` (character tracker — closed).*
