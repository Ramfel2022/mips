# MIP14: Protocol DAI Transfer

## Preamble

```
MIP#: 14
Title: Protocol DAI Transfer
Author(s): @LongForWisdom, @jtathmann
Contributors: N/A
Tags: process, governance, living
Type: Process
Status: Obsolete
Date Proposed: 2020-05-12
Date Ratified: 2020-10-27
Dependencies: MIP0
Replaces: N/A
Ratification Poll URL:
Forum URL: https://forum.makerdao.com/t/mip17-weekly-actual-debt-ceiling-and-actual-risk-premium-adjustments/3021
Extra: This MIP has been amended via [MIP4c2-SP32](https://mips.makerdao.com/mips/details/MIP4c2SP32). The previous version can be found [here](https://github.com/makerdao/mips/blob/7c48429e6362a7a16861dc328ec9a4978dd2e3f9/MIP14/mip14.md.
Extra: This MIP has been made obsolete by the passage of [MIP102c2-SP1](https://mips.makerdao.com/mips/details/MIP102c2SP1)
```

## References

**[MIP14c2-Subproposal-Template.md](MIP14c2-Subproposal-Template.md)**
**[MIP14c4-Subproposal-Template.md](MIP14c4-Subproposal-Template.md)**

## Sentence Summary

MIP14 defines a generic process for transferring DAI from the Maker Protocol to a target Ethereum address.

## Paragraph Summary

MIP14 defines a generic process for transferring DAI from the Maker Protocol to a target Ethereum address. This process is a fallback method of transferring value from the protocol in the event that a more specific process does not exist to do so.

## Component Summary

**MIP14c1: Considerations Regarding Protocol DAI Transfers**
A component which outlines the various considerations that should be made before transferring DAI out of the protocol using MIP14c2.

**MIP14c2: Protocol DAI Transfer Process**
A process component that allows Maker Governance to transfer DAI from the Maker Protocol to a target Ethereum address.

**MIP14c3: Protocol DAI Transfer List**
A list component that lists the previous direct DAI transfers that have been made by the protocol in the past.

## Motivation

Giving governance the ability to use the value generated by the Maker Protocol is beneficial for two main reasons:

* It allows Maker Governance to incentivize actions taken to improve the protocol.
* It reduces Maker Governance's reliance on the Maker Foundation.

Less reliance on the Foundation moves the protocol towards decentralization. Creating a process to allow Maker Governance to spend the value accrued by the protocol empowers Maker Governance to build and improve the protocol in the future.

## Specification / Proposal Details

### MIP14c1: Considerations Regarding Protocol DAI Transfers

There are several important considerations to take into account before transferring value out of the Maker Protocol.

* Transfer of DAI from the protocol to an external address that is not controlled by Maker Governance is a one-way operation.
* Transfer of DAI from the protocol will take DAI from the surplus buffer if available.
* If there is insufficient DAI available in the surplus buffer unbacked DAI will be created and FLOP auctions will be able to be triggered immediately.
* If there is a more specific process MIP that allows DAI transfers that is more appropriate to the use case, use that process instead.

### MIP14c2: Protocol DAI Transfer Process

MIP14c2 is a Process MIP component that allows Maker Governance to transfer DAI from the Maker Protocol to a target Ethereum address. Note that MIP14c2 subproposals are technical subproposals, they define executive code that transfers DAI from the Maker Protocol to one or more target addresses.

If a MIP14c2 subproposal is Accepted, The DAI Transfer is appended to the list in MIP14c3 by a MIP Editor.

MIP14c2 subproposals have parameters that depend on the total amount of DAI to be transferred (even if split among multiple target addresses) according to the following logic:

**< 10,000 DAI Transfer**

* **Feedback Period:**  0 full weeks
* **Frozen Period:**  0 full weeks

**10,000 - 100,000 DAI Transfer**

* **Feedback Period:**  4 full weeks
* **Frozen Period:**  1 full week

**> 100,000 DAI Transfer**

* **Feedback Period:**  12 full weeks
* **Frozen Period:**  4 full weeks

If a MIP14c2 subproposal would result in a FLOP auction, Governance Facilitator(s) will use established communication channels to ensure the community is informed

MIP14c2 subproposals must use the template located at  **[MIP14c2-Subproposal-Template.md](https://github.com/makerdao/mips/blob/master/MIP14/MIP14c2-Subproposal-Template.md)** . This template is considered ratified once this MIP moves to Accepted status.

### MIP14c3: Protocol DAI Transfer List

This list can be amended through subproposals created under MIP14c2.

**List Entry Template**  Entries into this list should follow the following template:

```
Reason:
Sub-proposal Number: #
Date Ratified: (yyyy-mm-dd)
Amount Transferred:
Recipient Address:
```

#### Historical Transfer List  

##### MIP14c3-SP1

- Reason: Fund TechOps CU (TECH-001) through the month of February 2023.
- Sub-proposal Number: 1
- Date Ratified: 2023-01-23
- Amount Transferred: 138,894 DAI
- Recipient Address: 0x2dC0420A736D1F40893B9481D8968E4D7424bC0B


##### MIP14c3-SP2

- Reason: Fund Immunefi Security CU (IS-001) from December 2022 to May 2023.
- Sub-proposal Number: 2
- Date Ratified: 2023-01-23
- Amount Transferred: 43,560 DAI
- Recipient Address: 0xd1F2eEf8576736C1EbA36920B957cd2aF07280F4



