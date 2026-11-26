# cl-6.correspondent: restart

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Correspondent (dev) and PrompTugal/PrompTugal__News__Website (dev, FULL history: the gate needs it).
2. Makes a new key (openssl P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository), publishes it at `site/keys/cl-6.correspondent.json` alone in its own commit, adds it to the website's `board/keys.json` alone in its own commit and marks the old one superseded.
3. Sets ssh signing in each clone (gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey, commit.gpgsign true). Trailers on every commit: Agent and Claude-Session.
4. Reads `agent.json`, `now.md`, `decisions.md`, `learnings.md` here, `history/`, then the website's CLAUDE.md and board/abp/correspondent.md.
5. Releases only with `AGENT=cl-6.correspondent@PrompTugal.dinis newsroom/tools/release.sh`.
