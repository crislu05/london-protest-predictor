# Git history author rewrite (MLH S6)

One-time maintenance so GitHub attributes commits to verified humans (no `you@example.com`, no separate Claude/Cursor contributor entries).

```bash
pip install git-filter-repo
git filter-repo --mailmap tooling/history-mailmap \
  --replace-message tooling/history-message-replacements.txt \
  --force
git remote add london https://github.com/crislu05/london-protest-predictor.git
git push --force london main
```

Teammate commits (Jakub, Mykhailo) are unchanged. Only `cl5924` and `Claude` author lines map to `crislu05`.
