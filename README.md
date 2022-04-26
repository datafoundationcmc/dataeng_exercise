# NN CMC BDS Data Engineering Exercise

Welcome to our data engineering exercise :) We're delighted that you decided to take the time to do this exercise. We'll be using your solution as basis of discussion when we get to meet you on your first interview. Below, you'll find an explanation for the exercise. You are free to write the solution to this exercise either as code, or with an textual explanation (the more detailed and clear, the better!).

We wish you the best of lucks!

# Getting Started

You're asked to fork this repository. When you do, we'll be notified. At the end of the time you're given to complete this exercise, we'll have a look at your fork, meaning you don't need to send us anything (except for an optional task in **Exercise 2**). Reach out to Diogo on 004530755550 should you have any questions. Don't forget you need the AWS access keys sent to you by the HR.

# Exercise 0

+ Install the [aws-cli-v2](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) (recommended kernel: linux)
+ Configure a profile `exercise` with the access keys provided by the HR

You can verify your installation and configuration with the expected output:

```shell
aws s3 ls --profile exercise

An error occurred (AccessDenied) when calling the ListBuckets operation: Access Denied

aws s3 ls s3://cmc-bds-de --profile exercise
    PRE wishes/

aws s3 cp s3://cmc-bds-de/wishes/you/good/luck.parquet data.parquet --profile exercise
download: s3://cmc-bds-de/wishes/you/good/luck.parquet to ./data.parquet
```

# Exercise 1

Fork this repo. Your fork should include the following branching strategy:

```txt
main
│
└╴tst
  │
  └╴dev
    │
    ├╴ exercise_1
    ├╴ exercise_2
    └╴ exercise_3
```

TODO:
+ **Exercise**: commit the work on `exercise_x` to the `exercise_x` branch (Example: commit changes to `exercise_2` to the branch `exercise_2`)
+ **Exercise**: At the end of each exercise `exercise_x`:
    + issue a PR from `exercise_x` to `dev`, approve it
    + issue a PR from `dev` to `tst`, approve it
    + issue a PR from `tst` to `main`, approve it
+ **Exercise**: branch `exercise_x` further should you find it fit
+ **Question**: Why are git branching strategies important? (commit `README.md` to the `exercise_1` branch)
    + Answer: **your answer here**


# Exercise 2

You're asked to build and publish a python package to a public package index ([pypi](https://pypi.org/)). The package should include a class `Ops` and two methods `dropna`, `pivot` such that the script `exercise_3/exercise_3.py` compiles and executes as expected. The commands you use to build and publish the package go to the script `exercise_2/azure-pipelines.yml`. This CICD pipeline script will encapsulate the logic for the following devops steps:
- linting
- unit testing
- building
- publishing

We don't ask that you setup a pipeline to actually do all of these things, but you're encouraged to do it should you find yourself having the time! (you can opt by any other pipelines provider, please send us an url to the pipeline if you choose to do it).

TODO
+ **exercise** include all the dependencies you see fit in `exercise_2/requirements.txt`.
+ **exercise** Create your own package in `exercise_2/{your-package-name}`, but `exercise_3/exercise_3.py` must import from [pypi](https://pypi.org/), not from `exercise_2/{your-package-name}`. If you can't publish the package to Pypi, import it locally.
+ **exercise** Include a dir `test` in your package with whatever unit tests you might find suiting. Make sure the tests are passing.
+ **exercise** Include pydocs in the module, class and methods.
+ **exercise** Lint the code


# Exercise 3

TODO:
+ Complete `exercise_3/exercise_3.py` such that it compiles and executes. We're expecting to find the result in our S3 bucket :)
+ Lint `exercise_3/exercise_3.py`
