# AC Zone Control — firmwares

Binaires prêts à installer pour le système AC Zone Control (centrale + télécommandes de zone).
Le code source est dans le dépôt privé `rkroman-86/ac-zone-control` (base Tasmota, licence GPL-3.0).

## Mise à jour depuis l'appareil

Interface web de l'appareil → **Firmware Upgrade** → **Start upgrade**.

L'URL de mise à jour est intégrée au firmware. Pour un appareil qui tourne encore avec une autre URL, la définir une fois dans la console :

| Appareil | Commande console |
|---|---|
| Centrale ESP32 | `OtaUrl https://raw.githubusercontent.com/rkroman-86/ac-zone-control-firmware/main/centrale/tasmota32-centrale.bin` |
| Télécommandes | à venir |

Chaque appareil a un chemin fixe sur la branche `main` : le lien reste le même, le fichier est remplacé à chaque nouvelle version (les versions précédentes restent dans l'historique git). Notes de version : [`centrale/CHANGELOG.md`](centrale/CHANGELOG.md).

## Contenu

- `centrale/` — centrale ESP32 (rail DIN) : AP+STA permanent (`WifiConfig 11`), IRHVAC, relais, sondes DS18B20, Berry
- `telecommandes/` — télécommandes de zone (à venir)

Les fichiers `.bin` sont des images de mise à jour OTA (pas des images `factory`).
