# pushwatch demo

A small demo site with [pushwatch](https://github.com/siddartha018/pushwatch) guarding it. The open pull requests copy two real attacks, defanged: every payload is replaced with a harmless `console.log` or `echo`.

- **[PR #1, "Update README.md"](../../pull/1)** looks like a README edit. It also hides code off-screen in `postcss.config.mjs`, adds a VS Code task that runs a fake font file whenever the folder is opened, and stops `.gitignore` from ignoring `.env`. pushwatch fails the check and marks each line on the diff.
- **The `rewrite-demo` branch** was force-pushed with a copy of a commit that kept its message and date but changed its files. The pushwatch run for that push reports the rewritten history.

Nothing here runs anything harmful. The real attacks are described in the [pushwatch README](https://github.com/siddartha018/pushwatch#why-it-exists).
