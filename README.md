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

La [version 1.1.1](../../releases/tag/v1.1.1) est publiée pour le **premier
essai Wi-Fi** depuis une carte déjà équipée de la version 1.1.0.
Elle ajuste l'alignement du texte de statut dans Options. Les essais sur
matériel, notamment coupure réseau et retour à la version précédente,
restent à effectuer avant de considérer cette distribution comme validée.

## Précautions

L'affichage et les alarmes de cet appareil sont temporairement suspendus
pendant l'installation. Garder l'appareil alimenté. L'application Dexcom
et ses alarmes restent la référence ; cet afficheur secondaire ne doit jamais
être la seule source d'alarme ni servir seul à une décision de traitement.
