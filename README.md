
🛡️ AI-Driven IDS : Système de Détection d'Intrusions Réseau
Ce projet implémente une Intelligence Artificielle (Random Forest) capable de détecter des cyberattaques (DDoS, Brute Force, Scans) dans des flux réseaux en temps réel. Il se base sur le dataset de référence CIC-IDS2017.

📂 Structure du Projet
Bash
├── data/                     # Dossier à créer pour les données brutes
├── 1_Exploration_Donnees.ipynb   # Nettoyage et Analyse (EDA)
├── 2_Entrainement_Modele.ipynb   # Entraînement et Tests
├── modele_ids_random_forest.pkl  # Le modèle sauvegardé (généré après étape 2)
└── README.md                 # Ce fichier

⚙️ Installation et Configuration
1. Pré-requis
Assurez-vous d'avoir Python installé avec les librairies suivantes :

Bash
pip install pandas numpy scikit-learn seaborn matplotlib joblib gc io sklearn.ensemble sklearn.metrics 

2. Téléchargement des Données (Important !)
Le dataset est trop volumineux pour être inclus directement.

Téléchargez le dataset CIC-IDS2017 via ce lien Kaggle : 👉 Network Intrusion Dataset (CIC-IDS-2017) 
https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset/data  

Note : Verifier bien que y a 8 fichiers

Créez un dossier nommé data à la racine du projet.

Dézippez et placez les fichier .csv téléchargé dans ce dossier data.

🚀 Guide d'Exécution
Pour faire fonctionner le projet, exécutez les notebooks dans cet ordre précis :

Étape 1 : Nettoyage et Exploration
Ouvrez et exécutez 1_Exploration_Donnees.ipynb.

Ce qu'il fait : Charge les données brutes, analyse les statistiques, nettoie les valeurs incorrectes et génère deux fichiers propres : train_set_final.csv et test_set_final.csv.

Étape 2 : Entraînement et Test
Ouvrez et exécutez 2_Entrainement_Modele.ipynb.

Ce qu'il fait : Entraîne le modèle Random Forest sur le jeu d'entraînement, évalue les performances (Matrice de confusion, F1-Score) et sauvegarde le modèle sous modele_ids_random_forest.pkl.

📊 Performances du Modèle
Le modèle atteint des performances de niveau industriel sur le jeu de test :

Précision Globale : 99.84%

Détection des menaces (Rappel) : 99.45%

Fiabilité des alertes (Précision) : 99.63%

👤 Auteurs
AIT ATMANE SAMIR,   Serkan AK 