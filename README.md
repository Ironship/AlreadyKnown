# Already Known?

![Release](https://github.com/ahakola/AlreadyKnown/actions/workflows/release.yml/badge.svg)

https://www.curseforge.com/wow/addons/alreadyknown

Puts green, blue, yellow, cyan or purple tint on already known scrolls/pets/other learnable items on vendors and AH.

Simple and small addon to color already known items on vendor and AH frames. Works at least on profession designs/patterns/etc, garrison plans, toys, mounts, pets and equipment blueprints.

Default color is green, but try `/alreadyknown` or `/ak` ingame to change the tint color.

Known issues:

* ~~Designs/patterns/etc of already known companion pets/mounts are shown as known even if they aren't~~ Fixed in 1.12!
* Quest based items (like equipment blueprints) - at the moment at least - has to be hard coded into addon, please let me know if you run into yet unsupported quest items sold by vendors.

## This fork: World of Warcraft: Forever

This branch is upstream's addon with a fix for WoW: Forever. Upstream already loads `AlreadyKnownClassic.lua` there, but it decides `isClassic` from `WOW_PROJECT_ID`, which reads as Retail on Forever, so the Classic paths (warlock grimoires, the old auction house) stay off.

The changes:

* `forever.lua`, loaded just before the Classic file, recognises Forever by its client version (1.60 or later) and adds `/akforever` (`/akf`), which prints what the client reports.
* In `AlreadyKnownClassic.lua`, `isClassic` is also true on Forever, the cosmetic-item check only runs when `C_TransmogCollection` exists, and the guild bank hook is kept on Forever.

Everything else, including the licence (MIT, `LICENSE.md`), is Sanex's (ahakola) and unchanged.
