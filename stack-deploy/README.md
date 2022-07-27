# Stack Utility

This Python Application utilizes the [Boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) module to intelligently deploy a [CloudFormation](https://docs.aws.amazon.com/cloudformation/index.html) stack and wait for the operation to complete.

For example, an execution will check AWS to see if the stack exists, if it does, checks its state (i.e. `UPDATE_COMPLETE`) and perform an update action instead of a create action. If the status of an existing stack is either `ROLLBACK_COMPLETE` or `UPDATDE_ROLLBACK_FAILED` and attempt to delete the stack and re-create it.

## Installation

Clone the repository, CD to this directory, and install via `pip`
    `pip install -r requirements.txt`
This will install the Boto3 library and all it's dependencies.

NOTE: On some systems, you'll need to use `pip3` instead of `pip`

## Running the script

To see the various options, run

`python stack_deploy -h`

An example run might look like this:

`python stack_deploy.py -n allenfmodule06 -t 6.1.yml -p parameters_61.json -r us-west-1`

NOTE: Some systems may require the use of `python3` instead of `python`

## Potential Future Enhansemens

- Scan the CFN Template and add capabilities dynamically (i.e. `CAPABILITY_IAM`) or pass as a parameter
