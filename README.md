tux-diff-demo
=============

## Beschreibung

Beispiel für eigene Diff-Kommandos, sowie die Github *Image-View-Modes*.

## Eigene Diff-Kommandos

Das Script `imgdiff` ist ein auf
[ImageMagick](http://www.imagemagick.org/script/index.php) basierendes
Diff-Kommando für Bilder.

Um es zu benutzen, müssen Sie zuerst ein externes Diff-Kommando konfigurieren:

    $ git config diff.imgdiff.command $PWD/imgdiff

Danach das Git-Attribut `diff` für den `gif` Dateitypen einstellen:

    $ echo "*.gif diff=imgdiff" >> .git/info/attributes

Und zuletzt noch aufrufen:

    $ git diff HEAD~2:tux.gif HEAD^:tux.gif

## Github Image-View-Modes

Github verfügt über ein ähnliches Feature, die sog. [Image View
Modes](https://github.com/blog/817-behold-image-view-modes). Damit werden
Unterschiede zwischen Bildern im Webinterface anschaulich dargestellt.

[Klicken Sie hier](https://github.com/gitbuch/tux-diff-demo/commit/ba633112a98afc596aa1edb37bf0e023b5212c53)
um den Tux so zu betrachten.
