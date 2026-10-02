# Mettre le site en ligne avec GitHub Pages

Durée : 15 minutes la première fois, puis 1 minute pour chaque ajout. Tout se fait dans le navigateur, sans logiciel à installer.

## 1. Créer un compte GitHub

1. Va sur https://github.com et clique sur **Sign up**.
2. Choisis ton nom d'utilisateur avec soin : il apparaîtra dans l'adresse du site
   (`https://nom-utilisateur.github.io/...`). Un nom neutre comme `techno-ndlr` convient bien.
3. Valide ton adresse e-mail.

Conseil : utilise une adresse professionnelle, et active la double authentification
(Settings → Password and authentication).

## 2. Créer le dépôt (repository)

1. En haut à droite, clique sur **+** puis **New repository**.
2. **Repository name** : par exemple `techno-snt` (minuscules, sans espaces ni accents).
3. Coche **Public** (obligatoire pour GitHub Pages avec un compte gratuit).
4. Coche **Add a README file**.
5. Clique sur **Create repository**.

## 3. Envoyer les fichiers

1. Décompresse `site-eleves.zip` sur ton ordinateur.
2. Dans ton dépôt, clique sur **Add file → Upload files**.
3. Ouvre le dossier `site-eleves`, sélectionne **tout son contenu** (pas le dossier lui-même)
   et fais-le glisser dans la zone de dépôt. Les sous-dossiers sont conservés.
4. En bas, écris un message (ex. « Première mise en ligne ») et clique sur **Commit changes**.
5. Vérifie que `index.html` apparaît bien **à la racine** du dépôt, et non dans un dossier `site-eleves/`.

Le README.md proposé par GitHub sera remplacé par le tien : c'est normal.

## 4. Activer le site

1. Dans le dépôt : **Settings** → menu de gauche **Pages**.
2. **Source** : *Deploy from a branch*.
3. **Branch** : `main` et dossier `/ (root)`, puis **Save**.
4. Patiente 1 à 2 minutes et recharge la page : l'adresse du site s'affiche en haut,
   du type `https://nom-utilisateur.github.io/techno-snt/`.

L'onglet **Actions** du dépôt montre le déploiement en cours (pastille orange, puis verte).

## 5. Ajouter une nouvelle activité

1. Dans le dépôt, ouvre le dossier du niveau (ex. `4eme`).
2. **Add file → Upload files**, puis glisse ton fichier.
   Pour créer un sous-dossier de sujet, clique sur **Add file → Create new file** et tape
   `energie/` : la barre oblique crée le dossier (GitHub demande un fichier dedans, glisses-y ta page ensuite).
3. Ouvre `index.html`, clique sur le crayon ✏️ (**Edit**), copie un bloc du tableau `RESSOURCES` :

   ```js
   { niveau:"4eme", sujet:"Énergie", titre:"Le circuit électrique",
     description:"Simulateur : branche les composants et observe le courant.",
     fichier:"4eme/energie/circuit-electrique.html" },
   ```

4. **Commit changes**. Le site est à jour en une ou deux minutes.

Règles pour les noms : minuscules, sans accents, sans espaces (tirets à la place).
Les accents sont autorisés dans `titre`, `sujet` et `description`.

## 6. Partager avec les élèves

- Envoie l'adresse du site via EcoleDirecte (message ou cahier de textes).
- Tu peux générer un QR code de l'adresse pour l'afficher en salle ou le projeter.
- Pour une page précise : `https://nom-utilisateur.github.io/techno-snt/4eme/energie/circuit-electrique.html`.

## Points de vigilance

- **Le site est public** : aucun nom d'élève, photo ou note dans les fichiers.
  L'outil « Élections de classe » ne contient aucune donnée : la liste saisie reste
  uniquement dans le navigateur de l'ordinateur qui l'utilise.
- Les pages qui mémorisent une progression (localStorage) le font sur chaque appareil :
  un élève qui change d'ordinateur repart de zéro.
- Une page ne s'affiche pas ? Vérifie le chemin dans `fichier` (majuscules, accents, extension `.html`).
- Si une page enregistrée depuis Claude utilise des fonctions propres à Claude
  (IA intégrée, sauvegarde partagée), elle ne fonctionnera pas sur GitHub Pages :
  demande à Claude une version autonome du fichier.
