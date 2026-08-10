# Activity Log

This repo exists for one reason: **not every valuable contribution to the
Summer 2026 Cohort is a commit to a project repo.** Design feedback,
documentation reviews, helping a teammate debug in voice chat, triaging
issues, mentoring - all of that is real work, and none of it shows up in
GitHub's activity graph the way a code commit does.

The cohort's activity floor requires visible, productive GitHub activity
every day (see `POLICY.md` / `COHORT_NOTES.md` in the main planning repo).
If your contribution that day wasn't a commit, PR, issue, or comment on one
of the project repos, log it here instead - a commit to this repo counts the
same way.

## How to log a day's work

1. Find (or create) your file at `logs/<your-github-username>.md`. Copy
   [`logs/TEMPLATE.md`](./logs/TEMPLATE.md) if it doesn't exist yet.
2. Append a new dated section at the **top** of your file (most recent
   first):

   ```markdown
   ## 2026-08-10

   Reviewed 3 open PRs on pulseboard and left feedback on naming and error
   handling. Paired with someone in voice chat for ~45 min helping them
   debug a Mongoose query.
   ```

3. Commit and push directly to `main` - **no PR needed for this repo.**

   ```bash
   git add logs/<your-github-username>.md
   git commit -m "activity log: 2026-08-10"
   git push
   ```

That's it. One commit, one entry, and it's picked up the same way any other
GitHub contribution is.

## A few ground rules

- **Only edit your own file.** Everyone has write access to this repo so
  logging stays frictionless, but please don't edit anyone else's log.
- **This supplements, it doesn't replace, real contribution.** If your work
  that day *was* a commit, PR, or issue/comment on a project repo, you don't
  need an entry here too - that already counts.
- **Be specific.** "Helped out today" doesn't tell anyone anything. A
  sentence or two on what you actually did is enough.
- This is an honour-system log, same as everything else in this cohort. If
  entries look like they're being used to fabricate activity rather than
  reflect it, that's a policy violation like any other.

## Why direct commits instead of PRs?

The whole point is removing friction for people whose contribution wasn't
code. Requiring a PR + review here would just recreate the same barrier
we're trying to route around. If you *want* feedback on how you're logging
things, feel free to ask in Discord - just don't wait on it to commit.
