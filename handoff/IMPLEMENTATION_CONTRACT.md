# Kital PRO Implementation Contract

## Principle

Figma component names, state axes and semantic token roles should map naturally to engineering concepts. The design file is visual authority; this document captures behavior that cannot be inferred safely from a screenshot alone.

## Forms

- Persistent labels; placeholders do not replace labels.
- Required state remains explicit.
- Error/helper copy expands layout vertically.
- Do not place dynamic field content inside rigid fixed-height wrappers.
- Error meaning is not communicated by color alone.
- Disabled controls are non-interactive and visually distinct.

Suggested mappings:

```text
Input/Text      → <TextField />
Input/Password  → <PasswordField />
Input/Date      → <DateField />
Select/Field    → <SelectField />
Input/Textarea  → <TextArea />
```

## Actions

```text
Button/Primary     → <Button variant="primary" />
Button/Secondary   → <Button variant="secondary" />
Button/Tertiary    → <Button variant="tertiary" />
Button/Destructive → <Button variant="destructive" />
```

- Loading blocks repeat submission.
- Disabled does not fire actions.
- Focus remains visible.
- S/M/L sizing is explicit; do not derive arbitrary heights per screen.

## Upload

```text
Upload/Dropzone
  State = Locked | Empty | Uploading | Reviewing | Reviewed
  Viewport = Desktop | Mobile
```

Production state changes must come from real runtime/server events. The portfolio prototype uses fixed timeouts only to demonstrate the processing sequence.

The outer Upload/Dropzone owns workflow actions. Upload/FileRow owns file identity/status/progress, not unrelated page actions.

## Responsive

- Do not scale the 1920 desktop composition.
- Onboarding sidebar becomes a progress header in the mobile reference.
- Multi-column forms stack.
- Drawers become full-width mobile sheets.
- Primary actions may become full-width.
- Long copy wraps and increases height.
- Mobile pages are expected to scroll vertically.

## Dialogs

- Use dialog semantics appropriate to message/success/destructive confirmation.
- Trap focus while modal.
- Restore focus on close.
- Escape behavior is defined for dismissible dialogs.
- Destructive initial focus should avoid accidental confirmation.
- Close controls require explicit accessible names.

## Permissions

`Permissions/RoleRow` state owns role semantics; do not expose a combination that allows an Administrator label with Auxiliary behavior.

Observed role model in the source:

- Administrator — broad/full platform access.
- Auxiliary — operational support.
- Unit Responsible — restricted segment/unit access.

## Filters

Desktop: right-side 403px drawer.
Mobile: full-width 390px reference sheet.

Modes:

- Applied
- Locations
- Departments

Filter chips wrap. Range controls remain grouped with their labels and enable/disable switch.

## Accessibility

- Visible focus.
- Keyboard operation.
- Practical 44px target for small controls where appropriate.
- Persistent labels.
- Error identification/recovery.
- Content/zoom resilience.
- Dialog focus management.

## Source integrity

Historical source remains immutable evidence. When implementing from PRO, consult `99 — SOURCE REFERENCE` if a product decision appears ambiguous. New behavior introduced retrospectively is labeled as a PRO extension rather than historical fact.
