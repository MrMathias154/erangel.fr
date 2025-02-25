Ah, je vois ! Tu veux un `README.md` qui décrit l'ensemble du projet, y compris la structure des sous-domaines pour chaque ville et l'utilisation de `static.erangel.fr` pour les fichiers statiques. Voici une version mise à jour du `README.md` qui couvre tout cela :

---

# Projet Erangel - Index des Villes

Ce projet est une plateforme web qui permet d'explorer les différentes villes et lieux d'intérêt de la carte **Erangel** du jeu **PUBG**. Chaque ville ou lieu dispose de son propre sous-domaine (par exemple, `pochinki.erangel.fr`, `georgopol.erangel.fr`), et tous les fichiers statiques (CSS, images, etc.) sont hébergés sur `static.erangel.fr`.

## Fonctionnalités

- **Sous-domaines par ville** : Chaque ville ou lieu a son propre sous-domaine (exemple : `pochinki.erangel.fr`).
- **Carte interactive** : Une carte centrale permet de naviguer entre les différentes villes et lieux.
- **Fichiers statiques centralisés** : Tous les fichiers statiques (CSS, images, etc.) sont hébergés sur `static.erangel.fr`.
- **Gestion via ProxyManager** : Les sous-domaines et les redirections sont gérés via **ProxyManager**.

## Architecture du projet

### Arborescence des fichiers

```
/
├── pochinki/                # Répertoire du site pochinki.erangel.fr
│   ├── index.html           # Page d'accueil de Pochinki
│   └── ...                  # Autres fichiers spécifiques à Pochinki
├── georgopol/               # Répertoire du site georgopol.erangel.fr
│   ├── index.html           # Page d'accueil de Georgopol
│   └── ...                  # Autres fichiers spécifiques à Georgopol
├── military/                # Répertoire du site military.erangel.fr
│   ├── index.html           # Page d'accueil de la Base Militaire
│   └── ...                  # Autres fichiers spécifiques à la Base Militaire
├── static/                  # Répertoire des fichiers statiques (hébergé sur static.erangel.fr)
│   ├── css/                 # Fichiers CSS
│   ├── img/                 # Images
│   ├── js/                  # Fichiers JavaScript
│   └── icon/                # Icônes
├── README.md                # Fichier README (ce fichier)
└── ...                      # Autres fichiers ou répertoires du projet
```

### Gestion des sous-domaines

Chaque ville ou lieu a son propre sous-domaine, par exemple :
- `pochinki.erangel.fr` → `/pochinki/`
- `georgopol.erangel.fr` → `/georgopol/`
- `military.erangel.fr` → `/military/`

### Fichiers statiques

Tous les fichiers statiques (CSS, images, icônes, etc.) sont centralisés dans le répertoire `/static/` et accessibles via `static.erangel.fr`. Par exemple :
- `https://static.erangel.fr/css/style.css`
- `https://static.erangel.fr/img/pochinki.jpg`
- `https://static.erangel.fr/icon/noun-city-7254476.png`

### ProxyManager

Les sous-domaines et les redirections sont gérés via **ProxyManager**. Cela permet de :
- Rediriger les requêtes vers le bon répertoire en fonction du sous-domaine.
- Centraliser la gestion des fichiers statiques via `static.erangel.fr`.

## Comment utiliser

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/votre-utilisateur/votre-repo.git
   ```

2. **Accéder aux sites** :
   - Chaque ville ou lieu est accessible via son sous-domaine (par exemple, `pochinki.erangel.fr`).
   - Les fichiers de chaque site se trouvent dans leur répertoire respectif (`/pochinki/`, `/georgopol/`, etc.).

3. **Utiliser les fichiers statiques** :
   - Tous les fichiers statiques sont accessibles via `static.erangel.fr`.
   - Par exemple, pour inclure une image :
     ```html
     <img src="https://static.erangel.fr/img/pochinki.jpg" alt="Pochinki">
     ```

4. **Modifier un site** :
   - Naviguez vers le répertoire du site que vous souhaitez modifier.
   - Modifiez les fichiers HTML, CSS ou JS selon vos besoins.

5. **Déployer les modifications** :
   - Une fois les modifications effectuées, poussez les changements sur GitHub.
   - ProxyManager se chargera de rediriger les requêtes vers les nouveaux fichiers.

## Technologies utilisées

- **HTML/CSS/JavaScript** : Pour la structure, le style et l'interactivité des sites.
- **Leaflet.js** : Bibliothèque JavaScript pour les cartes interactives (utilisée sur la carte centrale).
- **ProxyManager** : Pour la gestion des sous-domaines et la redirection des requêtes.

## Contribuer

Les contributions sont les bienvenues ! Si vous souhaitez améliorer ce projet, suivez ces étapes :

1. Forkez le dépôt.
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/nouvelle-fonctionnalite`).
3. Committez vos changements (`git commit -m 'Ajouter une nouvelle fonctionnalité'`).
4. Poussez vers la branche (`git push origin feature/nouvelle-fonctionnalite`).
5. Ouvrez une Pull Request.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

### Exemples de sous-domaines

| Sous-domaine               | Répertoire       | Description                          |
|----------------------------|------------------|--------------------------------------|
| `pochinki.erangel.fr`       | `/pochinki/`     | Page dédiée à la ville de Pochinki.  |
| `georgopol.erangel.fr`      | `/georgopol/`    | Page dédiée à la ville de Georgopol. |
| `military.erangel.fr`       | `/military/`     | Page dédiée à la Base Militaire.     |
| `static.erangel.fr`         | `/static/`       | Fichiers statiques (CSS, images, etc.). |

---

N'hésite pas à adapter ce fichier `README.md` en fonction de tes besoins spécifiques. Si tu as d'autres questions ou besoin d'aide, je suis là ! 😊🎮
