![](assets/banner.png)

![Python minimum version](https://img.shields.io/badge/Python-3.10%2B-brightgreen)

# Description

GitFive is an OSINT tool to investigate GitHub profiles.

Main features :
- Usernames / names history
- Usernames / names variations
- Email address to GitHub account
- Find GitHub's accounts from a list of email addresses
- Lists identities used by the target
- Clones and analyze every target's repos
- Highlights emails tied to GitHub's target account
- Finds local identities (UPNs, ex : jeanpierre@My-Computer.local)
- Finds potential secondary GitHub accounts
- Don't needs repos to work (but better)
- Generates every possible email address combinations and looks for matchs
- Dumps SSL public keys
- JSON export

Optimizations :
- Very low API consumption, stays under the rate-limit
- Multi-processing tasks (bypassing Python's GIL)
- Async scraping

# Workflow
**Click [here](https://user-images.githubusercontent.com/17338428/194182901-b062b2cf-c02c-40f0-854a-5f3c52031271.png) for a full view**

<br>

![](assets/workflow.png)

# Requirements
- Git
- Python >= 3.10

# Installation

```bash
$ pip3 install pipx
$ pipx ensurepath
$ pipx install gitfive
```
It will automatically use venvs to avoid dependency conflicts with other projects.

# Usage
First, login to GitHub :
```bash
$ gitfive login
```

*How to create the token : https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token \
Only "repo" and "delete_repo" scopes are needed.*

Then, profit :
```bash
usage: gitfive [-h] {login,user,email,emails,light} ...

positional arguments:
  {login,user,email,emails,light}
    login               Let GitFive authenticate to GitHub.
    user                Track down a GitHub user by its username.
    email               Track down a GitHub user by its email address.
    emails              Find GitHub usernames of a given list of email addresses.
    light               Quickly find emails addresses from a GitHub username.

options:
  -h, --help            show this help message and exit
```


*PS : plz avoid testing on torvalds or other authors of repos with 1 million commits*

**Have fun 🥰💞**

## Video demo

https://user-images.githubusercontent.com/17338428/194177613-6678034a-4c8c-4240-a638-3e9aecd1904d.mp4

## Obvious disclaimer

This tool is for educational purposes only, I am not responsible for its use.

### Less obvious disclaimer

The use of this tool in a paid service is strictly forbidden without my personal agreement.\
Please use it only in personal, criminal investigations, or open-source projects.

## Thanks

- novitae for being my Python colleague
- rayanlecat, ABH, 22sh, BlackWasp, Tartofraise, mpgn, M3SS for the beta test
- The HideAndSec team 💗 (blog : https://hideandsec.sh)

## You like the tool ?
[Sponsor me](https://github.com/sponsors/mxrch) on GitHub !
