# WiFi Dominator

Dépôt d’archives contenant des versions packagées de **WiFi Dominator**.

> ⚠️ **Important**
> Les fichiers livrés dans `kokan/*.zip` sont des binaires/chargeurs obfusqués (LuaJIT + scripts `.txt`) et **pas** un code source Python lisible.
> Utilisez uniquement dans un environnement de laboratoire autorisé, hors machine de production.

## Contenu du dépôt

- `kokan/Dominator-Wifi-v1.7.zip`
- `kokan/Wifi_Dominator_1.1.zip`
- `README.md`

## Corrections appliquées

Les anciennes instructions étaient erronées :
- elles utilisaient une URL `.zip` directement dans `git clone` (invalide),
- elles passaient un fichier `.zip` à `pip install -r` (invalide),
- elles lançaient `python3` sur une URL `.zip` (invalide).

Cette documentation remplace ces commandes par une procédure locale cohérente.

## Prérequis

- Windows (les archives contiennent `Launcher.cmd` et `luajit.exe`)
- Outil de décompression ZIP (`PowerShell`, `7-Zip`, etc.)
- Environnement de test isolé (VM recommandée)

## Installation (locale)

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/Bendjinymous/Wifi-Dominator.git
   cd Wifi-Dominator
   ```

2. Extraire une version :
   ```bash
   unzip kokan/Dominator-Wifi-v1.7.zip -d build/Dominator-Wifi-v1.7
   ```

## Exécution

Depuis le dossier extrait, lancer :

```bat
Launcher.cmd
```

## Vérification d’intégrité des archives

```bash
unzip -t kokan/Dominator-Wifi-v1.7.zip
unzip -t kokan/Wifi_Dominator_1.1.zip
```

## Avertissement légal

N’utilisez ces outils que sur des réseaux vous appartenant ou pour lesquels vous disposez d’une autorisation explicite.
