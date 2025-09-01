## Contributing

Thanks for contributing to the GenAI Developer Day notebooks! This guide outlines how to propose changes and follow our workflow.

## Development workflow
- Create a feature branch from `main` (e.g., `feat/my-improvement`)
- Make changes and run checks locally:
  - `pre-commit run --all-files`
  - Optional: run notebooks as needed to validate examples
- Open a Pull Request against `main` and fill out the PR template
- Ensure CI checks pass
- Request review (CODEOWNERS will be requested automatically)

## Commit conventions
Use conventional commits when possible:
- `feat:` new functionality
- `fix:` bug fix
- `docs:` documentation-only changes
- `chore:` tooling or maintenance

## Environment & secrets
- Copy `.env.example` to `.env` and fill values locally
- Never commit real credentials, tokens, or connection strings

## Large files
- Avoid committing large datasets or binaries to the repo
- If necessary, consider using Git LFS and update `.gitattributes`

## Pre-commit
Install and run pre-commit before committing:
```bash
pip install pre-commit
pre-commit install
pre-commit run --all-files
```

## Questions
Open an issue or ping the CODEOWNER.

