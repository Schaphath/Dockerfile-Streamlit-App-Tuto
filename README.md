# 🩺 Interface Streamlit - Prédiction du Cancer du Sein

Interface web moderne pour la prédiction du cancer du sein via une API FastAPI.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.40-red)
![Docker](https://img.shields.io/badge/Docker-Ready-blue)

---

## Description

Interface utilisateur intuitive permettant de communiquer avec l'API de prédiction du cancer du sein. L'utilisateur saisit 10 paramètres et obtient un diagnostic avec probabilité et niveau de confiance.

---

## Fonctionnalités

- **Résultats visuels** : Affichage clair du diagnostic et du score
- **Validation** : Vérification des données avant envoi à l'API
- **Gestion d'erreurs** : Messages clairs en cas de problème
- **Responsive** : Interface adaptée à tous les écrans

---

## Installation

### Prérequis

- Python 3.12+ (pour installation locale)
- Docker (pour conteneurisation)
- API FastAPI fonctionnelle accessible sur [github](https://github.com/Schaphath/Dockerfile-API-Tuto)

### Option 1 : Installation locale

```bash
# Installer les dépendances
pip install -r requirements-streamlit.txt

# Lancer l'application
streamlit run app_stream.py
```

### Option 2 : Avec Docker

#### Build de l'image

```bash
docker build -t my_app:v1.0.0 .
```

#### Lancer le conteneur

```bash
docker run -d -p 8501:8501 --name my_app_web my_app:v1.0.0
```

#### Gestion du conteneur

```bash
# Voir les logs
docker logs my_app_web

# Arrêter le conteneur
docker stop my_app_web

# Supprimer le conteneur
docker rm my_app_web

# Ou en une fois 
docker rm -f my_app_web

```

---

## Configuration

### Variables d'environnement

| Variable | Description | Valeur par défaut |
|----------|-------------|-------------------|
| `API_URL` | URL de l'API de prédiction | `http://localhost:8000/predict` |


---

## Utilisation

1. **Ouvrir l'interface** : [http://localhost:8501](http://localhost:8501)

2. **Remplir les paramètres** : Saisir les données
   
3. **Lancer l'analyse** : Cliquer sur le bouton "Lancer l'analyse"

4. **Consulter les résultats** :
   - Diagnostic : Bénin ou Malin
   - Probabilité du diagnostic
   - Niveau de confiance du modèle


---

## Auteur

**Madiba**

---

**Interface développée avec Streamlit**