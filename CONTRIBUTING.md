# Contributing

Thanks for contributing to this project.

## Setup

1. Use Python 3.10+.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

## Workflow

1. Create a branch from `main`.
2. Keep commits small and focused.
3. Use descriptive commit messages.
4. Open a pull request with a short summary and validation notes.

## Code Guidelines

- Follow existing project structure and naming.
- Keep functions readable and documented.
- Add type hints when introducing new public functions.
- Avoid unrelated refactors in feature commits.

## Validation

Before requesting review:

1. Run relevant scripts and checks in `src/`.
2. Verify data paths and outputs still work with project dataset.
3. Confirm no temporary artifacts are staged.
