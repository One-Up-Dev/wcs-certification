# WCS Data Analyst — Guide de Certification

Guide interactif de révision pour la certification **Data Analyst — Wild Code School** ([RNCP 37429](https://www.francecompetences.fr/recherche/rncp/37429/)). Application web statique consultable hors-ligne, organisée selon les 4 blocs du référentiel officiel.

![Made with HTML/CSS/JS](https://img.shields.io/badge/stack-vanilla-blue) ![Python 3.13+](https://img.shields.io/badge/python-3.13%2B-green) ![Statut](https://img.shields.io/badge/statut-en%20construction-orange)

---

## 🎯 Objectif

Reproduire et enrichir en local un guide de révision couvrant **toutes les compétences** du référentiel RNCP&nbsp;37429, avec&nbsp;:

- Une **notion par card** : « Pourquoi c'est important », exemples de code data-oriented, pièges classiques, astuces certif
- Un **contenu aligné sur les versions 2026** des bibliothèques (Python 3.13, Pandas 2.x, NumPy 2.x, scikit-learn 1.7, etc.)
- Une couverture **complète** des compétences RNCP — y compris RGPD, NLP, éthique IA, cartographie, accessibilité dataviz

---

## 📦 Stack technique

| Couche | Choix | Pourquoi |
|--------|-------|----------|
| Structure | HTML5 sémantique | Lisibilité, accessibilité |
| Style | CSS vanilla (custom properties) | Thème centralisé, zéro build |
| Interactivité | JavaScript ES6+ vanilla | Pas de framework pour ce niveau |
| Coloration code | highlight.js 11.9 via CDN | Standard, léger, Python/SQL/Bash |
| Fonts | Roboto + JetBrains Mono (Google Fonts) | Lisibilité, monospace pour le code |
| Icônes | SVG inline (style Lucide) | Zéro dépendance |
| Serveur local | `python -m http.server` | Aucune installation |

**Aucune dépendance npm ni build tool.** Tout est ouvrable directement depuis `index.html`.

---

## 🗂️ Structure du projet

```
wcs-certification/
├── index.html               # Page principale (toutes les sections)
├── styles/
│   ├── main.css             # Variables CSS + reset + layout
│   ├── sidebar.css          # Navigation latérale
│   └── cards.css            # Cards de notion, alerts, code blocks
└── scripts/
    ├── router.js            # Hash routing entre modules
    ├── clipboard.js         # Bouton « Copier » sur chaque bloc de code
    └── search.js            # Recherche temps réel dans le module actif
```

---

## 📚 Modules disponibles

19 modules organisés par bloc du RNCP :

### Bloc 1 — Collecte (102h)
- **SQL Filtrage** — `WHERE`, `LIKE`, `IN`, `BETWEEN`, `NULL`, agrégats, `GROUP BY/HAVING`
- **SQL Jointures** — `INNER/LEFT/RIGHT/FULL`, self-join, sous-requêtes, **CTE**, `UNION`
- **API &amp; JSON** — `requests`, params, auth, gestion d'erreurs, `pd.json_normalize`
- **Scraping** — BeautifulSoup4, sélecteurs CSS, éthique, robots.txt
- **RGPD &amp; Éthique data** — bases légales, droits, anonymisation, IA Act

### Bloc 2 — Préparation (102h)
- **Python Fondamentaux** — 16 notions (Python 3.12+, PEP 695, match/case, dataclass, uv)
- **NumPy** — ndarray, broadcasting, indexing, agrégations, NumPy 2.x
- **Pandas Nettoyage** — `read_csv`, inspection, NaN, doublons, types, PyArrow backend
- **Pandas Transformation** — `apply`, `groupby`, `merge`, `concat`, pivot, method chaining
- **Regex &amp; Anonymisation** — module `re`, patterns prêts, anonymisation pipeline

### Bloc 3 — Analyse (135h)
- **Statistiques** — tendance centrale, dispersion, distributions, corrélation, tests
- **ML Régression** — workflow sklearn, Pipeline, Ridge/Lasso, validation croisée
- **ML Classification** — LogReg, KNN, arbres, métriques, classes déséquilibrées
- **NLP** — spaCy français, TF-IDF, NER, analyse de sentiment
- **Éthique IA &amp; Biais** — fairness metrics, SHAP, IA Act, Model Card

### Bloc 4 — Restitution (206h)
- **Matplotlib &amp; Seaborn** — API OO, subplots, heatmap, pairplot
- **Plotly** — Plotly Express, interactivité, export HTML
- **Folium &amp; Cartographie** — markers, choropleth, HeatMap, accessibilité dataviz
- **Power BI** — Power Query, modèle en étoile, DAX, Time Intelligence, publication

---

## 🚀 Utilisation

### Consultation locale

```bash
cd wcs-certification
python -m http.server 8080
```

Puis ouvrir [http://localhost:8080](http://localhost:8080).

### Navigation

- **Sidebar** : sélection directe d'un module
- **Hash URL** : `#python-fondamentaux`, `#ml-regression`, etc.
- **Recherche** : barre en haut du contenu, filtre les cards du module actif

### Composants par notion

Chaque notion suit le même pattern visuel&nbsp;:

```
┌────────────────────────────────────────────────┐
│  [icône colorée] 1. Titre de la notion         │
├──────────────────────────┬─────────────────────┤
│ Pourquoi c'est important │                     │
│ Points clés              │  Bloc de code       │
│                          │  (filename.py)      │
│ ⚠ Piège classique        │  + bouton Copier    │
│ 💡 Astuce certif         │                     │
└──────────────────────────┴─────────────────────┘
```

---

## 🌿 Branches

| Branche | État | Contenu |
|---------|------|---------|
| `main` | Stable | 19 modules de cours + UI complète |
| `feat/datasets` | En réflexion (local uniquement) | Système de datasets &amp; notebooks Jupyter (15 datasets, 7 notebooks phares) |

---

## 📖 Sources &amp; vérification

Le contenu a été vérifié contre les documentations officielles via **Context7** pour&nbsp;:

| Bibliothèque | Version cible 2026 | Source Context7 |
|--------------|---------------------|------------------|
| Python | 3.13 / 3.14 | `/websites/devdocs_io_python_3_14` |
| NumPy | 2.3.1 | `/numpy/numpy` |
| Pandas | 2.x (PyArrow backend) | `/pandas-dev/pandas` |
| scikit-learn | 1.7.1 | `/scikit-learn/scikit-learn` |
| Matplotlib | stable | `/matplotlib/matplotlib` |
| Plotly | 5.x | `/plotly/plotly.py` |
| requests | 2.x | `/psf/requests` |
| BeautifulSoup4 | 4.13+ | `/wention/beautifulsoup4` |
| spaCy | 3.x | `/explosion/spacy` |
| Folium | latest | `/python-visualization/folium` |

Le contenu **SQL** et **Statistiques** repose sur des concepts standards stables. **Power BI** : connaissances générales DAX/Power Query (non vérifié via Context7).

Référentiel officiel utilisé : [Fiche RNCP 37429 — France Compétences](https://www.francecompetences.fr/recherche/rncp/37429/).

---

## 🎨 Design

- **Palette principale** : Wild Red `#f91f4b` (accent), `#0f172a` (sidebar), `#f8fafc` (fond)
- **Layout** : sidebar fixe 280px + main centré max 1200px
- **Responsive** : sidebar masquée sous 900px
- **Icônes** : SVG inline (style Lucide), 6 couleurs (blue/purple/cyan/green/orange/pink)

---

## 📝 Conventions du contenu

- Mots-clés SQL en MAJUSCULES, colonnes en minuscules
- Snippets Python data-oriented (`df`, `client`, `ventes`)
- Type hints encouragés (`x: int = 5`, `def f() -> str:`)
- f-strings préférées à `.format()` / `%`
- Pandas 2.x : mention du backend PyArrow et copy-on-write
- sklearn : Pipeline systématique (anti-fuite de données)
- Toujours `random_state=42` pour la reproductibilité

---

## ⚠️ Limitations connues

- La certification RNCP 37429 est **inactive depuis le 27 mars 2026** (expiration de l'enregistrement). En attente potentielle d'un renouvellement par WCS.
- Le contenu n'a pas été confronté au support de cours officiel WCS — certains termes peuvent différer.
- Les exemples de code ne sont pas tous exécutés/testés ; à vérifier dans un notebook avant usage en certif.
- Le module Power BI repose sur les connaissances générales (non vérifié Context7).

---

## 🔮 Pistes d'évolution

- [ ] Mode sombre
- [ ] Quiz QCM interactif par module
- [ ] Système de datasets (en exploration sur `feat/datasets`)
- [ ] Notes personnelles persistées (localStorage)
- [ ] Export PDF de révision
- [ ] Flashcards façon Anki
- [ ] Hamburger menu mobile

---

## 📄 Licence

Projet personnel à usage de révision. Contenu pédagogique inspiré du référentiel public RNCP 37429.

---

*Construit avec Claude Code (Anthropic) — Mai 2026*
