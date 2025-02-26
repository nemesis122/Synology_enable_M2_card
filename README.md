# Synology enable M2 card

<a href="https://github.com/007revad/Synology_enable_M2_card/releases"><img src="https://img.shields.io/github/release/007revad/Synology_enable_M2_card.svg"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2F007revad%2FSynology_enable_M2_card&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=views&edge_flat=false"/></a>
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/007revad)
[![committers.top badge](https://user-badge.committers.top/australia/007revad.svg)](https://user-badge.committers.top/australia/007revad)

### Description

Enable Synology M.2 PCIe cards in Synology NAS that don't officially support them

Allows using E10M20-T1, M2D20, M2D18 or M2D17 cards in Synology NAS models that aren't on their [supported model list](https://github.com/007revad/Synology_enable_M2_volume/wiki/Models-that-support-PCIe-M.2-cards).

  - Enables E10M20-T1, M2D20, M2D18 or M2D17 for DS1821+, DS1621+.
  - Enables M2D18 and M2D17 for DS1823xs+, DS2422+, RS2423+, RS2421+, RS2421RP+, RS2821RP+.
  - Enables M2D18 and M2D17 for RS822RP+, RS822+, RS1221RP+ and RS1221+ using DSM 7.1.1 and older.
  - Enables E10M20-T1, M2D20, M2D18 and M2D17 for other models  with a PCIe x8 slot.

[Synology HDD db](https://github.com/007revad/Synology_HDD_db) now enables using Storage Manager to create volumes on M.2 drives in a PCIe M.2 adaptor card.

<br>

## Which Synology models will this work on

</br>**Works on the following models:**

<details>
  <summary>Click here to see list</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS1821+   | yes | yes | yes | yes | |
| DS1621+   | yes | yes | yes | yes | |
| DS1823xs+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| DS2422+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2423+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2423RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2421+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2421RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2821RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS822+    | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS822RP+  | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS1221+   | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS1221RP+ | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| **others** | yes | yes | yes | yes | The NAS must have a PCIe x8 slot |

</details>

</br>**Should work for the following models but I have not tested them:**

<details>
  <summary>Click here to see list</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| FS2500    | yes | yes | yes | yes | |
| FS3410    | yes | yes | yes | yes | |
| FS6400    | yes | yes | yes | yes | |
| HD6500    | yes | yes | yes | yes | |
| SA4310    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| SA3610    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| SA6400    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |

</details>

</br>**Synology NAS models that this script may work on?**

<details>
  <summary>Click here to see list</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS1623xs+ | ???  | ??? | ???  | ??? |  |
| DS1817+   | ???  | ??? | ???  | ??? | M2D18 SATA already enabled in DSM |
| DS1517+   | ???  | ??? | ???  | ??? | M2D18 SATA already enabled in DSM |
| RS1219+   | ???  | ??? | ???  | ??? | M2D18 SATA already enabled in DSM |
| RS818+    | ???  | ??? | ???  | ??? | M2D18 SATA already enabled in DSM |
| RS818RP+  | ???  | ??? | ???  | ??? | M2D18 SATA already enabled in DSM |

</details>

</br>**Synology NAS models that this script won't work on:**

<details>
  <summary>Click here to see list</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS923+    | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| DS723+    | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| DS1522+   | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| RS422+    | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |

</details>

<br>

## How to run the script

### Download the script

1. Download the latest version _Source code (zip)_ from https://github.com/007revad/Synology_enable_M2_card/releases
2. Save the download zip file to a folder on the Synology.
    - Do ***NOT*** save the script to a M.2 volume. After a DSM or Storage Manager update the M.2 volume won't be available until after the script has run.
3. Unzip the zip file.

### Running the script via SSH

[How to enable SSH and login to DSM via SSH](https://kb.synology.com/en-global/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet)

**Note:** Replace /volume1/scripts/ with the path to where the script is located.
Run the script then reboot the Synology:
```YAML
sudo -s /volume1/scripts/syno_enable_m2_card.sh
```

**Options:**
```YAML
  -c, --check           Check M.2 card status
  -r, --restore         Restore from backups to undo changes
  -e, --email           Disable colored text in output scheduler emails.
      --autoupdate=AGE  Auto update script (useful when script is scheduled)
                        AGE is how many days old a release must be before
                        auto-updating. AGE must be a number: 0 or greater
      --model=CARD      Automatically enable specified card model
                        Required if you want to schedule the script
                        CARD can be E10M20-T1, M2D20, M2D18 or M2D17
  -h, --help            Show this help message
  -v, --version         Show the script version
```

### What about DSM updates?

After any DSM update you will need to run this script again. 

### Schedule the script to run at shutdown

Or you can schedule Synology_enable_M2_card to run when the Synology shuts down, to avoid having to remember to run the script after a DSM update.

See <a href=how_to_schedule.md/>How to schedule a script in Synology Task Scheduler</a>

</br>

## Screenshots

<p align="center">Available options</p>
<p align="center"><img src="/images/help.png"></p>

<p align="center">Enabling all M.2 card models</p>
<p align="center"><img src="/images/edited.png"></p>

<p align="center">Checking the current M.2 card settings</p>
<p align="center"><img src="/images/check.png"></p>

<p align="center">E10M20-T1 already enabled</p>
<p align="center"><img src="/images/e10m20.png"></p>

<p align="center">All M.2 card models already enabled</p>
<p align="center"><img src="/images/all.png"></p>

<p align="center">Restoring the original M.2 card settings</p>
<p align="center"><img src="/images/restore.png"></p>
