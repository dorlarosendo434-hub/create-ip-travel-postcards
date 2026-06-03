# create-ip-travel-postcards

Codex skill for creating a coordinated front-and-back cultural tourism postcard series that combines a user-provided IP character with a destination and season.

## Install In Codex

Install from this GitHub repository with the skill path:

```powershell
python -X utf8 "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --repo dorlarosendo434-hub/create-ip-travel-postcards `
  --path create-ip-travel-postcards
```

Restart Codex after installation.

## Use

Invoke the skill with:

```text
Use $create-ip-travel-postcards to generate a front-and-back travel postcard sample for my IP character and destination.
```

Required inputs:

- IP character reference image
- destination name and location
- recommended month
- 2-5 destination keywords

Optional inputs:

- IP nickname
- four-line poem
- approved front/back image from the same series for style anchoring

## Package

A distributable ZIP is included at:

```text
dist/create-ip-travel-postcards.zip
```

