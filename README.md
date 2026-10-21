# Independent AltStore build

This repository holds a manually triggered GitHub Actions workflow that compiles pinned, reviewed public AltStore source on a standard GitHub-hosted macOS runner. It does not sign or install apps, submit Apple account credentials, or contain device-specific signing material.

Source: [liuzhe1117/AltStore at 31972b5eb79a9df5badf25a0c073a033c7770db4](https://github.com/liuzhe1117/AltStore/tree/31972b5eb79a9df5badf25a0c073a033c7770db4), an unofficial fork of [AltStore](https://github.com/altstoreio/AltStore). The authentication dependency is pinned to [020ddb5691ffb9b75dfdd92b83a6809bbfdd1d5b](https://github.com/liuzhe1117/AltSign/tree/020ddb5691ffb9b75dfdd92b83a6809bbfdd1d5b).

Run **Actions → Build reviewed AltStore source → Run workflow**. The workflow uses the standard `xcode-27` runner and skips private repositories. [Standard hosted runners are free for public repositories](https://docs.github.com/en/actions/reference/runners/github-hosted-runners). Artifacts expire after one day.

Successful output includes an unsigned IPA, its SHA-256, the exact source and workflow commits, dependency revisions, build environment and logs. The output is an independent compilation; a successful build does not establish that every source dependency is safe or that Apple authentication will succeed.

Signing with the device owner's existing certificate is a separate local step. Do not add Apple passwords, certificates, signing passwords, provisioning profiles, device-pairing files or personal diagnostic reports to this repository or its Actions secrets.

AltStore is licensed under AGPLv3 with the permissions and dependency notices documented in its [source README](https://github.com/liuzhe1117/AltStore/blob/31972b5eb79a9df5badf25a0c073a033c7770db4/README.md) and [license](https://github.com/liuzhe1117/AltStore/blob/31972b5eb79a9df5badf25a0c073a033c7770db4/LICENSE).
