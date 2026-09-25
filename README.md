# Already Known? for WoW: Forever

[Already Known?](https://github.com/ahakola/AlreadyKnown) by Sanex (ahakola) tints items you already know on vendors and the auction house. This fork makes it work on WoW: Forever.

What this fork changes:

* `forever.lua` recognises Forever by its client version, because Forever reports Retail's `WOW_PROJECT_ID` and upstream's Classic detection misses it.
* `AlreadyKnownClassic.lua` turns its Classic paths on for Forever, so grimoires and the old auction house are handled.
* The cosmetic-item check runs only when `C_TransmogCollection` exists, since Forever may not have it.
* The warlock grimoire check uses `C_SpellBook` where `HasPetSpells` and `GetSpellBookItemName` no longer exist, as on Forever; before, a vendor selling grimoires raised an error.
* The guild bank hook stays on for Forever, which Classic Era would switch off.
* `/akforever` (`/akf`) prints what the client reports, for troubleshooting.

Install: unzip the release zip into `Interface\AddOns`, so the folder is `Interface\AddOns\AlreadyKnown`.

Licence: MIT, as in the original project (`LICENSE.md`).
