# OSF-bot
A community bot, used in the Manipal OSF server.

---

## Contribute

If you want to contribute, report a problem, add or suggest a new fix or feature, you can [open a new issue](https://github.com/Manipal-OSF/OSF-bot/issues/new). The issue should be accepted and discussed before starting to work on the feature. See [Dev Installation](#Dev-Installation) to know how to start working on said feature.

---

## Discord Setup

To get a **token**, go to [Discord Developer Portal](https://discord.com/developers/applications). Create an application and add a bot.

## Dev Installation

1. Clone the repository:
- Traditional way: `https://github.com/Manipal-OSF/OSF-bot.git` or `git@github.com:Manipal-OSF/OSF-bot.git`.

- Using Github CLI: `gh repo clone Manipal-OSF/OSF-bot`.

Then navigate to the directory `cd OSF-bot/`

2. Create a new branch by `git checkout -b <name of new local branch> main` or `git switch -c <name of new local branch> main`. Make sure the new branch name is related to the feature or the fix you have in mind.

3. Create a `.env` file with following contents:

   ```text
   BOT_TOKEN = <Your token> # See Discord Setup above
   ```

4. Install poetry: `pip install -U poetry` and run the following:

   ```sh
   # This will install the development and project dependencies.
   poetry install

   # This will install the pre-commit hooks.
   poetry run task precommit

   # Optionally: run pre-commit hooks to initialize them.
   # You can start working on the feature after this.
   poetry run task lint

   # Run the bot
   poetry run task bot

   ```
5. Lint and format your code properly using `poetry run task lint`, and push changes `git push -u origin <name of new remote branch>`

## Commands to Remember
`poetry run task precommit` - Installs the pre-commit git hook

`poetry run task format` - Formats the project with black

`poetry run task lint`- Runs pre-commit across the project, formatting and linting files.

`poetry run task bot` - Runs the discord bot.
