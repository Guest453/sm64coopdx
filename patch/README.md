# patch slot

Drop a unified diff at `patch/current.patch` and the `Build Windows x64`
workflow will run `git apply --verbose patch/current.patch` before `make`.

If the file is absent the build runs pristine.

Generate the patch from a clean checkout of the same upstream commit, e.g.:

```
git diff > current.patch
```

Keep it a normal `git apply`-able diff (paths relative to the repo root).
