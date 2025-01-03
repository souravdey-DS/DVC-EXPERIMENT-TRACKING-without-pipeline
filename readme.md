# Learn & practice about the DVC experiment tracking without pipeline

Steps to be followed:

Step 1: Git initialize the repo
Step 2: DVC initialize
Step 3: Add code to your training file
Step 4: Run DVC live with context manager and 'log_params()' and 'log_metrics()'
Step 5: Run the train.py file
Step 6: Parameters & metrics get logged in the 'dvclive' folder for the current experiment ['params.yaml' & 'dvc.yaml' also created]
Step 7: Change the parameter values and run train.py again
Step 8: Second experiment also got logged in the dvclive folder

History of the experiment is maintained in the temp folder in '.dvc' directory

Step 9: Create a new branch for the best experiment using 'dvc exp branch' command
Step 10 : Checkout to this new branch for further development

** The whole philosophy of experiment tracking in DVC is to declutter your git commits and only to save those experiments which are the best among all and leave the others in temp folder of dvc cache **

Step 11: Use 'dvc exp apply' to switch between the experiments without creating a new branch [ similar to 'dvc checkout' ]
Step 12: Use command 'dvc exp diff' to compare the parametrs & metrics among two experiments and to see the change in values between the two experiments.