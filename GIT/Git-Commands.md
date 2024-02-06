# added comment
### Configuration

- **`git config`**: Configure Git settings either globally or per repository.
  - `git config --global user.name "Your Name"`
  - `git config --global user.email "your@email.com"`

### Repository Initialization

- **`git init`**: Create an empty Git repository or reinitialize an existing one.

### Cloning and Branching

- **`git clone`**: Clone a repository into a new directory.
  - `git clone <repository_url>`

		To clone a Git repository using SSH, you need to configure SSH keys and use the SSH URL of the repository. Here are the steps:

		### 1. Check for Existing SSH Keys:

		First, check if you already have SSH keys generated on your machine:

		```bash
		ls -al ~/.ssh
		```

		Look for files named `id_rsa` (private key) and `id_rsa.pub` (public key). If they exist, you can skip the next step. If not, you need to generate a new SSH key pair.

		### 2. Generate SSH Key Pair (if needed):

		Generate a new SSH key pair using the following command:

		```bash
		ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
		```

		Replace "your_email@example.com" with your GitHub-associated email address. Press Enter to accept the default file locations and enter a passphrase if you wish.

		### 3. Add SSH Key to SSH Agent:

		Start the SSH agent and add your SSH key:

		```bash
		eval "$(ssh-agent -s)"
		ssh-add ~/.ssh/id_rsa
		```

		### 4. Copy the Public Key:

		Copy the content of your public key (`id_rsa.pub`) to your clipboard. You can use the following command:

		```bash
		cat ~/.ssh/id_rsa.pub
		```

		### 5. Add SSH Key to GitHub:

		Go to your GitHub account settings, navigate to "SSH and GPG keys," and add a new SSH key. Paste the copied public key into the "Key" field.

		### 6. Clone Repository using SSH:

		Now, you can clone a Git repository using the SSH URL. Replace `<your_username>` and `<repository_name>` with your GitHub username and the name of the repository:

		```bash
		git clone git@github.com:<your_username>/<repository_name>.git
		```

		### 7. Verify Clone:

		Navigate into the cloned repository:

		```bash
		cd <repository_name>
		```


- **`git branch`**: List, create, or delete branches.
  - `git branch`
  - `git branch <branch_name>`
  - `git branch -d <branch_name>`

- **`git checkout`**: Switch branches or restore working tree files.
  - `git checkout <branch_name>`
  - `git checkout -b <new_branch_name>`

- **`git switch`** (Git 2.23 and later): Switch branches or restore working tree files.
  - `git switch <branch_name>`
  - `git switch -c <new_branch_name>`

- **`git merge`**: Join two or more development histories together.
  - `git merge <branch_name>`

- **`git pull`**: Fetch from and integrate with another repository or a local branch.
  - `git pull origin <branch_name>`

### Staging and Committing

- **`git add`**: Add file contents to the index (staging area) for the next commit.
  - `git add <file_path>`

- **`git commit`**: Record changes to the repository.
  - `git commit -m "Commit message"`

### Viewing Changes

- **`git status`**: Show the working tree status.
- **`git log`**: Show the commit logs.
  - `git log --oneline`

### Remote Repositories

- **`git remote`**: Manage set of tracked repositories.
  - `git remote -v`

- **`git push`**: Update remote refs along with associated objects.
  - `git push origin <branch_name>`

- **`git fetch`**: Download objects and refs from another repository.
  - `git fetch origin`

### Merging and Rebasing

- **`git merge`**: Join two or more development histories together.
  - `git merge <branch_name>`

- **`git rebase`**: Forward-port local commits to the updated upstream head.
  - `git rebase <branch_name>`

### Undoing Changes

- **`git reset`**: Reset current HEAD to the specified state.
  - `git reset --hard HEAD`

- **`git revert`**: Create new commit that undoes changes from a previous commit.
  - `git revert <commit_hash>`

### Git Collaboration

- **`git fetch`**: Download objects and refs from another repository.
  - `git fetch origin`

- **`git pull`**: Fetch from and integrate with another repository or a local branch.
  - `git pull origin <branch_name>`

- **`git push`**: Update remote refs along with associated objects.
  - `git push origin <branch_name>`

### Git Tags

- **`git tag`**: Create, list, delete, or verify a tag object signed with GPG.
  - `git tag -a <tag_name> -m "Tag message"`

### Advanced Commands

- **`git cherry-pick`**: Apply the changes introduced by some existing commits.
  - `git cherry-pick <commit_hash>`

- **`git stash`**: Stash changes in a dirty working directory away.
  - `git stash`
  - `git stash apply`

These are just some of the most commonly used Git commands. Git has a rich set of commands and options, and the choice of commands depends on the specific workflow and requirements.
