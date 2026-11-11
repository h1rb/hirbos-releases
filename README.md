# HirbOS Releases

Öffentlicher Release-Kanal für **HirbOS Maintenance** (Arch-Linux-Paket).
Der Quellcode lebt in einem privaten Repository; hier liegen nur die
Auslieferungsartefakte:

- `hirbos-maintenance-<pkgver>-<pkgrel>-any.pkg.tar.zst` — das Arch-Paket (unsigniert)
- `*.sha256` — Prüfsummen-Sidecar (`sha256sum -c` zur Prüfung)
- `provenance.json` — Bauherkunft (Baucommit, Archiv- und Rezept-Hashes)

Die App prüft `releases/latest` dieses Repos (ohne Login) und installiert per
`sudo pacman -U` im eingebetteten Terminal; danach ist ein Neustart der App nötig.

Verifikation pro Release: Sidecar-Hash, Byte-Vergleich mit dem lokalen
Bauartefakt, Tag- und Body-Prüfung. Historie der Programmänderungen steht im
Changelog des Quell-Repos.
