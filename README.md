# README.md

## NDBundleBuildSvr-onoff and MNBundleBuildSvr-onoff

### V 0.1

### Prerequisites

1. install Python3

2. install boto3
    2.a pip install boto3

4. create credential and config files. Default Linux path = ~/.aws/credentials --  Default Windows path is = C:\Users\user\.aws

5. edit line 6 of the .py file to use the correct instance ID; make sure the single quote marks remain
    instance_id = 'i-1234567890' to 'i-yourinstanceid'


### Use

From a command line terminal, type the commands below. Provide the full path of the .py files as needed.  

Turn on the server
python3 NDbundleBuildSvr-onoff.py ON 

Turn off the server
python3 NDbundleBuildSvr-onoff.py OFF

Entering any argument except 'OFF' (case sensitive) will attempt the start the instance. For example, the command below will try to start the server.
python3 NdbundleBuildSvr-onoff.py whatever

The terminal will return json. If you have permissions, the json will display the 'CurrentState' and the 'PreviousState'. If you do not have permission, a long error message will be displayed.  Check your credential file prerequisites.