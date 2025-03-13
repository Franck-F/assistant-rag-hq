# Assistant IA RAG Avancé avec Hypothetical Questions (HQ)

## 💡 Description
Cet assistant IA est basé sur **Retrieval-Augmented Generation (RAG)** avec une approche avancée exploitant les **Hypothetical Questions (HQ)** pour améliorer la pertinence des réponses. Il intègre un pipeline optimisé pour récupérer des informations précises et fournir des réponses en citant exactement la source des documents.

##  Technologies Utilisées
- **Base de connaissances** : ChromaDB, BM25
- **Optimisation de la recherche** : Cohere Reranking
- **Framework** : LangChain
- **Modèle de génération** : OpenAI
- **Backend** : FastAPI
- **Frontend** : Streamlit
- **Extraction de texte des PDF** : Pydantic

##  Fonctionnalités
- ✅ **Extraction et indexation des documents PDF**
- ✅ **Génération de questions hypothétiques (HQ) pour améliorer la recherche**
- ✅ **Recherche hybride (BM25 + Vectorielle + Reranking Cohere)**
- ✅ **Génération de réponses contextuelles**
- ✅ **Affichage des sources utilisées pour chaque réponse**
- ✅ **Interface interactive en Streamlit**

##  Installation
### 1. Cloner le projet
```bash
git clone https://github.com/ton_projet/Assistant_rag_hq.git
cd assistant-rag-hq
```
### 2. Installer les dépendances
Créer un environnement virtuel (optionnel) :
```bash
python -m venv venv
source venv/bin/activate  # Sur Windows : venv\Scripts\activate
```
Puis installer les dépendances :
```bash
pip install -r requirements.txt
```

### 3. Configurer les variables d'environnement
Créer un fichier `.env` pour stocker les clés API (OpenAI, Cohere, etc.) :
```env
OPENAI_API_KEY=your_openai_key
COHERE_API_KEY=your_cohere_key
```

### 4. Lancer le backend (FastAPI)
```bash
uvicorn app.main:app --reload
```
Accéder à la documentation interactive : [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

### 5. Lancer l'interface utilisateur (Streamlit)
```bash
streamlit run app/frontend.py
```

## 🌐 Architecture du Projet
```bash
assistant-rag-hq/
│── app/
│   ├── main.py          # Backend FastAPI
│   ├── retriever.py     # Récupération et ranking des documents
│   ├── generator.py     # Génération de réponses
│   ├── hq_generator.py  # Génération des Hypothetical Questions
│   ├── pdf_parser.py    # Extraction de texte des PDF
│   ├── config.py        # Configuration des clés API
│   └── frontend.py      # Interface utilisateur Streamlit
├── requirements.txt     # Dépendances du projet
├── README.md            # Documentation
├── .env  
└── RAG_Avancé.ipynb                # Exemple de configuration
```

##  Améliorations Futures
-  **Ajout d'un système de feedback utilisateur**
-  **Meilleure visualisation des sources citées**
-  **Optimisation des embeddings pour de meilleures performances**

##  Contribution
Les contributions sont les bienvenues ! Ouvrez une issue ou faites une pull request.

## 🛡️ Licence
Ce projet est sous licence GNU.

