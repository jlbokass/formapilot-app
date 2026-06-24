# Figma Components

Ces correspondances sont prévues pour FormaPilot UI `0.1.0`. Les chemins React ci-dessous ne sont pas encore implémentés.

| Figma component | Planned React path |
| --- | --- |
| `Button` | `src/components/ui/Button.tsx` |
| `TextField` | `src/components/ui/TextField.tsx` |
| `Select` | `src/components/ui/Select.tsx` |
| `StatusBadge` | `src/components/ui/StatusBadge.tsx` |
| `NavItem` | `src/components/navigation/NavItem.tsx` |
| `EmptyState` | `src/components/ui/EmptyState.tsx` |
| `SessionRow` | `src/features/sessions/SessionRow.tsx` |
| `SessionCard` | `src/features/sessions/SessionCard.tsx` |

## Button

- Figma node: `Button` (`COMPONENT_SET`, `73:244`)
- Variants: `Type=Primary|Secondary|Ghost`, `Size=M|L`, `State=Default|Hover|Pressed|Focus|Disabled`
- Figma properties: `Label`, `Show leading icon`, `Leading icon`, `Show trailing icon`, `Trailing icon`, `Loading`, `Type`, `Size`, `State`
- Future TypeScript props: `children`, `type`, `size`, `state`, `leadingIcon`, `trailingIcon`, `loading`, `disabled`
- Nested components/layers: `Leading icon`, `Trailing icon`, `Loading indicator`, `Label`
- Main tokens: `action/primary/default`, `action/primary/hover`, `action/primary/pressed`, `action/primary/content`, `action/disabled/background`, `action/disabled/content`, `border/focus`, `border/interactive`, `control/height-md`, `control/height-lg`, `icon/size-md`, `radius/md`, `radius/sm`, `stroke/default`, `stroke/focus`, `surface/default`, `surface/subtle`, `surface/brand-subtle`, `text/primary`, `text/brand`

## TextField

- Figma node: `TextField` (`COMPONENT_SET`, `82:503`)
- Variants: `State=Default|Focus|Filled|Error|Disabled|State6`
- Figma properties: `Label`, `Value`, `Placeholder`, `Helper text`, `Error message`, `Show helper`, `Required`, `State`
- Future TypeScript props: `label`, `value`, `placeholder`, `helperText`, `errorMessage`, `showHelper`, `required`, `state`, `disabled`
- Nested components/layers: `Label row`, `Control`, `Label`, `Required marker`, `Placeholder`, `Value`, `Helper text`, `Error message`
- Main tokens: `surface/default`, `border/interactive`, `border/focus`, `feedback/error/content`, `stroke/default`, `stroke/focus`, `radius/md`, `space/1`, `space/2`, `space/4`, `text/primary`, `text/secondary`, `text/muted`, `text/disabled`
- Note: `State6` is present in Figma and is documented as-is until renamed or removed in Figma.

## Select

- Figma node: `Select` (`COMPONENT_SET`, `82:559`)
- Variants: `State=Default|Focus|Filled|Error|Disabled`
- Figma properties: `Label`, `Selected value`, `Placeholder`, `Helper text`, `Error message`, `Show helper`, `Required`, `State`
- Future TypeScript props: `label`, `value`, `placeholder`, `helperText`, `errorMessage`, `showHelper`, `required`, `state`, `disabled`, `options`
- Nested components/layers: `Label row`, `Control`, `Chevron icon`, `Label`, `Required marker`, `Selected value`, `Placeholder`, `Helper text`, `Error message`
- Main tokens: `surface/default`, `border/interactive`, `border/focus`, `feedback/error/content`, `icon/size-md`, `stroke/default`, `stroke/focus`, `radius/md`, `radius/sm`, `space/1`, `space/2`, `space/3`, `space/4`, `text/primary`, `text/secondary`, `text/muted`, `text/disabled`

## StatusBadge

- Figma node: `StatusBadge` (`COMPONENT_SET`, `82:568`)
- Variants: `Status=Draft|Confirmed|Full|Cancelled`
- Figma properties: `Label`, `Status`
- Future TypeScript props: `status`, `children`
- Nested components/layers: `Label`
- Main tokens: `status/draft/background`, `status/draft/content`, `status/confirmed/background`, `status/confirmed/content`, `status/full/background`, `status/full/content`, `status/cancelled/background`, `status/cancelled/content`, `radius/md`, `space/1`, `space/2`

## NavItem

- Figma node: `NavItem` (`COMPONENT_SET`, `82:581`)
- Variants: `State=Default|Hover|Active`
- Figma properties: `Label`, `Show icon`, `Icon`, `State`
- Future TypeScript props: `label`, `href`, `icon`, `showIcon`, `state`, `active`
- Nested components/layers: `Icon`, `Active indicator`, `Label`
- Main tokens: `surface/default`, `surface/subtle`, `surface/brand-subtle`, `text/primary`, `text/secondary`, `text/brand`, `border/focus`, `control/height-md`, `icon/size-md`, `radius/md`, `radius/sm`, `stroke/default`, `stroke/focus`, `space/2`, `space/3`, `space/4`

## EmptyState

- Figma node: `EmptyState` (`COMPONENT_SET`, `82:611`)
- Variants: `Variant=Default`
- Figma properties: `Title`, `Description`, `Show icon`, `Show primary action`, `Show secondary action`, `Variant`
- Future TypeScript props: `title`, `description`, `icon`, `primaryAction`, `secondaryAction`, `showIcon`, `showPrimaryAction`, `showSecondaryAction`
- Nested components/layers: `Icon`, `Actions`, `Primary action`, `Secondary action`, `Title`, `Description`
- Main tokens: `surface/default`, `border/subtle`, `border/interactive`, `action/primary/default`, `action/primary/content`, `control/height-md`, `icon/size-md`, `radius/md`, `radius/sm`, `stroke/default`, `space/2`, `space/3`, `space/4`, `space/6`, `space/8`, `text/primary`, `text/secondary`

## SessionRow

- Figma node: `SessionRow` (`COMPONENT`, `96:386`)
- Variants: none
- Figma properties: `Title`, `Date`, `Format`, `Participants`, `Status`
- Future TypeScript props: `title`, `date`, `format`, `participants`, `status`
- Nested components/layers: `Status badge`, `Title`, `Date`, `Format`, `Participants`
- Main tokens: `border/subtle`, `stroke/default`, `radius/md`, `space/1`, `space/2`, `space/4`, `text/primary`, `text/secondary`, `status/confirmed/background`, `status/confirmed/content`

## SessionCard

- Figma node: `SessionCard` (`COMPONENT`, `96:393`)
- Variants: none
- Figma properties: `Title`, `Date`, `Format`, `Participants`, `Status`
- Future TypeScript props: `title`, `date`, `format`, `participants`, `status`
- Nested components/layers: `Header`, `Details`, `Status badge`, `Date`, `Format`, `Participants`, `Title`
- Main tokens: `surface/default`, `border/subtle`, `stroke/default`, `radius/lg`, `radius/md`, `space/1`, `space/2`, `space/3`, `space/4`, `text/primary`, `text/secondary`, `text/muted`, `status/confirmed/background`, `status/confirmed/content`
