# Issue Board Homebrew tap

Private macOS tap for [Issue Board](https://github.com/danickfort/issue-board), a terminal board for YouTrack and GitLab. The tap is `danickfort/homebrew-issueboard`. Your GitHub account needs access to both repositories.

```sh
gh auth login
gh auth setup-git
HOMEBREW_GITHUB_API_TOKEN="$(gh auth token)" brew install danickfort/issueboard/issueboard
```

If the standalone formulas are installed, first run `brew uninstall youtrack-board gitlab-board`. Saved preferences and credentials are preserved. Issue Board installs `issueboard`, `youtrack-board`, and `gitlab-board`.

Run `issueboard` in a project folder to choose its tracker and board. Try `issueboard --demo youtrack` or `issueboard --demo gitlab` offline. YouTrack tokens stay in the OS keychain. GitLab boards require `glab` (`brew install glab`) and its own sign-in.

Update with `brew update`, then `HOMEBREW_GITHUB_API_TOKEN="$(gh auth token)" brew upgrade danickfort/issueboard/issueboard`.

Verify the installed demos with `brew test danickfort/issueboard/issueboard`.

The formula pins the source release tag and full Git commit, and checksums its Python dependency resources. Source archives and checksums are also available from the private [releases](https://github.com/danickfort/issue-board/releases). GitHub credentials are supplied through the environment and are never stored in the formula.
