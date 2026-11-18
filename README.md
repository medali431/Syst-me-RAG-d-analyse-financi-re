#  FallahTech - Analyse Financière par RAG (Retrieval-Augmented Generation)

Ce projet implémente un système de Question-Réponse (Q&A) basé sur l'architecture **RAG** pour analyser la solidité financière de l'entreprise **FallahTech**. Il extrait des informations à partir de documents PDF et de fichiers Excel, puis utilise un modèle de langage (LLM) pour générer une analyse de solvabilité et de liquidité.

##  Fonctionnalités


- **Chargement multi-formats** : Lecture automatisée de documents PDF et de fichiers Excel.
- **Découpage intelligent** : Segmentation des textes (Chunking) avec chevauchement pour ne rien perdre du contexte.
- **Base de données vectorielle** : Stockage des embeddings dans ChromaDB pour une recherche sémantique ultra-rapide.
- **LLM puissant** : Utilisation de `llama-3.3-70b-versatile` via l'API ultra-rapide de **Groq**.
- **Prompt Engineering** : Instructions précises pour forcer l'IA à ne pas inventer de données (zéro hallucination) et à citer ses sources.

##  Technologies utilisées


- **Python 3.12**
- **LangChain** : Pour l'orchestration du pipeline RAG.
- **Groq API** : Pour l'inférence du LLM (Llama 3.3).
- **ChromaDB** : Base de données vectorielle locale.
- **HuggingFace (Sentence-Transformers)** : Modèle `all-MiniLM-L6-v2` pour la génération des embeddings.
- **Pandas & Openpyxl** : Pour le traitement des données Excel.
- **PyPDF** : Pour l'extraction de texte des fichiers PDF.

##  Prérequis


Avant de lancer le projet, assurez-vous d'avoir :
1. Un compte Google (pour Google Colab et Google Drive).
2. Une clé API **Groq** (gratuite). Vous pouvez en créer une sur [console.groq.com](https://console.groq.com/).

Configurez la clé dans la variable d'environnement `GROQ_API_KEY` avant d'exécuter
le notebook. Sous PowerShell :

```powershell
$env:GROQ_API_KEY = "votre-cle-groq"
```

Dans Google Colab, utilisez l'onglet **Secrets** pour enregistrer `GROQ_API_KEY`
et autorisez le notebook à y accéder. Ne placez jamais la clé directement dans
le notebook ou dans un fichier versionné.

## ⚙️ Installation et Configuration

1. **Cloner le dépôt :**
   ```bash
   git clone https://github.com/votre-nom-utilisateur/votre-repo.git
   cd votre-repo