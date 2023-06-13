# Training Plan

'TrainingPlan' is a DAML application based on training plan management of an organization. This includes processes where proposer can propose their intended Training Plan to their supervisors and the supervisor to approve or reject the proposal. If the proposal is rejected, the proposer could modify the proposal based on the supervisor's input and submit again for approval. If the proposal is approved, it will then be pushed towards the organization's Training Team wherein they can start with the Training processes, where in this case, publishing the approved training to expected audiences.

This application can be extended further by adding in ability to register to a particular training, propose budget for a virtual/classroom training, etc.

<br>

## Workflow
1. Initial Contract (training rights) created by Company and assigned to parties that can submit training plans.
2. Proposer (Alice) creates Training Proposal via its Training Rights Contract and submits for approval to Supervisor.
3. Supervisor rejects Training Proposal and provide comments.
4. Alice modifies the proposal and submit for approval.
5. Supervisor approves the Training Proposal and submits to the Training Team.
6. Training Team publishes the approved training to expected audience of the training.
7. Expected Audience should be able to see the training details.

<br>

## Pre-Requisite

This application is running on daml version 2.6.4.
Ensure you have v2.6.4 or above installed.

See below reference links for further pre-requisites for running a standard DAML application.

https://docs.daml.com/getting-started/index.html#prerequisites

https://docs.daml.com/getting-started/installation.html

https://docs.daml.com/getting-started/path-variables.html


<br>

## Running the application's tests

To run the prepared daml script tests:

1. Open a terminal and then navigate to the project's `daml` folder. 

2. Use below commands to ensure clean and built application will be running.

    ```daml
        daml clean
        daml build
        daml test --show-coverage --color
    ```

<br>

## Running the application

In order to run the application: 

1. Open a terminal and then navigate to the project's `daml` folder. 

2. Use below commands to ensure clean and built application will be running.
    NOTE: `daml start` will automatically start the ledger as well as the navigator.

    ```daml
        daml clean
        daml build
        daml start
    ```

<br>