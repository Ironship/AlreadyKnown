# Known Recipes

Known Recipes tints items you already know on vendors, in the auction house and in the guild bank: recipes, pets, mounts, toys, warlock grimoires and other learnable items. It is made for WoW: Forever and also runs on Classic and Retail.

It began as a fork of [Already Known?](https://github.com/ahakola/AlreadyKnown) by Sanex (ahakola) and is now its own addon, with its own name, settings and commands, so the two can be installed side by side.

What it adds to Already Known?:

* Recognises Forever by its client version, since Forever reports Retail's `WOW_PROJECT_ID`, and turns on the Classic paths there, such as the warlock grimoires.
* A grimoire counts as known when your demon has its spell at that rank or higher, even under another spell id. What each demon has shown is kept for the character, so grimoires stay tinted while another demon is out.
* Items it knows to be known get a red "Already known" line in their tooltip when the game does not add one.
* The cosmetic-item check runs only when `C_TransmogCollection` exists, and the guild bank hook stays on for Forever.

Commands: `/knownrecipes` (`/kr`) sets the colour; `/krforever` (`/krf`) prints what the client reports, and `/krf pet` lists your demon's spellbook and the spells kept for it.

Install: unzip the release zip into `Interface\AddOns`, so the folder is `Interface\AddOns\KnownRecipes`.

Licence: MIT (`LICENSE.md`), which keeps the original author's notice.
