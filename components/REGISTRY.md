# Kital PRO Component Registry

Snapshot from Figma PRO file `MB4whc6pDTocrQfwv7c92I` after duplicate invitation-set cleanup.

## Actions

| Component | Variants | API summary |
| --- | ---: | --- |
| Button/Primary | 18 | Size S/M/L × Default/Hover/Pressed/Focus/Disabled/Loading; Label; optional leading/trailing icon via BOOLEAN + INSTANCE_SWAP |
| Button/Secondary | 18 | Same API as Primary |
| Button/Tertiary | 15 | Size S/M/L × Default/Hover/Pressed/Focus/Disabled |
| Button/Destructive | 18 | Same core API as Primary; source destructive tone |
| Action/CompactPill | 8 | Tone Neutral/Destructive × state; Label |
| Upload/FilePickerAction | 4 | Default/Hover/Focus/Disabled; Label |
| Setup/ResourceAction | 4 | Kind Video/Download × Default/Disabled |

## Forms

| Component | Variants | API summary |
| --- | ---: | --- |
| Input/Text | 6 | Default/Filled/Hover/Focus/Error/Disabled; Label, Required, Placeholder, Value, Helper, Show helper |
| Input/Email | 5 | Default/Filled/Focus/Error/Disabled |
| Input/Password | 15 | Mode Empty/Masked/Visible × Default/Hover/Focus/Error/Disabled; label/value/helper and reveal behavior |
| Input/AccessCode | 3 | Default/Error/Blocked |
| Input/Date | 5 | Default/Filled/Focus/Error/Disabled; Label |
| Input/Textarea | 4 | Default/Focus/Error/Disabled; Value |
| Select/Field | 7 | Default/Filled/Hover/Focus/Open/Error/Disabled; Label, Required, Placeholder, Value, Helper |
| Select/MenuItem | 4 | Default/Hover/Selected/Disabled; Label; optional leading icon |
| Checkbox/Control | 8 | Selected False/True × Default/Hover/Focus/Disabled |
| Toggle/Control | 8 | On False/True × Default/Hover/Focus/Disabled |

## Navigation / setup

| Component | Variants | API summary |
| --- | ---: | --- |
| Onboarding/ProgressNav | 8 | Current Account/Workspace/Invite/Survey × Desktop/Mobile |
| Setup/StepBadge | 2 | Active/Disabled; Number |
| SocialAuth/Button | 10 | Google/Facebook × Default/Hover/Pressed/Focus/Disabled |
| Password/Requirement | 3 | Met/Neutral/Error; Label |

## Invitation lifecycle

| Component | Variants | API summary |
| --- | ---: | --- |
| Invitation/StatusAction | 4 | Draft/Sent/Failed/Accepted |
| Invitation/Row | 10 | Draft/Sent/Failed/Accepted/ValidationError × Desktop/Mobile |

The active Invitation set is the one used by Product/Patterns. A later unused duplicate set was removed after dependency verification.

## Upload / processing

| Component | Variants | API summary |
| --- | ---: | --- |
| Progress/Linear | 10 | Value 25/50/60/75/100 × Desktop/Mobile |
| Upload/FileRow | 4 | Uploading/Complete × Desktop/Mobile; Filename + Meta |
| Upload/Dropzone | 10 | Locked/Empty/Uploading/Reviewing/Reviewed × Desktop/Mobile |
| Icon/CloudUpload | 2 | Default/Muted |

## Workspace / brand

| Component | Variants | API summary |
| --- | ---: | --- |
| Workspace/BrandCard | 4 | Type Colors/Logo × Ready/Invalid |

## Feedback / permissions

| Component | Variants | API summary |
| --- | ---: | --- |
| Modal/Feedback | 6 | Type Message/Success/Destructive × Desktop/Mobile; Title + Body |
| Permissions/RoleRow | 3 | Off/On/Disabled; State owns role semantics |
| Modal/RolesPermissions | 2 | Desktop/Mobile |

## Filters

| Component | Variants | API summary |
| --- | ---: | --- |
| Chip/Filter | 2 | Default/Selected; Label |
| Filter/Chip | 8 | Selected × Default/Hover/Focus/Disabled; Label |
| Filter/GroupHeader | 2 | Expanded True/False; Title |
| Filter/RangeSlider | 4 | Enabled/Disabled × Desktop/Mobile; Label/Min/Max |
| Filter/Section | 4 | Type Chips/Range × Enabled/Disabled; Title |
| Drawer/Filters | 6 | Mode Applied/Locations/Departments × Desktop/Mobile |

## Component design rules

- Product identity/source appearance is authoritative.
- TEXT / BOOLEAN / INSTANCE_SWAP are preferred over unnecessary variant multiplication.
- Error/helper content may increase component height.
- Mobile variants exist only where behavior/geometry meaningfully changes.
- States introduced retrospectively are documented as PRO extensions when not observed historically.
- No generic component is added only to make the design-system inventory look larger.
