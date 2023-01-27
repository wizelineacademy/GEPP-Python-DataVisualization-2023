# Session 02

## TOPIC : Setup Python locally

## TOPIC : Moneyball Discussion

## Article Discussion

[How a Math Genius Hacked OkCupid to Find True Love](https://www.wired.com/2014/01/how-to-hack-okcupid/)

### Check if Python is already installed

Open a Terminal (or Command) window.

Type `python3 --version`.

We expect the result to be Python 3.8 or more. Currently the latest version (2022-07-13) is 3.10.5.

#### If we already have Python Installed we are good to go

### Python Installation

The process is **different for each Operating System**.

#### The easy way

**[Install from the Python Webpage](https://www.python.org)**

![Installation menu](images/installation.png)

#### MacOS installation using [Homebrew](https://brew.sh)

```bash
brew install python3
```

#### Linux

```bash
sudo apt install python3
```

OR

```bash
sudo yum install python3
```

## Create a Virtual Environment

- Confirm Python is installed running `python3 --version` in a terminal or console.
- Create a directory for the Bootcamp.
- Move to the new directory.
- Create the virtual environment with: `python3 -m venv venv`

> The command reads as follows:
> `python3` --- Use the `Python 3` interpreter
> `-m venv` --- Use a module named `venv` > `venv` -- Create the new Virtual Environment in the `venv` directory

- Activate the virtual environment
  - In MacOS and Linux run `source venv/bin/activate`
  - In Windows run `.\env\Scripts\activate`

- Confirm you are using the virtual environment
  - In MacOS and Linux run `which python`
  - In Windows run `where python`

> Full Virtual Environments documentation [HERE](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)

## Install and Run [Jupyter](https://jupyter.org)

Run in the terminal `pip install jupyterlab`

Run Jupyter Lab with `jupyter-lab`

> Full Jupyter Install Documentation [HERE](https://jupyter.org/install)

## Feedback

Please helps us filling up the **[Feedback Form](https://docs.google.com/forms/d/e/1FAIpQLSfLdsad4R7pjyTppTO6haFmeIr_A5xZqgQvN5Bq2LmsBMY1VA/viewform)**.

## Next session

We will learn how to use IDEs (in particular Visual Studio Code), Git and GitHub.

**Homework:**

Read the article: [We Can Protect the Economy From Pandemics. Why Didn't We?](https://www.wired.com/story/nathan-wolfe-global-economic-fallout-pandemic-insurance/)

**Optional** See the movie: [The Big Short](<https://en.wikipedia.org/wiki/The_Big_Short_(film)>)
