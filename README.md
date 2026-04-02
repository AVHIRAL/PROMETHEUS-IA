# Prometheus AI

# Téléchargement : https://www.avhiral.com/download/Prometheus.zip

# Modèle GGUF : https://huggingface.co/

**Prometheus AI** est un assistant IA local en Python, développé par **AVHIRAL TE@M**.  

L’application propose une interface Tkinter moderne, le chargement local de modèles **GGUF**, la gestion des conversations, la génération de code, la rédaction de contenus, la prévisualisation de pièces jointes, ainsi que plusieurs options d’optimisation CPU / GPU.

---

## Points forts

- Assistant IA local
- Chargement direct de modèles **`.gguf`** sans conversion préalable
- Interface graphique **Tkinter**
- Conversations persistantes
- Mémoire locale chiffrée
- Génération de texte, code, résumés et articles
- Coloration syntaxique pour le code
- Support des pièces jointes texte, images, PDF, DOCX et ZIP
- OCR optionnel
- Optimisation CPU / GPU selon la machine et le backend
- Réponses en streaming
- Compatible **Windows / Linux / macOS** en version Python
- Version **Windows EXE** possible pour les utilisateurs sans Python

---

## Compatibilité

### Version Python
La version Python est conçue pour fonctionner sur :
- **Windows**
- **Linux**
- **macOS**

### Version Windows EXE
Une version **EXE** peut être proposée pour Windows pour les utilisateurs qui ne souhaitent pas installer Python.

### À propos d’AVX / AVX2
Prometheus AI a été pensé pour rester souple côté compatibilité.  
L’application Python elle-même ne dépend pas directement d’AVX/AVX2, mais la compatibilité réelle dépend aussi :
- de la version de Python,
- du backend `llama-cpp-python`,
- du modèle chargé,
- de la build installée sur la machine.

Autrement dit, l’application ne force pas à elle seule une exigence AVX / AVX2, mais il faut vérifier la chaîne complète d’exécution sur chaque configuration.

---

## Fonctionnalités principales

### 1. Chargement local de modèles GGUF
Prometheus AI peut ouvrir un fichier modèle local directement au format **`.gguf`**.

### 2. Interface graphique
L’application utilise **Tkinter** avec une interface sombre moderne.

### 3. Conversations persistantes
Les conversations sont stockées localement avec création, sauvegarde, suppression et rechargement.

### 4. Mémoire locale chiffrée
Une mémoire locale est gérée via un fichier chiffré afin de conserver un contexte exploitable sur la machine.

### 5. Pièces jointes
Le programme peut lire ou prévisualiser :
- fichiers texte,
- images,
- PDF,
- DOCX,
- ZIP.

### 6. Génération de code et coloration syntaxique
Prometheus AI inclut une logique de coloration syntaxique pour plusieurs langages.

### 7. Recherche web simple
Le projet intègre une recherche web légère avec extraction de contenu et construction de contexte.

### 8. Exécution locale avec `llama.cpp`
Le moteur s’appuie sur **`llama-cpp-python`** avec génération locale et streaming.

---

## Dépendances Python

### Dépendances de base

```bash
pip install llama-cpp-python pillow
```

### Dépendances optionnelles

```bash
pip install pytesseract psutil pygments PyPDF2 python-docx
```

### Résumé
- `llama-cpp-python` : moteur LLM local
- `Pillow` : images / prévisualisation
- `pytesseract` : OCR optionnel
- `psutil` : informations système / RAM
- `pygments` : coloration syntaxique
- `PyPDF2` : lecture PDF
- `python-docx` : lecture DOCX

---

## Installation

### 1. Cloner le dépôt

```bash
git clone <URL_DU_DEPOT>
cd <DOSSIER_DU_PROJET>
```

### 2. Créer un environnement Python

#### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux / macOS
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Installer les dépendances

```bash
pip install --upgrade pip
pip install llama-cpp-python pillow pytesseract psutil pygments PyPDF2 python-docx
```

### 4. Lancer le programme

```bash
python Prometheus.py
```

ou selon le nom du fichier principal :

```bash
python Prometheus_9.4.py
```

---

## Utilisation

### Charger un modèle
- lancer l’application ;
- sélectionner un modèle **`.gguf`** local ;
- attendre l’initialisation du moteur.

### Démarrer une conversation
- créer une nouvelle discussion ;
- écrire une demande ;
- laisser le moteur générer la réponse en streaming.

### Charger des pièces jointes
Le programme peut prévisualiser ou extraire le texte de plusieurs formats :
- `.txt`
- `.py`
- `.md`
- `.json`
- `.csv`
- `.log`
- `.html`
- `.css`
- `.js`
- `.xml`
- `.yaml`
- `.yml`
- `.ini`
- `.cfg`
- `.png`
- `.jpg`
- `.jpeg`
- `.gif`
- `.bmp`
- `.webp`
- `.pdf`
- `.docx`
- `.zip`

---

## Structure fonctionnelle

Le code contient notamment les composants suivants :

- `ConversationStore` : gestion des conversations
- `MemoryVault` : mémoire locale chiffrée
- `FileHandler` : lecture / prévisualisation des fichiers
- `WebResearcher` : recherche web simple
- `CodeHighlighter` : coloration syntaxique
- `LlamaEngine` : moteur de chargement et génération locale

---

## Philosophie du projet

Prometheus AI vise à fournir un **assistant local réellement utile**, capable de :
- suivre un échange,
- aider à la rédaction,
- générer et améliorer du code,
- travailler avec des modèles GGUF locaux,
- rester exploitable sur plusieurs environnements.

La qualité finale dépend naturellement :
- du modèle GGUF utilisé,
- de la quantification,
- de la VRAM,
- du CPU / GPU,
- du backend `llama-cpp` installé.

---

## Limitations

- la qualité dépend fortement du modèle GGUF utilisé ;
- les performances varient selon CPU, GPU, RAM et backend ;
- certaines fonctions sont optionnelles selon les bibliothèques installées ;
- l’OCR nécessite un environnement correctement configuré ;
- la compatibilité machine dépend aussi de la build de `llama-cpp-python`.

---

## Roadmap possible

- amélioration du suivi du contexte
- enrichissement des réponses longues
- meilleure détection et suppression des doublons
- amélioration des articles et résumés
- optimisation GPU plus avancée
- packaging Windows plus propre
- amélioration de la gestion multi-modèles

---

## Auteur

**Développé par AVHIRAL TE@M**

Discord :  
`https://discord.gg/daxTVZ2kGy`

---

## Recommandation GitHub

Tu peux ajouter ce README avec :
- `README.md`
- éventuellement un `requirements.txt`
- un dossier `models/` vide avec un `.gitkeep`
- un dossier `conversations/` ignoré dans `.gitignore`

Exemple `.gitignore` :

```gitignore
__pycache__/
*.pyc
venv/
.env
conversations/
memory.avhiral
*.gguf
*.zip
```

---

DON PAYPAL : https://www.paypal.com/donate/?hosted_button_id=FSX7RHUT4BDRY

## Note finale

Prometheus AI est un projet local ambitieux, orienté usage réel, avec une base Python importante et une architecture déjà riche.  
Le projet a pour objectif de proposer un assistant local autonome, pratique et évolutif, tout en laissant le choix du modèle et du matériel à l’utilisateur.
