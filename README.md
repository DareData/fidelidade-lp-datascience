# Fidelidade Data Science Learning Pod - Powered by LDSA & DareData Engineering

Welcome to Fidelidade Data Science Learning Pod!

## Suggested learning calendar

> **Note**: This is just a suggestion. Groups are encouraged to set their own deadlines with their mentors.

Week 01 _(~3.5 hours)_

- Discover Module01 SLU's Units.
- Pick contents that you've had the least exposure so far, read notebooks and run cells.

Week 02 _(~3.5 hours)_

- Select 2/3 SLU's to practice your coding skills, completing the `Exercise notebook.ipynb`


Week 03 _(~4 hours)_

- Data Workflows.
- Combining DataFrames.
- Advanced Pipelines.
- Complete exercises from `Exercise notebook.ipynb`

Week 04 _(~4 hours)_

- Time Series Baseline.
- Classic Time Series.
- ML Timeseries Models
- Complete exercises from BLU's

Week 05 _(~5 hours)_

- Final Project

Week 06 _(~5 hours)_

- Final Project


## Initial Setup

#### Creating a Python Virtual Environment

##### Start by installing ensuring pip, setuptools, and wheel are up to date:

```
python3 -m pip install --user --upgrade pip setuptools wheel
```

* Create a virtual environment with the name `module1`

```
python3 -m venv ~/.virtualenvs/module1
```

* Activate the environment

```
.virtualenvs/module1/bin/activate
```

>Note: after you activate your virtual environment you should see at the leftmost of your command line the name of your virtual environment surrounded by parenthesis, like this:

```
mig@my-machine % .virtualenvs/module1/bin/activate
(module1) mig@my-machine %
```

And you're able to make sure your virtual environment is active using the `which` command (it outputs the location of your virtual environment's python installation):

```
(module1) mig@my-machine % which python
/Users/mig/.virtualenvs/module1/bin/python
```

Now update pip.

```
(module1) pip install -U pip
```

### Setup your Workspace Repository

It's good practice to store your work with version control.
In this academy that is a requirement as it is how you will make your work
available to us.

#### Creating the Workspace

1. Log into _GitHub_
1. Fork this main repo into a new **private** _GitHub_ repository.



### Get the Learning Material

You will be cloning the [fidelidade-lp-data-science](https://github.com/DareData/fidelidade-lp-data-science)
repository.
All of the learning material you need will be made available on this repo
as the academy progresses.

1. Open a Terminal or Git Bash, the next steps are on this terminal
1. Clone the students repository
[fidelidade-lp-data-science](https://github.com/DareData/fidelidade-lp-data-science)

```
git clone https://github.com/DareData/fidelidade-lp-data-science.git
```

Or if you have your ssh keys set up:

```
git clone git@github.com:DareData/fidelidade-lp-data-science.git
```

### Running and Submitting a Learning Unit

In the `fidelidade-lp-data-science` repository that you just cloned there is a sample
learning unit.
It's used to give instructors guidelines to produce the learning units.
We are also using it to ensure that you are able to run and submit a learning
unit.

So go ahead and copy the sample directory `sample/module1 - LU Tutorial` from the `fidelidade-lp-data-science` repository to your repository (named `fidelidade-lp-data-science`).
![Sample learning unit](assets/sample_learning_unit.png "Sample learning unit")

The grader only requires you to have the contents in a directory starting with
the learning unit's ID, but we highly advise to keep the same directory
structure as the students repository.
All learning units are organized as:

```markdown
<specialization ID> - <specialization name>/<learning unit ID> - <learnin unit name>
```

Doing so will help you keep organized and ease copying data from the students
repository to yours.

#### Working on the Learning Unit

All learning units come as a set of Jupyter Notebooks (and some links to
presentations).
Notebooks are documents that can contain text, images and live code that you
can run interactively.

In this section we will launch the Jupyter Notebook application.
The application is accessed through the web browser.

Once you have the application open feel free to explore the sample learning
unit structure.
It will give you a handle on what to expect and what rules the instructors
follow (and the effort they put) when creating a learning unit.

So let's start the Jupyter Notebook app:

1. Activate your virtual environment

    ```
    .virtualenvs/module1/bin/activate
    ```

1. Enter the Learning unit directory in your workspace directory (`fidelidade-lp-data-science`).
    >Note: It is **VERY IMPORTANT** that you **ALWAYS** work on the files on your `fidelidade-lp-data-science` repository, and **NEVER** work on files that are in your `fidelidade-lp-data-science` repository!

    ```
    cd ~/projects/batch4-workspace/sample/"module1 - LU Tutorial"
    ```

1. Installing the necessary packages

    ```
    pip install -r requirements.txt
    ```

1. Run the jupyter notebook
    >**Windows 10 note:** if you are running **Windows 10** with WSL, the command to run the jupyter notebook is: `jupyter notebook --NotebookApp.use_redirect_file=False`

    ```
    jupyter notebook
    ```

When you run the `jupyter notebook` command, you should see something similar to this in your terminal:
![Open exercise notebook](assets/jupyter_terminal.png "Open exercise notebook")
Your browser should pop up with Jupyter open, however, if this does not happen, you can simply copy the link you see on your terminal (the one that contains `localhost`) and past it in your browser's address bar:

![Open exercise notebook](assets/jupyter_terminal_link.png "Open exercise notebook")

>Note: If you see these scarry looking error messages, don't worry, you can just ignore them.

![Open exercise notebook](assets/jupyter_error_red.png "Open exercise notebook")

##### The Exercise Notebook

Make sure you open and go through the Learning Notebook first.

Every learning unit contains an exercise notebook with exercises you will
work on.
So let's have a look at the sample Learning Unit.

1. On the Jupyter Notebook UI in the browser open the exercise notebook
![Open exercise notebook](assets/jupyter_exercise_notebook.png "Open exercise notebook")
1. Follow the instructions provided in the notebook

Besides the exercises and the cells for you to write solutions you will see
other cells with a series of `assert` statements.
This is how we (and you) will determine if a solution is correct.
If all `assert` statements pass, meaning you dont get an `AssertionError` or
any other kind of exception, the solution is correct.

Once you've solved all of the notebook we recommend the following this simple
checklist to avoid unexpected surprises.

1. Save the notebook (again)
1. Run "Restart & Run All"
![Restart & Run All](assets/jupyter_clear_and_run.png "Restart & Run All")
1. At this point the notebook should have run without any failing assertions

If you want to submit your notebook before it is all the way done to
check intermediate progress, feel free to.

If you are able to go through the entire process and get a passing grade on
the sample LU you'll have a good understanding of the same flow that you'll use
for all LUs throughout the academy.

#### Commit and Push

Now you have worked on the sample learning unit and you have some uncommitted
changes.
It's time to commit the changes, which just means adding them to your `fidelidade-lp-data-science`
repository history, and pushing this history to you remote on _GitHub_.

* Using the terminal commit and push the changes

```
git add .
git commit -m 'Testing the sample notebook'
git push
```

