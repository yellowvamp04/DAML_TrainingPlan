# <a name="module-main-6666"></a>Main

## Templates

<a name="type-main-training-27114"></a>**template** [Training](#type-main-training-27114)

> holds the approved Trainings that can already be published to the expected audiences
> this can be use for registration purposes (but that is currently out of scope for now)
> assumption: published date pass is the current date
>
> | Field                                                                                                                                                                                    | Type                                                                                                                                                                                     | Description |
> | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
> | proposer                                                                                                                                                                                 | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)                                                                                                  |  |
> | supervisor                                                                                                                                                                               | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)                                                                                                  |  |
> | approvalDate                                                                                                                                                                             | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)                                                                                                    |  |
> | trainingTeam                                                                                                                                                                             | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)                                                                                                  |  |
> | trainingPlan                                                                                                                                                                             | [TrainingPlan](#type-main-trainingplan-58995)                                                                                                                                            |  |
> | published                                                                                                                                                                                | [Bool](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-bool-66265)                                                                                                         |  |
> | publishedDate                                                                                                                                                                            | [Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253) |  |
> | audience                                                                                                                                                                                 | \[[Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)\]                                                                                              |  |
>
> * **Choice Archive**
>
>   (no fields)
>
> * **Choice Publish**
>
>   | Field                                                                                                                                                                                    | Type                                                                                                                                                                                     | Description |
>   | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
>   | publishedDate                                                                                                                                                                            | [Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253) |  |

<a name="type-main-trainingplanproposal-90777"></a>**template** [TrainingPlanProposal](#type-main-trainingplanproposal-90777)

> template that is created to propose the training plan to the proposer's supervisor
>
> | Field                                                                                                                                                                               | Type                                                                                                                                                                                | Description |
> | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
> | proposer                                                                                                                                                                            | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)                                                                                             |  |
> | supervisor                                                                                                                                                                          | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)                                                                                             |  |
> | proposalDate                                                                                                                                                                        | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)                                                                                               |  |
> | trainingPlan                                                                                                                                                                        | [TrainingPlan](#type-main-trainingplan-58995)                                                                                                                                       |  |
> | status                                                                                                                                                                              | [ProposalStatus](#type-main-proposalstatus-77050)                                                                                                                                   |  |
> | supervisorNotes                                                                                                                                                                     | [Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952) |  |
>
> * **Choice Approve**
>
>   | Field                                                                                   | Type                                                                                    | Description |
>   | :-------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :---------- |
>   | trainingTeam                                                                            | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
>   | approvalDate                                                                            | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)   |  |
>
> * **Choice Archive**
>
>   (no fields)
>
> * **Choice CancelProposal**
>
>   (no fields)
>
> * **Choice Reject**
>
>   | Field                                                                                                                                                                               | Type                                                                                                                                                                                | Description |
>   | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
>   | supervisorNotes                                                                                                                                                                     | [Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952) |  |
>
> * **Choice UpdateProposal**
>
>   | Field                                         | Type                                          | Description |
>   | :-------------------------------------------- | :-------------------------------------------- | :---------- |
>   | updatedTrainingPlan                           | [TrainingPlan](#type-main-trainingplan-58995) |  |

<a name="type-main-trainingrights-63033"></a>**template** [TrainingRights](#type-main-trainingrights-63033)

> template that can be use by a proposer to create proposals
> assumption: proposal date pass is the current date
>
> | Field                                                                                   | Type                                                                                    | Description |
> | :-------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :---------- |
> | issuer                                                                                  | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> | employee                                                                                | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
>
> * **Choice Archive**
>
>   (no fields)
>
> * **Choice CheckApproveTrainingViaCid**
>
>   | Field                                                                                                                                   | Type                                                                                                                                    | Description |
>   | :-------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
>   | cid                                                                                                                                     | [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [Training](#type-main-training-27114) |  |
>
> * **Choice CheckProposalViaCid**
>
>   | Field                                                                                                                                                           | Type                                                                                                                                                            | Description |
>   | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
>   | cid                                                                                                                                                             | [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingPlanProposal](#type-main-trainingplanproposal-90777) |  |
>
> * **Choice CheckViaTitle**
>
>   | Field                                                                                | Type                                                                                 | Description |
>   | :----------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------- | :---------- |
>   | titles                                                                               | \[[Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)\] |  |
>
> * **Choice CreateTrainingPlanProposal**
>
>   | Field                                                                                   | Type                                                                                    | Description |
>   | :-------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :---------- |
>   | trainingPlan                                                                            | [TrainingPlan](#type-main-trainingplan-58995)                                           |  |
>   | proposalDate                                                                            | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)   |  |
>   | supervisor                                                                              | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |

## Data Types

<a name="type-main-proposalstatus-77050"></a>**data** [ProposalStatus](#type-main-proposalstatus-77050)

> holds the available status for a proposal
> proposal that is already approved will be archived and a separate Training contract will be created instead (so no need to have "approved" status here)
>
> <a name="constr-main-pending-86225"></a>[Pending](#constr-main-pending-86225)
>
>
> <a name="constr-main-rejected-65933"></a>[Rejected](#constr-main-rejected-65933)
>
>
> <a name="constr-main-updated-25317"></a>[Updated](#constr-main-updated-25317)
>
>
> **instance** [Eq](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713) [ProposalStatus](#type-main-proposalstatus-77050)
>
> **instance** [Show](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360) [ProposalStatus](#type-main-proposalstatus-77050)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "status" [TrainingPlanProposal](#type-main-trainingplanproposal-90777) [ProposalStatus](#type-main-proposalstatus-77050)

<a name="type-main-trainingplan-58995"></a>**data** [TrainingPlan](#type-main-trainingplan-58995)

> holds the details of the training plan
> possible updates here is to add in optional fees, needed budget, location etc. (which are out of scope as of now)
>
> <a name="constr-main-trainingplan-6084"></a>[TrainingPlan](#constr-main-trainingplan-6084)
>
> > | Field                                                                                                                                                                                   | Type                                                                                                                                                                                    | Description |
> > | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
> > | title                                                                                                                                                                                   | [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)                                                                                                        |  |
> > | courseDescription                                                                                                                                                                       | [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)                                                                                                        |  |
> > | objectives                                                                                                                                                                              | [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)                                                                                                        |  |
> > | preRequisites                                                                                                                                                                           | [Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) \[[Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)\] |  |
> > | audience                                                                                                                                                                                | \[[Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)\]                                                                                             |  |
> > | trainingType                                                                                                                                                                            | [TrainingType](#type-main-trainingtype-84846)                                                                                                                                           |  |
> > | startDate                                                                                                                                                                               | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)                                                                                                   |  |
> > | endDate                                                                                                                                                                                 | [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)                                                                                                   |  |
>
> **instance** [Eq](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713) [TrainingPlan](#type-main-trainingplan-58995)
>
> **instance** [Show](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360) [TrainingPlan](#type-main-trainingplan-58995)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "audience" [TrainingPlan](#type-main-trainingplan-58995) \[[Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)\]
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "courseDescription" [TrainingPlan](#type-main-trainingplan-58995) [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "endDate" [TrainingPlan](#type-main-trainingplan-58995) [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "objectives" [TrainingPlan](#type-main-trainingplan-58995) [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "preRequisites" [TrainingPlan](#type-main-trainingplan-58995) ([Optional](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153) \[[Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)\])
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "startDate" [TrainingPlan](#type-main-trainingplan-58995) [Date](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-date-32253)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "title" [TrainingPlan](#type-main-trainingplan-58995) [Text](https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingPlan" CreateTrainingPlanProposal [TrainingPlan](#type-main-trainingplan-58995)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingPlan" [Training](#type-main-training-27114) [TrainingPlan](#type-main-trainingplan-58995)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingPlan" [TrainingPlanProposal](#type-main-trainingplanproposal-90777) [TrainingPlan](#type-main-trainingplan-58995)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingType" [TrainingPlan](#type-main-trainingplan-58995) [TrainingType](#type-main-trainingtype-84846)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "updatedTrainingPlan" UpdateProposal [TrainingPlan](#type-main-trainingplan-58995)

<a name="type-main-trainingtype-84846"></a>**data** [TrainingType](#type-main-trainingtype-84846)

> holds the available types of training that can be proposed
> | virtual and classroom type of training can only be approved 1 week before it should start - to give way for preparation
>
> <a name="constr-main-virtual-94065"></a>[Virtual](#constr-main-virtual-94065)
>
>
> <a name="constr-main-classroom-69203"></a>[Classroom](#constr-main-classroom-69203)
>
>
> <a name="constr-main-online-55316"></a>[Online](#constr-main-online-55316)
>
>
> **instance** [Eq](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713) [TrainingType](#type-main-trainingtype-84846)
>
> **instance** [Show](https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360) [TrainingType](#type-main-trainingtype-84846)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingType" [TrainingPlan](#type-main-trainingplan-58995) [TrainingType](#type-main-trainingtype-84846)
