# National Anthem Project - Git & GitHub Practice Workshop

A small Flask app that shows India's national anthem, built by a team of
three to practice the daily Git loop: pull, change, commit, push - plus
branches, merges, a real merge conflict, and recovery with reflog.
The app runs live on AWS EC2.

## Meet the Team

| Name            | Role      | What they did                                  |
|-----------------|-----------|------------------------------------------------|
| Prerana N Bathi | Team Lead | Owns the repository, merges, resolves conflicts |
| Chinmayi D A    | Developer | Writes the application and the anthem content   |
| Prerana S K Das | Tester    | Finds problems, fixes formatting and text       |

## The Journey

- Part 0 - Three users configured, one name per member
- Part 1 - Repository published on GitHub and cloned
- Part 2 - Push and pull between two people
- Part 3 - Branch, merge, delete (feature/second-stanza)
- Part 4 - Merge conflict created from the same commit and fixed,
  keeping "Bharat ka Rashtragan - Jana Gana Mana"
- Part 5 - Undo and recover: uncommitted work lost, committed work
  brought back with git reflog

## Repository at a Glance

| File                | What it is                          |
|---------------------|-------------------------------------|
| app.py              | Flask app, serves one page on :5000 |
| templates/index.html| The anthem page                     |
| anthem.txt          | First line of the anthem            |
| requirements.txt    | Python dependency list (flask)      |

## Run It Yourself

    python3 -m venv venv
    source venv/bin/activate
    pip install flask
    python3 app.py

Then open http://<ec2-public-ip>:5000 in a browser.

## Four Things We Learnt

- A branch is a small file containing one commit hash. Creating one copies nothing.
- git pull brings the team's work to you. git push sends yours to them. Always pull before you start.
- A conflict happens when two branches change the same lines, having started from the same commit. Resolving it is a human decision, not a Git command.
- Committed work is almost always recoverable with reflog. Uncommitted work is not.
