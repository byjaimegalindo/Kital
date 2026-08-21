# Kital PRO Golden-Path Prototype

The prototype is wired on real top-level Product screens in the PRO Figma file, not only represented as a diagram.

## Desktop path

| Step | Source control / state | Destination |
| ---: | --- | --- |
| 1 | Welcome · Confirmar Contraseña | Create Account |
| 2 | Create Account · Crear cuenta en Kital | Invite Users |
| 3 | Invite Users · Guardar y Continuar | Workspace |
| 4 | Workspace · Guardar y Continuar | Upload Collaborators · Locked |
| 5 | Locked · Ver Video Tutorial | Upload Collaborators · Empty/Ready |
| 6 | Empty · Seleccionar Archivo | Uploading |
| 7 | Uploading | Reviewing after 1.2s prototype timeout |
| 8 | Reviewing | Reviewed after 1.2s prototype timeout |
| 9 | Reviewed · Guardar y Continuar | First Measurement |
| 10 | First Measurement · Guardar y Continuar | Success |

Navigation uses short Smart Animate transitions where continuity adds value.

## Production caveat

The 1.2s Uploading/Reviewing transitions are **portfolio prototype simulation only**. Production must transition on actual upload/validation/runtime events.

## Unhappy paths represented in the system

- Invalid access code → Welcome / Error.
- Repeated access failure → Welcome / Blocked.
- Account validation → Create Account / Validation Error.
- Invitation send failure → Invitation/Row Failed + `Reintentar`.
- Upload error → Error feedback dialog.
- Upload/delete action → Destructive confirmation.
- First Measurement missing/invalid inputs → Validation Error.

## Interaction contract

- Disabled states do not navigate.
- Loading prevents repeat submission.
- Dialog close restores focus.
- Destructive confirmation remains explicit.
- Keyboard/focus behavior is documented in the Accessibility page.

## Figma screen IDs

- Welcome: `85:2066`
- Create Account: `81:1708`
- Invite Users: `70:995`
- Workspace: `86:2179`
- Upload Locked: `75:1111`
- Upload Empty: `75:1183`
- Uploading: `75:1251`
- Reviewing: `75:1333`
- Reviewed: `75:1430`
- First Measurement: `88:2336`
- Success: `96:2218`
