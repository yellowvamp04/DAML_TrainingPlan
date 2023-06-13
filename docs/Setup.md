# <a name="module-setup-53573"></a>Setup

## Data Types

<a name="type-setup-testparties-37364"></a>**data** [TestParties](#type-setup-testparties-37364)

> data record that will hold all test parties
>
> <a name="constr-setup-testparties-76451"></a>[TestParties](#constr-setup-testparties-76451)
>
> > | Field                                                                                   | Type                                                                                    | Description |
> > | :-------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :---------- |
> > | issuer                                                                                  | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | proposer                                                                                | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | supervisor                                                                              | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | trainingTeam                                                                            | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | employeeLevel1                                                                          | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | employeeLevel2                                                                          | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
> > | employeeLevel3                                                                          | [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932) |  |
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "employeeLevel1" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "employeeLevel2" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "employeeLevel3" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "issuer" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "proposer" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "supervisor" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)
>
> **instance** [HasField](https://docs.daml.com/daml/stdlib/DA-Record.html#class-da-internal-record-hasfield-52839) "trainingTeam" [TestParties](#type-setup-testparties-37364) [Party](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932)

## Functions

<a name="function-setup-setuptestparties-70170"></a>[setupTestParties](#function-setup-setuptestparties-70170)

> : Script [TestParties](#type-setup-testparties-37364)
>
> Allocate parties with the given display name

<a name="function-setup-setupusers-15488"></a>[setupUsers](#function-setup-setupusers-15488)

> : Script ([TestParties](#type-setup-testparties-37364), [ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingRights](Main.html#type-main-trainingrights-63033))
>
> Setup users with rights

<a name="function-setup-setupinitcontracts-48099"></a>[setupInitContracts](#function-setup-setupinitcontracts-48099)

> : [TestParties](#type-setup-testparties-37364) -\> Script ([ContractId](https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282) [TrainingRights](Main.html#type-main-trainingrights-63033))
>
> setup initial training rights contract for the proposer
