# Thunderbird Git Migration

The `git-migration` script was used to perform the initial population of the
[thunderbird-desktop](https://github.com/thunderbird/thunderbird-desktop)
branches and tags.

The `final-push` script was then used to update the branches and tags of
[thunderbird-desktop](https://github.com/thunderbird/thunderbird-desktop) with
any new commits and tags since the last update (meaning the last run of
`git-migration` or `final-push`).

## Populating a new branch

To populate a new branch, for example `comm-esr153` for the upcoming esr,
update `BOOKMARKS` to only include the new branch name and then run:

```sh
./git-migration \
  --github-url https://github.com/thunderbird/thunderbird-desktop \
  --include-cvs-history \
  --push
```
