# Design Tokens

Figma est la source de référence actuelle des design tokens FormaPilot. Cette synchronisation correspond à la bibliothèque **FormaPilot UI 0.1.0** dans le fichier Figma **FormaPilot — Product Design**.

Le snapshot local est généré depuis Figma et ne doit pas être modifié manuellement. Toute évolution de tokens doit partir de Figma, être resynchronisée dans une branche dédiée, puis passer par une pull request.

## Collections

Collections publiques synchronisées :

- `Semantic`
- `Dimensions`

Collection interne :

- `Primitives`

La collection `Primitives` ne constitue pas une API publique côté code. Elle peut apparaître dans `design-tokens/figma.snapshot.json` uniquement comme origine d'alias pour les variables Semantic.

## Nommage CSS

Les variables CSS sont générées dans `src/styles/tokens.css`.

Quand Figma définit une syntaxe Web, elle est prioritaire. Exemple : `action/primary/default` devient `--color-action-primary-default`.

Quand Figma ne définit pas de syntaxe Web, la convention locale applique le préfixe de groupe :

- `space/4` devient `--space-4`
- `radius/md` devient `--radius-md`
- `control/height-md` devient `--control-height-md`
- `icon/size-md` devient `--icon-size-md`
- `layout/content-max` devient `--layout-content-max`
- `stroke/default` devient `--stroke-default`

Pour la version `0.1.0`, les dimensions sont conservées en pixels.

## Resynchronisation

1. Ouvrir une branche dédiée, jamais `main`.
2. Inspecter Figma en lecture seule.
3. Régénérer `design-tokens/figma.snapshot.json` depuis les collections publiques `Semantic` et `Dimensions`.
4. Régénérer `src/styles/tokens.css` à partir du snapshot.
5. Mettre à jour ce document et vérifier la table de correspondance.
6. Ouvrir une pull request avec le rapport de différences.

Ne modifiez jamais `design-tokens/figma.snapshot.json` directement pour changer une valeur de design. La source de vérité reste Figma.

## Correspondance

| Figma token | CSS property | Valeur | Usage |
| --- | --- | --- | --- |
| `surface/brand-subtle` | `--color-surface-brand-subtle` | `#EFF6FF` | Surface de marque discrète |
| `surface/default` | `--color-surface-default` | `#FFFFFF` | Surface de base |
| `surface/page` | `--color-surface-page` | `#F8FAFC` | Fond de page |
| `surface/subtle` | `--color-surface-subtle` | `#F1F5F9` | Surface secondaire |
| `text/brand` | `--color-text-brand` | `#1D4ED8` | Texte de marque |
| `text/disabled` | `--color-text-disabled` | `#94A3B8` | Texte désactivé |
| `text/inverse` | `--color-text-inverse` | `#FFFFFF` | Texte sur fond sombre ou brand |
| `text/muted` | `--color-text-muted` | `#64748B` | Texte atténué |
| `text/primary` | `--color-text-primary` | `#0F172A` | Texte principal |
| `text/secondary` | `--color-text-secondary` | `#475569` | Texte secondaire |
| `border/focus` | `--color-border-focus` | `#2563EB` | Bordure de focus |
| `border/interactive` | `--color-border-interactive` | `#64748B` | Bordure interactive |
| `border/subtle` | `--color-border-subtle` | `#E2E8F0` | Bordure discrète |
| `stroke/default` | `--stroke-default` | `1px` | Trait standard |
| `stroke/focus` | `--stroke-focus` | `2px` | Trait de focus |
| `action/disabled/background` | `--color-action-disabled-background` | `#E2E8F0` | Fond d'action désactivée |
| `action/disabled/content` | `--color-action-disabled-content` | `#64748B` | Contenu d'action désactivée |
| `action/primary/content` | `--color-action-primary-content` | `#FFFFFF` | Contenu d'action primaire |
| `action/primary/default` | `--color-action-primary-default` | `#2563EB` | Action primaire par défaut |
| `action/primary/hover` | `--color-action-primary-hover` | `#1D4ED8` | Action primaire au survol |
| `action/primary/pressed` | `--color-action-primary-pressed` | `#1E40AF` | Action primaire pressée |
| `status/cancelled/background` | `--color-status-cancelled-background` | `#FEF2F2` | Badge statut annulé, fond |
| `status/cancelled/content` | `--color-status-cancelled-content` | `#B91C1C` | Badge statut annulé, texte |
| `status/confirmed/background` | `--color-status-confirmed-background` | `#F0FDF4` | Badge statut confirmé, fond |
| `status/confirmed/content` | `--color-status-confirmed-content` | `#166534` | Badge statut confirmé, texte |
| `status/draft/background` | `--color-status-draft-background` | `#F1F5F9` | Badge statut brouillon, fond |
| `status/draft/content` | `--color-status-draft-content` | `#334155` | Badge statut brouillon, texte |
| `status/full/background` | `--color-status-full-background` | `#FFFBEB` | Badge statut complet, fond |
| `status/full/content` | `--color-status-full-content` | `#92400E` | Badge statut complet, texte |
| `feedback/error/background` | `--color-feedback-error-background` | `#FEF2F2` | Fond d'erreur |
| `feedback/error/content` | `--color-feedback-error-content` | `#B91C1C` | Texte d'erreur |
| `space/0` | `--space-0` | `0px` | Espacement |
| `space/1` | `--space-1` | `4px` | Espacement |
| `space/2` | `--space-2` | `8px` | Espacement |
| `space/3` | `--space-3` | `12px` | Espacement |
| `space/4` | `--space-4` | `16px` | Espacement |
| `space/5` | `--space-5` | `20px` | Espacement |
| `space/6` | `--space-6` | `24px` | Espacement |
| `space/8` | `--space-8` | `32px` | Espacement |
| `space/10` | `--space-10` | `40px` | Espacement |
| `space/12` | `--space-12` | `48px` | Espacement |
| `space/16` | `--space-16` | `64px` | Espacement |
| `radius/none` | `--radius-none` | `0px` | Rayon nul |
| `radius/sm` | `--radius-sm` | `6px` | Petit rayon |
| `radius/md` | `--radius-md` | `8px` | Rayon moyen |
| `radius/lg` | `--radius-lg` | `12px` | Grand rayon |
| `radius/pill` | `--radius-pill` | `999px` | Forme pilule |
| `control/height-sm` | `--control-height-sm` | `32px` | Hauteur de contrôle S |
| `control/height-md` | `--control-height-md` | `40px` | Hauteur de contrôle M |
| `control/height-lg` | `--control-height-lg` | `48px` | Hauteur de contrôle L |
| `icon/size-sm` | `--icon-size-sm` | `16px` | Icône S |
| `icon/size-md` | `--icon-size-md` | `20px` | Icône M |
| `icon/size-lg` | `--icon-size-lg` | `24px` | Icône L |
| `layout/content-max` | `--layout-content-max` | `1160px` | Largeur maximale de contenu |
| `layout/sidebar-width` | `--layout-sidebar-width` | `240px` | Largeur de navigation latérale |
