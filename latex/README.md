# Template LaTeX -- Rendus de Master (Thème Darkred)

Template LaTeX moderne et modulaire spécialement conçu pour les rendus de rapports, projets et travaux pratiques en Master.

---

## 📁 Structure du projet

```
template/
├── main.tex       # Document principal (métadonnées à modifier + contenu du rapport)
├── template.sty   # Feuille de style (packages, thème darkred, en-têtes, boîtes)
├── README.md      # Documentation et guide d'utilisation
└── .gitignore     # Fichiers temporaires LaTeX ignorés
```

---

## 🚀 Utilisation rapide

1. **Dupliquer le dossier** pour chaque nouveau projet ou rendu de Master.
2. Ouvrir [main.tex](file:///home/edynak/Documents/Etudes/Master/Rendus/template/main.tex) et personnaliser les informations au début du fichier :
   ```latex
   \matiere{Nom de la Matière}
   \titre{Titre du Rapport}
   \soustitre{Sous-titre (optionnel)}
   \auteur{Prénom Nom}
   \formation{Master Informatique}
   \etablissement{Université}
   \annee{2026 -- 2027}
   ```
3. Décommenter dans le corps de `main.tex` les blocs préfaits dont vous avez besoin (`\section`, `infobox`, `warningbox`, figures, code, etc.).
4. Compiler avec `pdflatex` :
   ```bash
   pdflatex main.tex
   ```

---

## 🎨 Caractéristiques du template

- **Couleur principale :** `darkred` (`#8B0000`) appliquée de façon cohérente (titres de section, filets décoratifs, numérotation des pages, liens hypertexte, listes à puces).
- **Page de garde :** Présentation élégante avec bandeau latéral, informations de l'université, du master, titre, auteur et encadrant.
- **En-têtes et pieds de page (`fancyhdr`) :**
  - **En-tête gauche :** Matière du rapport en `darkred` gras.
  - **En-tête droit :** Section courante.
  - **Pied de page gauche :** Nom de l'auteur.
  - **Pied de page droit :** Numéro de page en `darkred` gras.
- **Boîtes de dialogue stylisées (TikZ) :**
  - `\begin{infobox}[Titre] ... \end{infobox}` (Bleu)
  - `\begin{warningbox}[Titre] ... \end{warningbox}` (Ambre / Orange)
  - `\begin{notebox}[Titre] ... \end{notebox}` (`darkred` du thème)
  - `\begin{tipbox}[Titre] ... \end{tipbox}` (Vert)
  - `\begin{dangerbox}[Titre] ... \end{dangerbox}` (Rouge vif)
- **Code source (`listings`) :** Style prédéfini avec coloration syntaxique, mots-clés en `darkred`, fond doux et numérotation des lignes.
