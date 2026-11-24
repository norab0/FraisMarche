# FraisMarché

Application locale de gestion du stock pour un supermarché de proximité. Frontend React/TypeScript/Vite, API Express et base SQLite.

## Prérequis
- Kubuntu avec Node.js 20 ou plus récent
- npm

## Installation
Depuis le dossier du projet :

```bash
npm install
```

## Démarrage
```bash
npm run dev
```
Ouvrir **http://localhost:5173**. L’API locale écoute sur http://localhost:3001.

## Tests et compilation
```bash
npm test
npm run build
npm run start
```

## Données
La base est créée automatiquement dans `data/fraismarche.sqlite`. Elle reste conservée entre les démarrages. Aucun service externe ni compte n’est nécessaire.

Le bouton **« Réinitialiser la démonstration »** demande confirmation puis restaure uniquement les données du projet FraisMarché dans sa base locale. Les DLC du scénario sont recalculées par rapport à la date du jour.

## Scénario de démonstration
1. Ouvrir avec Karim — Responsable de stock. Vérifier « Yaourt nature » à 12 pots.
2. Passer sur Julien, choisir « Déclarer une sortie », lot A, Vente, 3 pots.
3. Vérifier lot A à 4, lot B à 5, total à 9.
4. Revenir sur Karim et ouvrir « Priorités du jour » : le yaourt apparaît une fois à 9 pots.
5. Vendre les 4 pots restants du lot A.
6. Préparer une commande depuis les alertes, corriger la quantité à 8 et valider ; le stock reste à 5.
7. Passer Julien sur « Réceptionner », recevoir 8 pots dans un nouveau lot ; le stock passe à 13.

Les profils jouent uniquement les rôles : ils conservent les mêmes données.