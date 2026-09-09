# Repository guidance

## Purpose and map

This is a historical Electron/React window-management proof of concept. Current dependency, build, and platform compatibility are unverified.

- `src/electron-starter.js` owns desktop window creation; `src/App.js` is the React interface.
- `src/App.test.js` is the existing React smoke test.
- `package.json` and `package-lock.json` describe the historical npm toolchain, including `react-scripts` 1.1.5 and Electron 2.
- `Procfile` and `src/electron-wait-react.js` coordinate local development processes.
- `README.md` combines project notes with inherited Create React App documentation. Preserve its attribution and distinguish historical instructions from verified current behaviour.

Follow applicable task restrictions and more specific repository guidance. This file does not grant merge, deployment, installation, or external-service authority.

## Protected state and boundaries

Preserve unexplained working-tree changes. Use a separate checkout when necessary; do not reset, stash, or clean user work. Keep `.env`, dependencies, generated builds, credentials, and local data out of commits. `.env.example` contains only local development behaviour.

Preserve `LICENSE` and upstream attribution. Do not modernise dependencies or rewrite the historical implementation as part of a documentation correction. Desktop launch opens windows and an external website; it is not a read-only validation command. Generic deployment examples in the inherited guide are not deployment authority.

## Validation

For documentation-only changes, check Markdown structure, rendering, relevant links and fragments, privacy, scope, and the complete diff. Run `git diff --check` and `git diff --cached --check`. Do not run the application merely to verify documentation.

The manifest declares `npm test` for React tests and `npm run build` for a production build. These commands and compatibility with current runtimes are unverified. There is no established combined local gate or checked-in CI workflow. For code changes, inspect scripts and dependencies first, establish a compatible isolated environment with synthetic data, select a non-interactive test invocation, add focused regression coverage, and run the relevant tests and build. Record actual commands and limitations rather than claiming a skipped gate passed.

## Delivery and rollback

Verify the actual upstream target and existing PRs before creating a feature branch; the current default branch is `master`. Keep changes small and update relevant documentation. With publication authority, push normal commits and open a reviewable PR, then verify its hosted head and diff. Preserve required reviews, checks, and holds. Merge only with applicable explicit authority and current evidence; never bypass repository requirements.

A documentation rollback is a reviewed revert commit. Runtime or dependency rollback needs its own compatibility assessment. Keep transient execution logs and private context outside the repository.
