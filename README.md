# Odeus

Odeus is a small Python utility that creates dated Git commits in a repository
and pushes them to its configured remote. It is intended for personal testing
of Git history and contribution activity. Use it only with repositories you
own or are authorized to modify.

## Requirements

- Python 3
- Git installed and configured
- A local Git repository with a remote

## Setup

For a dedicated repository, create a repository named `odeus` on GitHub and
clone it:

```bash
git clone https://github.com/YOUR_USERNAME/odeus.git
cd odeus
```

Copy `main.py` into the repository, or run it from this project while passing
the repository path when prompted.

## Run

```bash
python main.py
```

The program asks for:

1. The number of commits (default: `20`)
2. The local repository path (default: current directory)
3. The file to update (default: `data.txt`)

Each commit appends one line to the selected file, uses a random date from
the previous 365 days, and is pushed with `git push`.

## Notes

- Make sure the selected repository has a configured remote and valid Git
  credentials before running the program.
- GitHub may not count commits unless the commit email is associated with
  your account and the commits are pushed to a branch GitHub recognizes.
- This tool does not replace genuine project work or contributions.
