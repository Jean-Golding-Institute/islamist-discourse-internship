# Developer Guidelines

## Directory structure.

The structure of the directory is as follows, not all of this is available through GitHub as explained below.
```
.
├── _ data/
│   ├── created/
│   └── original/
├──  misc/
├──  scripts/
├──  venv/
├── README.md
├── .gitignore
└── requirements.txt

```

| File/directory | Notes|
|----------------|------|
| `data/` | We don't provide the data here, since it is of a sensitive nature. |
| `data/created` | All newly created/processed data is stored in this directory |
| `data/created/arabic_corpus.csv` | Arabic script speeches |
| `data/created/english_corpus.csv` | Speeches translated into English |
| `data/original` | All original data should be stored in this directory (and the files should be made read-only. |
| `figures/` | This is where we will store figures |
| `misc/` | Contains miscellaneous documents relating to the project that we don't want to upload to GitHub, like timesheets, CVs, etc. |
| `scripts/` | Contains Python scripts. Each script has a docstring explaining what it does at the top of the file. |
| `.gitignore` | Tells Git what we want to save copies of (and therefore what will be visible on GitHub) and what we do not. |
| `CONTRIBUTING.md` | Explains how to get things installed, and how to make changes to the repository |
| `README.md` | Acts as a front-page for the GitHub repository for anyone who comes across it. |
| `requirements.txt` | Lists the Python packages that are needed to run the code. |

<!--
| `venv/` | When working on Python projects, having a virtual environment is helpful to make sure that you keep the right version of each package where you are using it (see [setting up a virtual environment](#virtual-environments) |
-->

## How-to

### How to set up your computer

1. If you don't have one already, create a [GitHub account](https://github.com/join) and make sure that you have Python installed (for example, through Anaconda).
3. [Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) the main branch of the repository to create your own copy. 
3. Open a terminal on your computer and [Git clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository) your fork of the repository to your local machine.
5. Go to the cloned repository and create new folders for `data`, `data/created`, `data/original`, etc.
6. Go to [this Sharepoint directory](https://uob-my.sharepoint.com/:f:/r/personal/fd17626_bristol_ac_uk/Documents/Text-Mining%20Project?csf=1&web=1&e=6vj49M) and download the data into the `data/orginal` directory you just created and rename the two csv files to `arabic_corpus.csv` and `english_corpus.csv`.
7. Make these files read only, so you don't accidentally overwrite anything in them.
8. Install the packages in the `requirements.txt` file using `pip install requirements.txt` or `conda install --file requirements.txt` if you're using Anaconda.

### How to make changes

1. Find the GitHub issue, or make a new GitHub issue for the task that you're planning on working on, and assign it to yourself and comment on it to let us know you're working on it. You can also comment on this issue (and tag me @nataliethurlby) which will notify me if you need to ask any questions at any point.
2. Make sure that your fork is up to date with the main repository, by [syncing your fork](https://docs.github.com/en/github/collaborating-with-pull-requests/working-with-forks/syncing-a-fork).
3. Create a new branch for the new feature that you're working on. 
3. Work on your local branch to make changes, commiting and pushing frequently.
    - Note: If you use a new Python package in your code, add it to the `requirements.txt` file
3. When you have made some progress, e.g. got tokenisation working, make a Pull Request, and ask for a review. This will let us know about the change that you've made and we can "pull in" the work that you've done to the main repository. It's good to do this little and often.
4. I will approve the pull request, or ask for some small changes. If small changes, make the changes, then let me know when you're finished. 
5. Success! [Delete your old branch](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository#deleting-a-branch) from your Fork now that you no longer need it.

----
Notes:
- Be careful what you commit to logfiles as these are tracked by GitHub