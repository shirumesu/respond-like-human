# Installing Respond-like-human for Agent

## Installation

1. Download the [latest packaged archive](https://github.com/shirumesu/respond-like-human/releases/latest/download/respond-like-human.zip) for this skill when one is available. If you are installing directly from the repository, copy the files from the repository instead.
2. If you are using the packaged archive, extract it directly into the directory your agent scans for installed skills. The archive already contains the `respond-like-human/` root folder, so do not create another nested folder first.
3. If you are installing manually from the repository, create a folder named `respond-like-human` inside the skills directory and copy the skill files into it.
4. Confirm that `SKILL.md` ends up at the root of the installed skill directory.

A full install can look like this:

```text
<skills-dir>/
  respond-like-human/
    SKILL.md
    agents/
      openai.yaml
```

If you want the smallest working install, this is enough:

```text
<skills-dir>/
  respond-like-human/
    SKILL.md
```

## When finish

Once you confirm that `SKILL.md` is in the skill root, the installation is complete.

If the current host is not Codex, check whether `agents/openai.yaml` is still present. Tell the user that it is a Codex-specific descriptor file and ask whether they want it removed. If they say yes, delete it. If they say no, leave it in place. In both cases, tell the user that the installation is complete and that only a restart is still required.

## Updating

Replace the existing `respond-like-human` folder with a newer package, or overwrite the files you installed manually.

If you made local edits, back them up before replacing files.

After updating, restart your agent so it loads the new version.

## Troubleshooting

- If the skill is not detected, check that the final path is `<skills-dir>/respond-like-human/SKILL.md`, not an extra nested path such as `<skills-dir>/respond-like-human/respond-like-human/SKILL.md`.
- If the old behavior is still active, fully restart the host instead of only opening a new chat inside the same running process.
- If your host reports an error on `agents/openai.yaml`, delete that file and restart.
- If you installed only `SKILL.md` and expected bundled docs or descriptors, copy the remaining files you want from the repository and restart.
