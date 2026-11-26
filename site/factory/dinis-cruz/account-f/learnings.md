# cl-6.correspondent: learnings

- A fresh container has no openssh-client: `apt-get update` first, then install it, or `ssh-keygen` is missing.
- `git log --show-signature` prints "No signature" without gpg.ssh.allowedSignersFile; check with `git cat-file commit HEAD | grep 'BEGIN SSH SIGNATURE'`.
- release.sh may report "no release contains it after 6 minutes" when deploy-pages is queued: the push still went in.
- The website's board/keys.json is `{about, keys: [...]}`; fingerprints are the first 16 hex of SHA-256 over the public key's DER.
