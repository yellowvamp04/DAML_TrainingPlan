# <a name="module-test-86191"></a>Test

## Functions

<a name="function-test-testcreatetrainingproposal-68465"></a>[test\_createTrainingProposal](#function-test-testcreatetrainingproposal-68465)

> : Script ([TestParties](Setup.html#type-setup-testparties-37364), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingPlanProposal](Main.html#type-main-trainingplanproposal-90777))
>
> Create Training Proposal: Proposer proposes training plan for supervisor's approval

<a name="function-test-testapproveproposalflow-97495"></a>[test\_approveProposal\_flow](#function-test-testapproveproposalflow-97495)

> : Script ([TestParties](Setup.html#type-setup-testparties-37364), ([ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [Training](Main.html#type-main-training-27114), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [Training](Main.html#type-main-training-27114)))
>
> Training Proposal Approval Flow: Supervisor approves the training plan proposal and sending it to the Training Team to publish.
> | This also includes training team publishing the Approved Training to expected audience types (which employees levels will be able to search/register for the training)
> Note: The search/registration for training is out of scope of this project as of the moment

<a name="function-test-testrejectproposal-19378"></a>[test\_rejectProposal](#function-test-testrejectproposal-19378)

> : Script ([TestParties](Setup.html#type-setup-testparties-37364), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingPlanProposal](Main.html#type-main-trainingplanproposal-90777), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingPlanProposal](Main.html#type-main-trainingplanproposal-90777))
>
> Training Proposal Update: Supervisor rejects the proposal and ask for revision.

<a name="function-test-testupdaterejectedproposal-4674"></a>[test\_updateRejectedProposal](#function-test-testupdaterejectedproposal-4674)

> : Script ([TestParties](Setup.html#type-setup-testparties-37364), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingPlanProposal](Main.html#type-main-trainingplanproposal-90777))
>
> Training Proposal Update: Proposer updates the rejected proposal

<a name="function-test-testapproveupdatedproposalflow-99305"></a>[test\_approveUpdatedProposal\_flow](#function-test-testapproveupdatedproposalflow-99305)

> : Script ([TestParties](Setup.html#type-setup-testparties-37364), ([ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [Training](Main.html#type-main-training-27114), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [Training](Main.html#type-main-training-27114)))
>
> Updated Training Proposal Approval: Supervisor approves the revised training proposal and shares to training team.
> | This also includes training team publishing the Approved Training to expected audience types (which employees levels will be able to search/register for the training)
> Note: The search/registration for training is out of scope of this project as of the moment

<a name="function-test-testvalidationtrainingproposal-43512"></a>[test\_validationTrainingProposal](#function-test-testvalidationtrainingproposal-43512)

> : Script ()
>
> Testing the 'ensure/assertion' in place at the create training proposal

<a name="function-test-testchoiceproposalviacid-83108"></a>[test\_choice\_proposalViaCid](#function-test-testchoiceproposalviacid-83108)

> : Script ()
>
> Test CheckProposalViaCid with correct and incorrect cid

<a name="function-test-testchoiceapprovetrainingviacid-6082"></a>[test\_choice\_approveTrainingViaCid](#function-test-testchoiceapprovetrainingviacid-6082)

> : Script ()
>
> Test CheckApproveTrainingViaCid with correct and incorrect cid

<a name="function-test-testchoicetrainingviatitle-5312"></a>[test\_choice\_trainingViaTitle](#function-test-testchoicetrainingviatitle-5312)

> : Script ()
>
> Test CheckViaTitle with existing and non-existing titles

<a name="function-test-testcancelproposal-88705"></a>[test\_cancelProposal](#function-test-testcancelproposal-88705)

> : Script ()
>
> Test to cancel a proposal

<a name="function-test-testarchivechoicetrainingproposal-51411"></a>[test\_archiveChoice\_TrainingProposal](#function-test-testarchivechoicetrainingproposal-51411)

> : Script ()
>
> This is just to test the "Archive" default choices if working
> can be use if only needed; for now we are expecting the "CancelProposal" choice to be use via Training Rights.
> This 'archive' choice can be use during further extension of application.

<a name="function-test-testarchivechoiceapprovedtraining-30840"></a>[test\_archiveChoice\_ApprovedTraining](#function-test-testarchivechoiceapprovedtraining-30840)

> : Script ()
>
> This is just to test the "Archive" default choices if working
> This 'archive' choice can be use during further extension of application.

<a name="function-test-testarchivechoicetrainingrights-48386"></a>[test\_archiveChoice\_trainingRights](#function-test-testarchivechoicetrainingrights-48386)

> : Script ()
>
> This is just to test the "Archive" default choices if working
> This 'archive' choice can be use during further extension of application.
