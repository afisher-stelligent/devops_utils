# AWS MFA Generator for CLI

This Python 3 script allows Mac or Linux users to generate 8 hour
sessions using MFA.

## Prerequistes

Follow the instructions provided in Lab 0.1.1: AWS Access Keys before continuing.
Add the following line to your ~/.aws/config file's [default] section before continuing:

`mfa_serial = arn:aws:iam::<your MFA Serial ARN>`

## Installation

It's recommended to run this utility inside a [Python Virtual Environment](https://docs.python.org/3/library/venv.html)

Clone the repository, CD to this directory, and then do a `pip3 install`:
    `pip3 install -r requirements.txt`
This will install the Boto3 library and all it's dependencies.

## Running the script

To run the script, execute as follows:

`python3 aws-mfa.py`

and follow the prompts. This will create a new profile called `temp`
which you can either add to your `.bashrc` or `.zshrc` file as
an environment variable or use with the `--profile` flag with the aws
cli commands.

NOTE: if you run in a virtual enviroment or on certain systems, you'll use `pip` instead of `pip3` and `python` instead of `python`
