# Issue Board Homebrew tap

Public macOS tap for [Issue Board](https://github.com/danickfort/issue-board), a terminal issue board for YouTrack, GitLab and Jira Cloud.

```sh
brew install danickfort/issueboard/issueboard
issueboard
```

No GitHub login or token is needed. Alternatively, run `brew tap danickfort/issueboard`, then `brew install issueboard`.

If the older standalone formulas are installed, first run `brew uninstall youtrack-board gitlab-board`. Saved preferences and credentials are preserved. Issue Board installs `issueboard`, `youtrack-board`, `gitlab-board` and `jira-board`.

Run `issueboard` in a project folder to choose its tracker and board. Try `issueboard --demo youtrack`, `issueboard --demo gitlab` or `issueboard --demo jira` offline. YouTrack and Jira tokens stay in the OS keychain. GitLab boards require `glab` (`brew install glab`) and its own sign-in.

```sh
brew update
brew upgrade danickfort/issueboard/issueboard
brew test danickfort/issueboard/issueboard
brew uninstall issueboard
```

The formula downloads the public source release into an isolated Python environment and checks SHA-256 hashes for the source and dependency resources. The installation workflow checks the public tap on macOS with `brew install` and `brew test`.

Linux users can download the standalone archive from [releases](https://github.com/danickfort/issue-board/releases); see the [installation instructions](https://github.com/danickfort/issue-board#installation). The formula currently supports macOS.
