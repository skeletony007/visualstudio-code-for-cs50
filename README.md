## What is this? 👇

> [cs50.readthedocs.io/code](https://cs50.readthedocs.io/code)

*Visual Studio Code for CS50*, web-based IDE

### Shortcuts 🍔

- Visit
  [code.cs50.io/.devcontainer.json](https://code.cs50.io/.devcontainer.json)
  for the latest version of CS50’s `.devcontainer.json`.
- Visit [code.cs50.io/codespaces](https://code.cs50.io/codespaces) to access
  your codespaces in CS50’s GitHub organization.
- Visit [code.cs50.io/commits](https://code.cs50.io/commits) to access all of
  the commits that have been pushed to your repository in CS50’s GitHub
  organization.
- Visit [code.cs50.io/repo](https://code.cs50.io/repo) to access your
  repository in CS50’s GitHub organization.
- Visit [code.cs50.io/restart](https://code.cs50.io/restart) to restart your
  codespace.
- Visit [code.cs50.io/settings.json](https://code.cs50.io/settings.json) for
  CS50’s default settings for VS Code.
- Visit [code.cs50.io/stop](https://code.cs50.io/stop) to stop your codespace.
- Visit [code.cs50.io/update50.sh](https://code.cs50.io/update50.sh) for the
  latest version of `update50`.

### Deleting a Codespace 🗑️

**Deleting a codespace will delete all files and folders therein.** If you are
sure you want to delete a codespace:

1. Visit [code.cs50.io/codespaces](https://code.cs50.io/codespaces).
2. Under Your codespaces, to the right of `main`, click …, select **Delete**,
   and click **OK**.

You can then create a new codespace by logging back into code.cs50.io.

## 🔑 Key

| Placeholder | Value                                                                                        |
|--           |--                                                                                            |
| `USERNAME`  | Your GitHub Login                                                                            |
| `ID`        | Your (numeric) GitHub ID (retrieved using GitHub API: https://api.github.com/users/USERNAME) |
| `REPO`      | The name of the GitHub repository what you want to work on                                   |

## 🌵 Git and Visual Studio Code for CS50

> [cs50.readthedocs.io/code/#git](https://cs50.readthedocs.io/code/#git)

Because a codespace is already associated with a Git repository in CS50’s
code50 organisation at https://github.com/code50, which is used for automated
backups, CS50 effectively disables git anytime you’re inside of
`/workspaces/ID` (which is a codespace’s default directory).

However, you can still use git outside of that directory, such as by cloning
other repositories into /workspaces itself.

## Using Git with Visual Studio Code for CS50

### Symbolic links and Git 🔗

A symbolic link is a file that points to another file or directory. When
accessed, it redirects to the file or directory it points to. It acts like a
shortcut or alias.

1. Change directory to `/workspaces` so that you can use Git

   ```bash
   $ cd /workspaces
   ```

2. Now you can execute

   ```bash
   $ git clone https://github.com/USERNAME/REPO.git
   ```

3. Create the symbolic link

   ```bash
   $ ln -s /workspaces/REPO /workspaces/ID
   ```

   where

   `/workspaces/REPO` is the "target" directory; the symbolic link will point here

   `/workspaces/ID` is the "source" directory; will contain the symbolic link named `REPO`

Now you can use Git outside of the `/workspaces/ID` directory to operate on
your repository, and because of your symbolic link, the same files work with
the frontend of Visual Studio Code for CS50:

- Will be automatically backed up to CS50’s code50 organisation (only
  `/workspaces/ID` will be automatically backed up)
- Will be visible in the explorer pane of Visual Studio Code

### Using Git step-by-step ⚙️

See <https://github.com/skeletony007/guide/blob/main/git-usage.md> for instructions on... using Git.
