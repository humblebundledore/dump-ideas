# Système de Gestion des Connaissances par IA

## Vue d'ensemble

Pensez-y comme une **cuisine professionnelle** :
- Le dossier **template** est le livre de recettes — la référence absolue
- Le dossier **brut** est le plan de travail — les ingrédients déposés et grossièrement triés
- Le dossier **traité** est l'assiette finale — le résultat produit par l'IA
- Le dossier **compétences** est le manuel de formation du chef — les règles que suit l'IA

---

## Arborescence des dossiers

```
espace-de-travail-ia/
│
├── _template/                        ← Le plan de référence (ne jamais modifier)
│   ├── structure-dossiers.md         ← Dossiers requis et leur contenu attendu
│   ├── conventions-nommage.md        ← Comment nommer les fichiers (dates, préfixes, etc.)
│   ├── exemples-rendus/              ← Exemple de résultat final parfait
│   │   ├── exemple-rapport.pdf
│   │   └── exemple-synthese.docx
│   └── checklist-qualite.md          ← Ce que signifie "c'est terminé"
│
├── _competences/                     ← Manuels d'instructions pour l'IA (règles lues avant chaque traitement)
│   ├── regle-01-traitement-vocal.md       ← Transcrire, nettoyer les mots parasites, identifier les intervenants...
│   ├── regle-02-traitement-papier.md      ← OCR, corriger les erreurs de scan, extraire les données clés...
│   ├── regle-03-traitement-texte.md       ← Nettoyage emails/chat, extraire les actions à mener...
│   ├── regle-04-comment-synthetiser.md    ← Ton, longueur, structure des synthèses
│   └── regle-05-mise-en-forme.md          ← Titres, langue (FR/EN), format d'export
│
├── clients/
│   │
│   ├── dupont-sa/
│   │   ├── brut/                     ← Déposer tout ici, grossièrement trié
│   │   │   ├── vocal/                ← Mémos vocaux, enregistrements de réunions (.mp3, .m4a)
│   │   │   ├── texte/                ← Emails, exports de chat, notes (.txt, .docx)
│   │   │   ├── papier/               ← Documents scannés (.pdf, .jpg)
│   │   │   └── autre/                ← Tout ce qui ne rentre pas dans les catégories ci-dessus
│   │   │
│   │   └── traite/                   ← Résultat produit par l'IA, prêt à livrer
│   │       ├── syntheses/
│   │       ├── rapports/
│   │       └── actions-a-mener/
│   │
│   └── martin-consulting/
│       ├── brut/
│       │   ├── vocal/
│       │   ├── texte/
│       │   ├── papier/
│       │   └── autre/
│       └── traite/
│           ├── syntheses/
│           ├── rapports/
│           └── actions-a-mener/
```

---

## A-t-on besoin du dossier `_competences` ?

**Oui, absolument** — c'est en réalité la partie la plus importante.

Sans règles, l'IA produit des résultats incohérents. Le dossier compétences est ce qui rend le système **répétable et professionnel**. Imaginez l'intégration d'un nouvel employé : on ne lui remet pas juste des fichiers en espérant le mieux — on lui donne un manuel de procédures.

Règles essentielles à rédiger dès le départ :

| Fichier de règle | Ce qu'il résout |
|---|---|
| `regle-01-traitement-vocal` | Comment transcrire les enregistrements, gérer les chevauchements de parole, identifier les intervenants |
| `regle-02-traitement-papier` | Comment lire les docs scannés, ce qu'il faut ignorer (en-têtes/pieds de page), ce qu'il faut extraire |
| `regle-03-comment-synthetiser` | Longueur, ton (formel/informel), langue, ce qui doit toujours apparaître |
| `regle-04-mise-en-forme` | Nommage des fichiers, emplacement, format d'export (PDF ou Word) |

---

## Le flux de travail

```
[Réunion client / visite terrain]
        ↓
  brut/ ← l'équipe dépose tout (mémo vocal, photo de tableau blanc, fil d'emails)
        ↓
  L'IA lit les règles de _competences/ et le plan de référence _template/
        ↓
  traite/ ← synthèses propres, rapports, actions à mener — prêts à envoyer
```

L'équipe n'a besoin de faire que l'étape 1. Le reste, c'est le travail de l'IA.

---

## Notes

- Ajouter un nouveau client = simplement créer un nouveau dossier dans `clients/`
- Les règles et le template restent identiques → qualité homogène pour tous les clients
- Le préfixe `_` sur `_template/` et `_competences/` les place en haut de l'explorateur de fichiers et indique "fichiers système — ne pas toucher"
