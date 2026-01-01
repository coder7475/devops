# Linting Best Practices

## Linting Definition

Linters look at program's source code and find problems automatically. They are a common feature of pull request automation because they ensure that "obvious" bugs do not make it to production.

### The Nit Approach Definition

Code reviewers leave little comments on the code called "nits" that the team can ignore until broader reviews. Nits are helpful as future references but prevent blocking important changes.

### Auto Formatter Definition

Tools that help apply code style rules based on the style guide your team has choosen automatically.

## Linting automatically in CI:

Cheap and convenient to run linting and formatting within CI steps.

```yaml
COPY ..
RUN npm run lint
```

### Better Solution

Automatically fix the issues:

```yaml
COPY ..
RUN if ! npm run eslint; then \
npm run eslint --fix && \
git config user.name 'lint-bot' && \
git config user.email 'lint@ex.com' && \
git add -A && \
git commit -m "Automatically linted" && \
git checkout -b $(git branch --show-current)-linted && \
git push -f origin $(git branch --show-current)-linted && \
echo 'lint failed!'; exit 1; \
fi
```

---

**Note**:

Any team with **more than one developer working in the same codebase** should setup a linter to catch obvious bugs.
