
  # Futuristic Tech School Landing Page

  >Projet techSchool LGC

  ## Détails techniques
  
  - Pile: Vite + React 18 + TypeScript + Motion (animations) + CSS utilitaire pré‑générée (pas de build Tailwind requis à l’exécution).
  - Entrée: `index.html` charge `src/main.tsx` qui monte `src/App.tsx`.
  - Navigation ancrée: le composant `src/components/Nav.tsx` fournit un menu centré avec scroll fluide vers `#formations`, `#team`, `#events` et gestion mobile (burger → croix, panneau animé). Les sections utilisent `scrollMarginTop` pour éviter d’être masquées par la barre fixe.
  - Accessibilité: attributs ARIA validés (bouton burger avec `aria-haspopup/aria-expanded`, `role="menu"`/`role="menuitem"` sur le panneau mobile).
  - TypeScript: configuration JSX moderne via `tsconfig.json` (`jsx: react-jsx`, `jsxImportSource: react`) et types React/DOM installés.
  - Imports « versionnés »: Vite résout les alias dans `vite.config.ts` (ex: `lucide-react@0.487.0` → `lucide-react`), et TypeScript est informé via `src/types/alias-modules.d.ts`.
  - Assets statiques: tout fichier placé sous `public/` est servi à la racine.
    - Dossiers présents: `public/assets/` et `public/asset/` (selon besoin projet).
    - Exemple d’utilisation: `<img src="/asset/avatar.png" alt="..." />` ou `<img src="/asset/avatar.svg" />`.
  - Clés de listes: remplacées par des clés stables (titre/nom/label) dans les composants pour éviter les warnings React.
  
  ## Scripts utiles
  
  - `npm run dev` — lance Vite en mode développement (port 3000 par défaut).
  - `npm run build` — build de production dans `build/`.
  - `npx tsc --noEmit` — vérification de type TypeScript sans émission.
  
  ## Structure (extrait)
  
  - `src/components/` — sections de la page (Hero, Formations, Team, Events, etc.) et UI.
  - `src/components/Nav.tsx` — barre de navigation centrée (desktop) et burger animé (mobile).
  - `public/asset/` et `public/assets/` — fichiers statiques servis par Vite.
  
