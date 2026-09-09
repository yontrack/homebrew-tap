Yontrack tap
============

The Homebrew tap for the [Yontrack CLI](https://github.com/yontrack/yontrack-cli).

```bash
brew install yontrack/tap/yontrack
```

Homebrew 6 asks that third-party taps be trusted before it loads them. If it
says this tap is not trusted:

```bash
brew trust --formula yontrack/tap/yontrack
```

## The formula is generated

`Formula/yontrack.rb` is rendered by `homebrew_formula.sh` in
[yontrack/yontrack-cli](https://github.com/yontrack/yontrack-cli) and pushed
here by that repository's release workflow, on every tag. Editing it here
achieves nothing: the next release overwrites it. Change the generator.

It installs the binary published with the GitHub release and pins its sha256
rather than building from source. The reasoning is recorded in
[ADR 0002](https://github.com/yontrack/yontrack-cli/blob/main/docs/adr/0002-homebrew-ships-the-release-binary.md).

Anything about the CLI itself belongs in
[its issues](https://github.com/yontrack/yontrack-cli/issues), not here.
