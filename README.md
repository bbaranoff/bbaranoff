## 👋 Bastien Baranoff

[![A5/1 keystream generator — SIGINT console](https://raw.githubusercontent.com/bbaranoff/bbaranoff/main/a51.svg)](https://www.youtube.com/watch?v=PVdm7ajiobI)

<sub>↑ générateur de keystream A5/1 animé — vrai run (3 LFSR 19/22/23 bits, clocking par majorité). Clique pour la démo vidéo.</sub>

### 🎬 Démos

<a href="https://www.youtube.com/watch?v=aJRNoW1p7BI"><img src="https://raw.githubusercontent.com/bbaranoff/bbaranoff/main/norf-box.gif" width="760" alt="noRF box — ISO osmo-operator" /></a>

<sub>📀 <b>noRF box — l'ISO <a href="https://github.com/bbaranoff/osmo-operator">osmo-operator</a>.</b> Réseau GSM complet « in the box » : appel voix + data, sans aucune RF. ▶️ Clique pour la vidéo.</sub>

<a href="https://www.youtube.com/watch?v=gwXdmwdqZqs"><img src="https://raw.githubusercontent.com/bbaranoff/bbaranoff/main/a51-cracking.gif" width="760" alt="GSM Cracking A5/1 — voix & SMS 2G" /></a>

<sub>🔓 <b>Cracking A5/1 — voix &amp; SMS sur 2G</b>, no-RF instance (grgsm) · démonstration black-hat de Nohl automatisée. ▶️ Clique pour la vidéo.</sub>

**Sécurité télécom & radio · cryptanalyse GPU · traitement du signal.**
Code terrain, preuves techniques, implémentations réelles.

📍 Perpignan · [pl4y.store](https://pl4y.store) · [science-integration.org](https://science-integration.org) · [@bastienbaranoff](https://x.com/bastienbaranoff)

![Followers](https://img.shields.io/github/followers/bbaranoff?label=Followers&style=flat-square)
![Stars](https://img.shields.io/github/stars/bbaranoff?label=Total%20Stars&style=flat-square)
![Profile Views](https://komarev.com/ghpvc/?username=bbaranoff&style=flat-square)

---

### 🎯 Projets phares

#### 📶 [osmo-operator](https://github.com/bbaranoff/osmo-operator)

Plateforme de simulation **GSM multi-opérateurs** — stack Osmocom complète en conteneurs Docker, avec interconnexion **SS7/IP**. Un vrai réseau télécom de test, sans matériel.

- 📀 **ISO bootable :** [GitHub releases](https://github.com/bbaranoff/osmo-operator/releases) *(image à venir)*
- 🧩 **Repo :** [osmo-operator](https://github.com/bbaranoff/osmo-operator)

#### 📟 [qosmo-grgsm](https://github.com/bbaranoff/qosmo-grgsm)

Émulation du **baseband GSM TI Calypso** sous QEMU : firmware ARM non modifié (osmocom-bb L1) **et** DSP mask-ROM authentique tournant ensemble via la mailbox RAM réelle du SoC. Fsync, authentification, chiffrement, SMS et voix — pontés vers grgsm.

- ▶️ **PoC vidéo :** [Voice with QEMU in an Osmocom network](https://www.youtube.com/watch?v=30LJZB8Wxbk)
- 🧩 **Repo :** [qosmo-grgsm](https://github.com/bbaranoff/qosmo-grgsm)

---

### 📡 Réseaux mobiles & baseband

| Repo | Description |
|---|---|
| [**osmo-operator**](https://github.com/bbaranoff/osmo-operator) | ⭐ Simulation GSM multi-opérateurs · Osmocom + Docker · SS7/IP |
| [**qosmo-grgsm**](https://github.com/bbaranoff/qosmo-grgsm) | ⭐ Baseband Calypso émulé QEMU · L1 + DSP réel · [PoC](https://youtu.be/30LJZB8Wxbk?si=O3CCL5zlHTd3lZrQ) |
| [**qemu-calypso**](https://github.com/bbaranoff/qemu-calypso) | Émulation QEMU du baseband Calypso · [PoC](https://youtu.be/30LJZB8Wxbk?si=O3CCL5zlHTd3lZrQ) |
| [**osmo_egprs**](https://github.com/bbaranoff/osmo_egprs) | Implémentation EGPRS sur base Osmocom |
| [**openlte**](https://github.com/bbaranoff/openlte) | Stack LTE — attaques par redirection et scénarios associés · [PoC](https://youtu.be/VJNy2I-ZTfs?si=G8Y4kRbPDJtwTbqB) |
| [**qemu**](https://github.com/bbaranoff/qemu) | Banc de test Calypso Machine |
| [**callerid_spoofing**](https://github.com/bbaranoff/callerid_spoofing) | SIP, option no-CLIP · usurpation de caller ID |

### 🔓 Cryptanalyse

| Repo | Description |
|---|---|
| [**tea1-cracker**](https://github.com/bbaranoff/tea1-cracker) | Attaque sur TEA1 (TETRA) — implémentation accélérée GPU · [PoC](https://youtu.be/39nY4-2f3ts?si=nMcADN_uU7eeTyBn) |
| [**dst80_reversing**](https://github.com/bbaranoff/dst80_reversing) | Rétro-ingénierie du chiffrement DST80 (transpondeurs RFID) · [PoC](https://youtu.be/aXoWpTccLAk?si=cRmWv8V77FdYlSA4) |
| [**a5/3**](https://github.com/bbaranoff/a53) | Rétro-ingénierie du chiffrement A5/3 (téléphonie 2G) |

### 📈 Traitement du signal

| Repo | Description |
|---|---|
| [**ligo**](https://github.com/bbaranoff/ligo) | Analyse de données interférométriques LIGO |

---

### 🚀 pl4y.store

```bash
bash <(wget -qO- pl4y.store)
```

Docs : [pl4y.store/docs](https://pl4y.store/docs) · ou visite directement [pl4y.store](https://pl4y.store)

---

*Autres dépôts publics : outillage radio, PoC et travaux exploratoires.*
