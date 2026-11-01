# SmartMonument — Reconnaissance des monuments historiques marocains par CNN et LLM

## Présentation du projet

**SmartMonument** est une application intelligente développée dans le cadre de mon Projet de Fin d'Études (PFE), visant à valoriser le patrimoine historique et culturel du Maroc grâce à l'intelligence artificielle.

L'application permet d'identifier automatiquement des monuments historiques marocains à partir d'une photographie et de fournir des informations historiques à travers un chatbot intelligent.

Ce projet combine deux technologies principales :

- **CNN (Convolutional Neural Network) :** un modèle de Deep Learning basé sur MobileNetV2, utilisé pour reconnaître les monuments historiques à partir d'images.
- **LLM (Large Language Model) :** Llama 3, exécuté localement avec Ollama, permettant aux utilisateurs de poser des questions et d'obtenir des réponses sur les monuments identifiés.

L'ensemble est intégré dans une interface web interactive développée avec **Streamlit**.

## Fonctionnement de l'application

L'application fonctionne en plusieurs étapes :

1. **Importation d'une image :** l'utilisateur téléverse une photographie d'un monument historique marocain.
2. **Reconnaissance du monument :** le modèle CNN analyse l'image et prédit le monument correspondant.
3. **Affichage du résultat :** l'application affiche le nom du monument identifié et le score de confiance du modèle.
4. **Informations historiques :** l'utilisateur peut consulter les informations associées au monument.
5. **Interaction avec le chatbot :** l'utilisateur peut poser des questions sur l'histoire, l'architecture, la localisation et l'importance culturelle du monument.

Le modèle est entraîné sur **21 classes de monuments historiques marocains** et peut reconnaître de nouvelles photographies des monuments appartenant à ces classes.

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python | Développement de l'application |
| TensorFlow / Keras | Reconnaissance des images avec CNN |
| MobileNetV2 | Modèle de classification |
| Streamlit | Interface web interactive |
| Ollama | Exécution locale du LLM |
| Llama 3 | Chatbot intelligent |
| JSON | Informations historiques et noms des monuments |

## Structure du projet

```text
pfe_idsd/
│
├── app.py
├── best_model_phase1_v2.h5
├── class_names.json
├── monuments_infos.json
├── image/
├── images/
├── requirements.txt
├── README.md
└── .gitignore
```

Le fichier `app.py` constitue le point d'entrée de l'application.

Le modèle CNN entraîné est enregistré dans `best_model_phase1_v2.h5`.

## Installation et exécution sur un autre ordinateur

Pour utiliser SmartMonument sur un autre ordinateur Windows, suivre les étapes ci-dessous.

### 1. Installer les prérequis

Installer les logiciels suivants :

- Python 3.10
- Git
- Ollama

Liens de téléchargement :

- Python : https://www.python.org/downloads/
- Git : https://git-scm.com/
- Ollama : https://ollama.com/

### 2. Télécharger le projet depuis GitHub

Ouvrir un terminal et exécuter :

```bash
git clone https://github.com/ouahbiwalid32-droid/SmartMonument.git
cd SmartMonument
```

Ces commandes permettent de télécharger le dépôt GitHub et d'accéder au dossier du projet.

**Remarque :** le dépôt doit avoir été publié sous le nom `SmartMonument` pour que cette adresse fonctionne.

### 3. Créer un environnement virtuel Python

Dans le terminal, exécuter :

```powershell
python -m venv .venv
```

Activer l'environnement virtuel sous Windows :

```powershell
.venv\Scripts\activate
```

Si PowerShell bloque l'activation, utiliser directement `.venv\Scripts\python.exe` à la place de `python` dans les commandes suivantes.

### 4. Installer les bibliothèques nécessaires

Exécuter :

```powershell
python -m pip install -r requirements.txt
```

Cette commande installe les bibliothèques Python nécessaires au fonctionnement de l'application.

Le fichier `requirements.txt` doit être présent dans le dépôt GitHub et contenir les dépendances compatibles du projet.

### 5. Installer et préparer Llama 3 avec Ollama

Après avoir installé Ollama, ouvrir un terminal et exécuter :

```powershell
ollama pull llama3
```

Cette commande télécharge le modèle de langage Llama 3.

Vérifier ensuite qu'Ollama fonctionne. Si son service n'est pas déjà démarré, exécuter :

```powershell
ollama serve
```

Conserver le service actif pendant l'utilisation du chatbot.

### 6. Vérifier les fichiers du modèle CNN

Vérifier la présence des fichiers suivants dans le dossier du projet :

```text
best_model_phase1_v2.h5
class_names.json
monuments_infos.json
```

Ces fichiers sont nécessaires à la reconnaissance des monuments et à l'affichage des informations historiques.

Si le modèle `.h5` est hébergé séparément du dépôt GitHub, le télécharger et le placer à l'emplacement attendu par `app.py`.

### 7. Lancer l'application Streamlit

Dans le terminal, depuis le dossier du projet, exécuter :

```powershell
python -m streamlit run app.py
```

L'application sera normalement accessible à l'adresse suivante :

http://localhost:8501

L'utilisateur pourra alors :

- Importer une image d'un monument historique marocain.
- Obtenir le résultat de reconnaissance du CNN.
- Consulter les informations historiques du monument identifié.
- Interagir avec le chatbot Llama 3 pour obtenir des informations supplémentaires.

## Auteur

**Walid Ouahbi**

Étudiant en cycle d'ingénieur — Génie de l'Intelligence Artificielle et Machine Learning

Projet de Fin d'Études — SmartMonument (DUT Informatique Décisionnelle et Sciences de Données

Maroc
