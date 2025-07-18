# Data for Minecraft: Java Edition

This folder only records **cheaters/spammers**

So **DON'T** commit anyone for violation of rules in **your server**

## Reporting

Open an issue [here](https://github.com/blackwallmc/data/issues)

## Directory schema

```
|- offline
    |- a
        |- anyone.json
    |- b
    |- c
    |- ...
    |- u
        |- username.json
    |- ...
|- online
    |- 1a
        |- <uuid>.json
    |- 1b
    |- 1c
    |- ...
```

- Identify offline players by IGN
    - First character as directory name
    - Player name in **short case** as file name
- Identify online players by UUID
    - Pre 2 characters as directory name
    - **Trimmed UUID** as file name
    - Get UUID in your server console, information commands and [MCUUID](https://mcuuid.net/)

## File schema
```json
{
    "firstCommit": "yyyy/MM/dd",
    "lastCommit": "yyyy/MM/dd",
    "record": {
        "SPAMMING": 0,
        "CHEATING": 0
    },
    "records": [
        {
            "source": "Source server IP (where this happened, no further update needed)",
            "reason": "Short description for this event",
            "type": "SEE BELOW"
        }
    ]
}
```
- `firstCommit` Date of first commit for this player
- `lastCommit` Date of last commit for this player
- `record` Successful reports counters
    - `SPAMMING`
    - `CHEATING`
- `records` Latest 5 records
    - `source` Where this happened
    - `reason` Short description
    - `type` Record type, see keys in `record`
