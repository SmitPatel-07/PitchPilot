# Contributing to PitchPilot

Thanks for wanting to help. PitchPilot is a small project, so the process is simple.

## Before you start

- **Small fix or typo?** Just open a pull request.
- **New feature or a big change?** Open an issue first so we can agree on the idea before you spend time on it.
- **Looking for something to pick up?** Check the issues labeled `good first issue`.

## Set it up

You need Python 3.11 or newer.

```bash
git clone https://github.com/SmitPatel-07/PitchPilot.git
cd PitchPilot
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
pip install ruff pytest
cp .env.example .env             # add your model settings
streamlit run app.py
```

Use the sample data in `sample_data/` while you work. It's fake, so nothing real gets emailed.

## Making a change

1. Fork the repo and create a branch from `main`. Short names are fine: `fix-mx-check`, `feat-follow-ups`, `docs-quickstart`.
2. Make your change. Keep each pull request focused on one thing.
3. Add or update tests if you changed behavior.
4. Run the checks locally before you push:

   ```bash
   ruff check .
   python -m pytest -q
   ```

5. Open the pull request and say what changed and why. A screenshot helps for anything in the UI.

The same checks run automatically on every pull request. A green check is needed before merging.

## Commit messages

Start with a short label so the history is easy to read:

- `feat:` a new feature
- `fix:` a bug fix
- `docs:` documentation only
- `test:` tests only
- `refactor:` code cleanup with no behavior change

Example: `fix: skip role addresses like info@ in the verifier`

## Code style

- Python 3.11+, with type hints on functions.
- Keep functions short and names clear.
- `ruff check .` must pass.
- Put new settings in `.env.example` and explain them in the README.

## Things that are not up for change

PitchPilot is built to be careful with people's inboxes, so pull requests that do any of the following won't be merged:

- Remove or bypass the **human approval step**
- Remove or weaken the **unsubscribe link**, the **suppression list**, or the **daily send limits**
- Turn **dry-run off by default**
- Add features designed to hide the sender's identity or get around spam filters

## Security and privacy

- Never commit API keys, passwords, or your `.env` file.
- Don't put real prospect data in issues, pull requests, screenshots, or test files. Use made-up data.
- If you find a security problem, don't post it publicly. Message me on [LinkedIn](https://www.linkedin.com/in/mrpatelsmit) instead.

## Reporting bugs

Open an issue and include:

- What you did and what you expected
- What actually happened, with the error message if there is one
- Your Python version, your OS, and which model provider you used

## Questions

Open an issue or start a discussion. Questions are welcome.
