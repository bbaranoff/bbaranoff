# osmo-operator-desktop.iso — v0.2

![osmo-operator: the GSM LAB desktop, the mast beacon over the city](https://raw.githubusercontent.com/bbaranoff/osmo-operator/main/configs/osmo-balise-jour.png)

[![Build ISO](https://github.com/bbaranoff/osmo-operator/actions/workflows/build-iso.yml/badge.svg?branch=main&event=workflow_dispatch)](https://github.com/bbaranoff/osmo-operator/actions/workflows/build-iso.yml)

**osmo-operator** : un banc GSM/LTE pédagogique et multi-opérateurs qui tourne sur une seule machine, sans SDR ni téléphone physique.
Le réseau Osmocom complet (BTS, BSC, MSC, HLR, MGW, SMSC, GPRS, Asterisk) sert des téléphones Calypso émulés.
L'ARM tourne sous QEMU et le DSP TI C54x exécute sa vraie ROM masque. Le téléphone s'enregistre sur le réseau, s'authentifie, chiffre, envoie des SMS et passe des appels.
En 4G : Open5GS, srsRAN, le repli 4G → 2G pour les appels (CSFB) et un téléphone postmarketOS. Plusieurs opérateurs peuvent s'interconnecter en SS7 via un STP.

[![Voir la vidéo](https://img.youtube.com/vi/-UY50ZZ_mLc/maxresdefault.jpg)](https://www.youtube.com/watch?v=-UY50ZZ_mLc)

---

### 💿 Télécharger l'ISO desktop (v0.1-9)

Live GNOME avec tout le banc prêt à l'emploi (2G, DSP, 4G, CSFB, postmarketOS), plus Wireshark, Linphone et les spectres I/Q. Rien à compiler.

- [Part 00](https://github.com/bbaranoff/osmo-operator/releases/download/v0.1-9/osmo-operator-desktop.iso.part-00)
- [Part 01](https://github.com/bbaranoff/osmo-operator/releases/download/v0.1-9/osmo-operator-desktop.iso.part-01)
- [Part 02](https://github.com/bbaranoff/osmo-operator/releases/download/v0.1-9/osmo-operator-desktop.iso.part-02)
- [Part 03](https://github.com/bbaranoff/osmo-operator/releases/download/v0.1-9/osmo-operator-desktop.iso.part-03)
- [SHA256SUMS](https://github.com/bbaranoff/osmo-operator/releases/download/v0.1-9/SHA256SUMS)

> [!IMPORTANT]
> Télécharge **les quatre** parties : GitHub limite chaque fichier à 2 Gio.

```bash
cat osmo-operator-desktop.iso.part-* > osmo-operator-desktop.iso
sha256sum -c --ignore-missing SHA256SUMS
qemu-system-x86_64 -cdrom osmo-operator-desktop.iso -m 8G -enable-kvm -cpu host -smp 4 \
  -nic user,hostfwd=tcp::8080-:8080
```

| | |
|---|---|
| Mot de passe live | `osmo` |
| Mot de passe du téléphone postmarketOS | `147147` |
| Machine minimale | x86_64, 8 Go de RAM, 4 cœurs, virtualisation imbriquée activée si l'ISO tourne dans une VM |

La release contient aussi `osmo-operator.iso` (sans le bureau), `osmo-operator-lite.iso` (sans les sources) et `interstp.iso` (le STP seul) : [toutes les images v0.1-9](https://github.com/bbaranoff/osmo-operator/releases/tag/v0.1-9).

---

### 📡 Réseaux mobiles & baseband

| Repo | Description |
|---|---|
| [**osmo-operator**](https://github.com/bbaranoff/osmo-operator) | ⭐ Opérateur GSM/LTE complet · Osmocom + Open5GS · multi-PLMN interconnectés en SS7/IP · Docker, natif ou ISO |
| [**qosmo**](https://github.com/bbaranoff/qosmo) | ⭐ Baseband Calypso émulé sous QEMU · layer1 OsmocomBB ou firmware TI d'origine (Magnetite) |
| [**c54x_exe**](https://github.com/bbaranoff/c54x_exe) | ⭐ Émulateur du DSP TI C54x du Calypso, exécuté sur l'hôte avec la vraie ROM masque |
| [**grgsm_exe**](https://github.com/bbaranoff/grgsm_exe) | ⭐ Layer 1 gr-gsm à la place du DSP |

---

### 🚀 pl4y.store

```bash
bash <(wget -qO- pl4y.store)
```

Docs : [pl4y.store/docs](https://pl4y.store/docs) · ou directement [pl4y.store](https://pl4y.store)

---

*Autres dépôts publics : outillage radio, PoC et travaux exploratoires.*
