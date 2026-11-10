# PPT Master Skill

This repository vendors the upstream [PPT Master](https://github.com/hugohe3/ppt-master) skill as a pinned Git submodule.

## Get the skill files

Clone this repository with its submodule:

```bash
git clone --recurse-submodules https://github.com/z64200928-byte/111.git
cd 111
```

If you already cloned it without submodules:

```bash
git submodule update --init --recursive
```

The skill is exposed at `skills/ppt-master` (a symlink to `vendor/ppt-master-upstream/skills/ppt-master`). The upstream source is pinned to commit `3c6ffd0ee6d6e31aa9ca316bd157173802e3526f`.

## Install dependencies

PPT Master requires Python 3.10–3.14. From the repository root, install the upstream project requirements:

```bash
python3 -m pip install -r vendor/ppt-master-upstream/requirements.txt
```

Use an agent host that can read/write files and execute shell commands, and open this repository as its working folder. Follow `skills/ppt-master/SKILL.md` for the required workflow and configuration. Configure any provider API keys only in your local environment or an untracked `.env` file; never commit secrets.

## Update the upstream skill

```bash
git submodule update --remote --merge
```

Review and commit the updated submodule pointer after updating.
