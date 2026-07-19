# setup-hadolint action

easy way to install [hadolint](https://github.com/hadolint/hadolint) in your GitHub Actions
workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-hadolint@LATEST_RELEASE_TAG
```

if you don't want to use the default version of hadolint that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-hadolint@LATEST_RELEASE_TAG
  with:
    version: '2.14.0'
    checksum: '6bf226944684f56c84dd014e8b979d27425c0148f61b3bd99bcc6f39e9dc5a47'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
