# faderport-xair-raspi-bridge
Control a Behringer X Air XR16 with a FaderPort 16 via Raspberry Pi (MCU ↔ OSC bridge)

# 🎛️ XR16-FaderBridge

**Contrôler une Behringer X Air XR16 avec un FaderPort 16 via un Raspberry Pi 4**  
🛠️ Projet open-source de passerelle MIDI MCU ↔ OSC pour mixage live assisté par surface de contrôle

---

## 🎯 Objectif

Créer un système simple, stable et open-source permettant de piloter une **Behringer X Air XR16** avec une **surface motorisée PreSonus FaderPort 16**, en utilisant un **Raspberry Pi 4** comme interface de conversion MIDI ↔ OSC.

> 🎚️ Objectif final : mixer en live avec un FaderPort, sans PC, avec retour moteur complet et compatibilité avec X Air Edit ou l’app mobile.

---

## 🧱 Matériel visé

- **Raspberry Pi 4 B (4 Go recommandé)**
- **FaderPort 16** (mode MCU)
- **Behringer X Air XR16**
- **Câble USB-A vers USB-B** (FaderPort → Pi)
- **Câble Ethernet** (Pi ↔ XR16)
- **Alimentation USB-C 5V/3A pour le Pi**

---

## 📡 Connexions prévues

- FaderPort connecté en USB au Raspberry Pi
- Le Pi communique avec la XR16 en OSC via Ethernet
- En parallèle, X Air Edit et l’application mobile restent utilisables

---

## ✅ Fonctionnalités prévues

- ✳️ Mode unique initial : **FaderPort → XR16 via Raspberry Pi**
- Traduction **MIDI MCU** vers **OSC** : faders, mute, pan, etc.
- **Retour OSC vers MCU** : mise à jour moteur et LEDs
- 🛠️ Scripts Python légers et configurables
- **Zéro PC** requis une fois le Raspberry lancé

---

## 🔜 Évolutions futures (non prioritaires)

- 🔁 **Switch de mode** entre "XR16" et "DAW" (USB MIDI Gadget)
- ⚡ **Alimentation GPIO 5V** pour libérer le port USB-C
- 🌐 Interface web (Flask) pour config et monitoring
- 🧠 Apprentissage automatique du mapping (optionnel)

---

## 📅 État du projet

🧪 **En cours de conception**  
Aucune ligne de code écrite pour l’instant – l’objectif est de documenter, organiser, puis démarrer le prototypage ouvertement.

---

## 📚 Ressources techniques

### 🎚️ Protocole MCU (Mackie Control Universal)
- Specifation MCU Protocol: http://www.midibox.org/dokuwiki/doku.php?id=mc_protocol_mappings
- MCU DIY Guide: https://sites.google.com/view/mackiecontroluniversaldiyguide/home
  
### 🎛️ Protocole OSC XR16/XR18
- Guide démarrage rapide xAir16: https://manuals.plus/fr/behringer/x-air-xr16-digital-mixer-for-ios-and-android-manual
- Manuel : https://mediadl.musictribe.com/media/PLM/data/docs/X-AIR/M_BE_0605-AAA_X-AIR_FR.pdf
- X AIR Mixer Series Remote Control Protocol: https://mediadl.musictribe.com/download/software/behringer/XAIR/X%20AIR%20Remote%20Control%20Protocol.pdf 
### 🧠 Outils Python

- [`python-rtmidi`](https://pypi.org/project/python-rtmidi/) – pour écouter/émettre des messages MIDI
- [`python-osc`](https://pypi.org/project/python-osc/) – pour envoyer/recevoir des messages OSC
- [`mido`](https://mido.readthedocs.io/en/latest/) – alternative pour traitement MIDI simple

---

## 💬 Contributions bienvenues

Le projet est **ouvert à la contribution** dès maintenant : idées, discussions, documentation, suggestions d’implémentation, tests futurs…

---

## 📜 Licence

MIT
