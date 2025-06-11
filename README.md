# SpaceX Launches Tracker 🚀

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Tkinter](https://img.shields.io/badge/GUI-Tkinter-green)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-orange)
![Selenium](https://img.shields.io/badge/Scraping-Selenium-yellowgreen)
![Matplotlib](https://img.shields.io/badge/Visualization-Matplotlib-red)

Une application desktop Python pour suivre les lancements SpaceX, stocker les données dans MongoDB, et afficher des statistiques graphiques.

## 📌 Fonctionnalités
- **Scraping des données** depuis [spacex.com/launches](https://www.spacex.com/launches/) avec Selenium.
- **Stockage** dans une base MongoDB locale.
- **Interface intuitive** avec Tkinter :
  - Affichage des missions dans un tableau interactif.
  - Boutons pour actualiser les données, vider la base, ou générer des graphiques.
- **Visualisation** avec Matplotlib :
  - Graphiques des lancements par organisation/cliente.
- **Export JSON** des données scrapées (indépendant de la base MongoDB).

## 🛠 Installation
1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/Akemi-ito/SpaceX-Launches-Tracker.git
   cd SpaceX-Launches-Tracker
   ```

2. **Installer les dépendances** :
   ```bash
   pip install -r requirements.txt
   ```

3. **Configurer MongoDB** :
   - Installez [MongoDB Community Server](https://www.mongodb.com/try/download/community).
   - Lancez le service MongoDB (ex: `sudo systemctl start mongod` sur Linux).

4. **ChromeDriver** :
   - Téléchargez [ChromeDriver](https://chromedriver.chromium.org/) compatible avec votre version de Chrome.
   - Placez le fichier dans `C:/chemin/vers/chromedriver.exe` (ou modifiez le chemin dans `spacex_scraper.py`).

## 🖥 Utilisation
1. Lancer l'application :
   ```bash
   python main.py
   ```

2. **Actions disponibles** :
   - **Actualiser les données** : Télécharge les dernières missions SpaceX.
   - **Effacer la base** : Supprime toutes les données MongoDB.
   - **Générer des stats** : Affiche un graphique des lancements par organisation.

3. **Fichier JSON** :
   - Les données scrapées sont sauvegardées dans `data/spacex_launches.json` (non affecté par la vidange de la base).

## 📂 Structure du Projet
```
SpaceX-Launches-Tracker/
├── assets/                   # Logo et ressources
├── database/
│   └── db_operations.py      # Interactions MongoDB
├── scraping/
│   └── spacex_scraper.py     # Scraping avec Selenium
├── utils/
│   └── utils.py              # Graphiques et boîtes de dialogue
├── main.py                   # Point d'entrée
├── main_window.py            # Interface Tkinter
└── README.md
```

## 📸 Captures d'Écran
| Interface Principale | Graphique des Stats |
|----------------------|---------------------|
| ![Interface](assets/screenshot_main.png) | ![Graphique](assets/screenshot_stats.png) |

## 🔧 Technologies
- **Python 3.8+**
- **Tkinter** : Interface graphique.
- **MongoDB** : Base de données NoSQL.
- **Selenium** : Scraping web.
- **Matplotlib** : Visualisation des données.
- **Pillow (PIL)** : Gestion des images (logo).

---

## 🧑‍💻 Auteurs

* [Akemi-ito](https://github.com/Akemi-ito)

---

📚 *Projet universitaire - Ynov B3A Data & IA - 2025*
