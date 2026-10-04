# Anna CGM Display — mises à jour

Ce dépôt public est réservé à la distribution des firmwares pour la carte
**Waveshare ESP32-S3-Touch-LCD-4B, Flash 16 Mo DIO / PSRAM 8 Mo OPI**.
Il ne contient ni identifiants Wi-Fi/Dexcom, ni relevés de glycémie.

## Avertissement — projet indépendant

Anna CGM Display est un projet indépendant, non officiel, non affilié à Dexcom
et non approuvé par Dexcom.

Ce logiciel fournit un affichage secondaire des données. Il ne remplace ni
l’application ou le récepteur Dexcom, ni leurs alarmes, ni les conseils d’un
professionnel de santé.

Les informations affichées peuvent être retardées, incomplètes ou indisponibles.
Ne prenez aucune décision de traitement sur la seule base de cet afficheur.

Le logiciel est fourni « en l’état », sans garantie de fonctionnement continu
ni d’absence d’erreurs, dans les limites autorisées par la loi. Aucune mention
ne vise à exclure une responsabilité qui ne peut légalement être exclue.

Dexcom et les noms de ses produits sont des marques de leurs titulaires respectifs.

Dans le firmware intégrant cet avertissement, le texte apparaît au premier
démarrage, y compris après une mise à jour depuis une version sans avertissement.
Le bouton « J’ai lu et compris » confirme sa lecture ; il ne constitue pas une
renonciation aux droits ou recours. Cette confirmation est conservée sur la carte
et le texte reste accessible dans **Options → À propos**. Un effacement complet
des réglages entraîne une nouvelle présentation de l’avertissement.

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

La [version 1.1.12](https://github.com/Hesse56/Esp32-Anna-updates/releases/tag/v1.1.12)
redessine les indicateurs de tendance avec des formes pleines et des anneaux
réguliers. Sur la courbe historique, le seuil haut est rouge et le seuil bas
est bleu, conformément aux couleurs des alarmes.

La version 1.1.9 ajoute le choix automatique ou manuel du fuseau horaire
pour les voyages, ainsi que plusieurs corrections de fiabilité. La base
embarquée provient d'IANA 2026e / tzdata 2026.5 ; sa provenance et sa licence
sont détaillées dans [TIMEZONE_DATA_LICENSE.txt](TIMEZONE_DATA_LICENSE.txt).

La [version 1.1.6](https://github.com/Hesse56/Esp32-Anna-updates/releases/tag/v1.1.6)
ajoute l'avertissement au premier démarrage, améliore l'heure de veille,
la page MAJ et la courbe tactile, et aligne le statut Dexcom. Lire
l'avertissement sur la carte après l'installation ; l'application Dexcom
reste la référence.

La [version 1.1.3](https://github.com/Hesse56/Esp32-Anna-updates/releases/tag/v1.1.3)
est publiée pour tester l'installation Wi-Fi depuis une carte équipée de
la version 1.1.2. Elle conserve la correction des téléchargements GitHub
et l'alignement du statut dans Options. La recherche et la signature ont
été validées sur la carte ; l'installation Wi-Fi a été validée le
4 octobre 2026. Le test volontaire de retour arrière reste à effectuer.

Ne pas réinstaller la version 1.1.1 : elle contient un défaut de tampon
HTTP corrigé à partir de la 1.1.2.

## Précautions

L'affichage et les alarmes de cet appareil sont temporairement suspendus
pendant l'installation. Garder l'appareil alimenté. L'application Dexcom
et ses alarmes restent la référence ; cet afficheur secondaire ne doit jamais
être la seule source d'alarme ni servir seul à une décision de traitement.
