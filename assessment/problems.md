# Assessment Problems

Follow the [assessment instructions](assessment.md) and [guidance](guidance.ipynb) closely to ensure you solve the following problems correctly.

## Problem 1: Data

In this problem set, you will download data from [waterlevel.ie](https://waterlevel.ie/) using their API.

Using the command line, create a folder called `data` in your repository.

Then download the latest water level data for Annaghdown Pier using `wget` with the following URL.

```sh
https://waterlevel.ie/data/day/30083_0001.csv
```

Move the downloaded file to `data/latest.csv`.

In your `problems.ipynb` notebook in the root of your repository, explain how the wget program works.

Add and commit your work to the repository, and push it back to GitHub.

## Problem 2: Timestamps

Modify your `wget` command above to save the file with a timestamped filename:

```sh
data/waterlevel_YYYYmmdd_HHMMSS.csv
```

To do this, use the `date` command with backticks.

Note the `YYYY` is the four digit year and `mm` is the tow digit month, etc.

Test the command at least three times, creating at least three new files.

In your `problems.ipynb` notebook in the root of your repository, explain what backticks are used for in bash scripts.

Add and commit your work to the repository, and push it back to GitHub.

## Problem 3: Script

Write a bash script called `get_data.sh` to download the latest data, saving it with a timestamped filename in `data/`.

Then make the script executable and test it.

Run the script at least three times on different days or times.

In your `problems.ipynb` notebook in the root of your repository, explain how your bash script works.

Add and commit your work to the repository, and push it back to GitHub.

## Problem 4: GitHub Actions Automation

Create a GitHub Actions workflow in `.github/workflows/get_data.yml`.

The workflow should:

* Run daily at 10:00am (`cron`).
* Support manual triggering (`workflow_dispatch`).
* Use a Ubuntu virtual machine.
* Clone the repository.
* Run your script with: `bash scripts/log_water.sh`.
* Commit and push changes.

Make sure to include steps to configure GitHub user identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@ema.il"
```

Make sure the workflow works by testing it manually.

In your `problems.ipynb` notebook in the root of your repository, write a brief note explaining how GitHub Actions workflows work.

Add and commit your work to the repository, and push it back to GitHub.

## Problem 5: Analysis

In your `problems.ipynb` notebook:

* Explain what the data set contains (you need to research this yourself.)
* How you obtained the data (explain your bash script and GitHub Action workflow).
* Describe the downloaded data (columns, formats, etc.).
* Load and visualize the latest data file.

***

**End**
