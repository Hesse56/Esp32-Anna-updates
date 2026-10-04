# Anna CGM Display — mises à jour

Ce dépôt public est réservé à la distribution des firmwares pour la carte
**Waveshare ESP32-S3-Touch-LCD-4B, Flash 16 Mo DIO / PSRAM 8 Mo OPI**.
Il ne contient ni identifiants Wi-Fi/Dexcom, ni relevés de glycémie.

## Depuis l'appareil

Avec un firmware compatible : **Options → MAJ → Rechercher une mise à jour**.
L'appareil présente la version et les changements, puis demande confirmation.
Il télécharge le firmware par Wi-Fi, vérifie sa signature et son intégrité,
et redémarre. Aucun compte GitHub n'est nécessaire.

La version 1.0 nécessite d'abord une installation USB du support de mise à jour.
Ne pas utiliser un fichier `firmware.factory.bin` pour une mise à jour distante.

## Publications

Chaque Release validée contiendra uniquement :

- `firmware.bin` : application destinée à cette carte ;
- `manifest.txt` : version, modèle, taille, empreinte et résumé ;
- `manifest.sig` : signature du manifeste.

La [version 1.1.3](https://github.com/Hesse56/Esp32-Anna-updates/releases/tag/v1.1.3)
est publiée pour tester l'installation Wi-Fi depuis une carte équipée de
la version 1.1.2. Elle conserve la correction des téléchargements GitHub
et l'alignement du statut dans Options. La recherche et la signature ont
été validées sur la carte ; l'installation et le retour arrière restent
à tester avant de considérer cette distribution comme validée.

Ne pas réinstaller la version 1.1.1 : elle contient un défaut de tampon
HTTP corrigé à partir de la 1.1.2.

## Précautions

L'affichage et les alarmes de cet appareil sont temporairement suspendus
pendant l'installation. Garder l'appareil alimenté. L'application Dexcom
et ses alarmes restent la référence ; cet afficheur secondaire ne doit jamais
être la seule source d'alarme ni servir seul à une décision de traitement.
