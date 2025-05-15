# Contributing Guidelines

## Branching Strategy

- \`main\`: Production-ready code
- \`develop\`: Development branch, all feature branches merge here
- \`feature/*\`: New features
- \`bugfix/*\`: Bug fixes
- \`release/*\`: Release preparation
- \`hotfix/*\`: Urgent fixes for production

## Commit Message Format

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

\`\`\`
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
\`\`\`

Types:
- feat: A new feature
- fix: A bug fix
- docs: Documentation changes
- style: Changes that do not affect the meaning of the code
- refactor: Code changes that neither fix a bug nor add a feature
- perf: Performance improvements
- test: Adding or correcting tests
- chore: Changes to the build process or auxiliary tools

## Pull Request Process

1. Create a branch from \`develop\` for your work
2. Make your changes and commit using conventional commit format
3. Push your branch and create a PR against \`develop\`
4. Ensure CI passes
5. Request review from at least one team member
6. Once approved, merge your PR

## Release Process

1. Create a \`release/vX.Y.Z\` branch from \`develop\`
2. Run \`npm run release\` to update version and changelog
3. Create a PR from \`release/vX.Y.Z\` to \`main\`
4. Once merged, tag the commit on \`main\` with the version
5. Merge \`main\` back into \`develop\`