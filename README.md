<div align="center">

<img src="static/kraken.png" alt="Kraken" width="120" />

# Kraken

GitHub identity intelligence: resolve emails from a username, or the account behind an email.

</div>

---

## What it does

Kraken combines two OSINT directions into one web tool, switchable from a single toggle.

**find emails** (username input) scrapes public git patch metadata from a user's commit history and ranks each address by how closely it matches the target handle. No authentication; public repositories only.

**find account** (email input) probes GitHub's commit-author linking to resolve the account behind an email, using your own token. It creates a throwaway private repo, authors a commit with the target email, reads back the linked profile, then deletes the repo.

Built with SvelteKit (Svelte 5) and Tailwind v4.

## Privacy and scope

- **find emails** reads only public commit metadata. Ranking reflects handle/email similarity, not confirmed ownership; surfaced addresses may belong to co-authors.
- **find account** returns only public profile data and is attributable to the operator's own rate-limited account. Anyone can opt out by enabling *Keep my email addresses private* at <https://github.com/settings/emails>.

---

Tooling by [NotAlex](https://github.com/NotAlex-Tooling/).
