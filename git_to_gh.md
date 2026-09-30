# This is a step-by-step reference guide for daily use of Git and GitHub

1. Each project directory must first be initialized with: `git init`

2. Before anything can be uploaded to GitHub, a new repo must be created there

	- both README and .gitignore files can be created simultaneously

3. This repo can't be accessed until running the command: `git remote add origin <url>`

	- link is provided upon repo creation

	- to ensure it worked as expected, run: `git ls-remote`

	- once the repo link has been added as "origin", it's then possible to send changes with: `git push origin main`

4. Before pushing, changes must be staged and committed with:

	- `git add .`

	- `git commit -m "message"`

5. Only then can we run: `git push origin main`

### On the contrary, we can do the opposite if changes are made on GitHub or have come from someone else

1. Ensure the GitHub repo exists according to the above steps

	- when pulling to a new system, remember that the remote must still be added

	- run this command to get a repo NOT already on your system: `git clone <url>`

2. Commit changes on GitHub itself

	- the local machine won't know about these yet

3. For retrieval, run this command in your terminal: `git pull origin main`

	- this effectively downloads the new commit(s) and merges into the current local branch

	- `git pull origin main` essentially uses the fetch and merge commands at the same time

## Update 9/30/26

Best practice is to create projects on GitHub *first*:

    - initialize repo on GitHub

    - clone with `git clone <url>`

    - set upstream with `git push -u origin main`

    - simply use `git push` and `git pull` going forward
