# WiFi Dominator

Un outil d'audit de sécurité WiFi multifonctionnel, conçu pour des fins éducatives et de recherche en sécurité.

**Avertissement :** Cet outil est puissant. Ne l'utilisez que sur des réseaux que vous possédez ou pour lesquels vous avez une autorisation explicite. L'utilisation non autorisée de cet outil est illégale.

## Fonctionnalités

* **Vecteur 1 (Extraction Locale) :** Extrait les mots de passe Wi-Fi enregistrés sur Windows, macOS et Linux.
* **Vecteur 2 (Sniffing & Deauth) :** Capture les handshakes WPA/WPA2 en utilisant une attaque par désauthentification.
* **Vecteur 3 (Evil Twin) :** Crée un faux point d'accès avec un portail captif pour l'ingénierie sociale.

## Prérequis

* Python 3.x
* Privilèges root / Administrateur
* Une carte sans fil compatible avec le mode moniteur (pour les vecteurs 2 et 3)
* La suite `aircrack-ng` (pour le cracking)

## Installation

1.  Clonez le dépôt :
    ```bash
    git clone [https://github.com/bendjinymous/Wifi-Dominator.git](https://github.com/bendjinymous/Wifi-Dominator.git)
    cd Wifi-Dominator
    ```

2.  Installez les dépendances Python :
    ```bash
    pip install -r requirements.txt
    ```

## Utilisation

```bash
# Extraire les mots de passe locaux
sudo python3 dominator.py --local

# Sniffer un réseau
sudo python3 dominator.py --sniff -i wlan0mon -t "MonWiFi" -w /chemin/vers/wordlist.txt

# Lancer une attaque Evil Twin
sudo python3 dominator.py --evil-twin -i wlan0 -t "WiFi_Gratuit"
