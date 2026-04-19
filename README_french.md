# 🚌 GTFS4EV

## 📚 Documentation et matériel de formation

GTFS4EV est un outil open source en Python conçu pour soutenir la planification de l’électrification des bus publics. En s’appuyant sur le format standardisé General Transit Feed Specification (GTFS), il permet aux planificateurs et aux chercheurs de simuler rapidement les opérations de bus et d’explorer différents scénarios d’électrification sans nécessiter de données propriétaires ni de données opérationnelles détaillées au niveau des véhicules.

- 📖 **Documentation complète** : Guide utilisateur, API et méthodologie  
- 💻 **Projet GitHub** : Code source, exemples  
- 🐍 Langage : Python 3.12  

---

## 🧠 Aperçu du modèle

Le modèle permet de simuler rapidement les opérations de bus et d’explorer des scénarios d’électrification en utilisant les données GTFS comme entrée principale. Il comble l’écart entre les simulateurs détaillés basés sur des agents et les calculateurs simplifiés, en proposant un processus de simulation modulaire comprenant le prétraitement des données GTFS, la simulation des opérations de flotte et de recharge, ainsi qu’une analyse a posteriori des impacts de l’électrification (économies de CO₂, réduction de l’exposition à la pollution de l’air, économies de carburant) et l’intégration potentielle de l’énergie photovoltaïque.

Les fonctionnalités principales de GTFS4EV couvrent trois dimensions clés :

1. **Prétraitement des données GTFS** : validation et nettoyage des données GTFS.  
2. **Simulation des opérations de flotte** : estimation du nombre de véhicules en service et de leurs schémas de déplacement.  
3. **Recharge basée sur des scénarios** : estimation de la demande de recharge, faisabilité et besoins en infrastructure.  

---

## ⚙️ Installation

### 🐍 Configuration Python

```bash
conda create --name evpv-env python=3.12
conda activate gtfs4ev-env
```

### 📦 Installer GTFS4EV

```bash
pip install gtfs4ev
```

---

## ▶️ Utilisation de GTFS4EV

### 🔹 Étape 1 : Préparer votre configuration

- Adapter le fichier `cli_basic.py`  
- Vérifier les données GTFS  

### 🔹 Étape 2 : Lancer le modèle

```bash
gtfs4ev
```

---

## 🧪 Utilisation avancée

```python
from gtfs4ev.core.gtfsmanager import GTFSManager
from gtfs4ev.core.fleetsimulator import FleetSimulator
from gtfs4ev.core.chargingsimulator import ChargingSimulator
```

---

## ⭐ Fonctionnalités

- Filtrage et enrichissement GTFS  
- Intégration photovoltaïque  
- Analyse des impacts (CO₂, pollution, coûts)  
- Stratégies de recharge flexibles  
- Visualisation spatiale  
- CLI ou bibliothèque Python  

---

## 📜 Licence

GNU GPLv3  
