---
layout: post

redirect_from: /2021/03/17/a-supervisory-framework-ensuring-consumer-protections-for-psd2-payments
author: by Mike Kelly (mike@hafini.group)
title: A supervisory framework ensuring consumer protections for PSD2 payments in the UK
---
This paper details the principles of how PSD2 payments, including Variable Recurring Payments (VRPs), are treated under existing regulation. In doing so it, demonstrates the safety of PSD2 payments for consumers due to:

1. The obligation of firms conducting PSD2 payments to ensure consumers are appropriately protected.
2. The array of ways in which PSD2 payments enable strong protection of customers, by providing high assurance risk control mechanisms to regulated firms.

The paper concludes with a framework on consumer protection for PISP payments, that can be issued as additional guidance for regulated firms. The framework is derived from [OBIE’s VRP Proposition consultation paper](https://www.openbanking.org.uk/wp-content/uploads/OBIE-VRP-Proposition.pdf).


## PSD2 payments can only be conducted by licensed PISPs

In order to conduct any payments activity under PSD2, the organisation must hold a license granted by the FCA to operate as a PISP. Getting a PISP license is a significant undertaking that requires firms to carefully detail their intended business models, activities, risks, and risk controls - all of which are reviewed by the regulator before a license is granted.

Access to instruct payments under PSD2 is highly secure since they can only be instructed when accompanied by a secure digital certificate from the PISP, which the ASPSP cryptographically verifies before honouring the request. Those certificates uniquely identify the firm and are only issued to firms with a PISP license reflected in the FCA’s register. Additionally, the use of digital certificates leaves behind unforgeable signatures on each payment which creates “non-repudiation” between PISP and ASPSP; establishing irrefutable proof of PISP responsibility for each payment instruction they make on behalf of the PSU.


## VRPs are regulated PISP activity under PSD2

VRPs are an emerging form of payment activity, possible through an ASPSP dedicated interface (sometimes referred to as “Open Banking APIs”). VRP activity is classified under PSD2 in the UK as a form of PISP activity, and this has been confirmed through formal correspondence between the FCA and the OBIE Trustee.

VRPs are classified a form of “Continuous Payment Authority” (CPA), and should be treated as such by all regulated firms. This includes rules on CPAs defined in the FCA's [Consumer Credit sourcebook (CONC)](https://www.handbook.fca.org.uk/handbook/CONC).

## PISPs are licensed and supervised by the FCA

As well as having to gain their license to operate, PISPs must retain that license whilst conducting their activity under the supervision of the financial regulator. This involves, amongst other things, continual reporting and disclosures of anything which the regulator would reasonably expect notice about - as per principle 11 of the FCA’s Principles for Business. This is to ensure that, as the business of a PISP evolves, the firm assists the regulator in continually monitoring their activities and ensuring they are meeting obligations to protect consumers and control risk.


## PISPs have obligations to appropriately protect consumers and control risk for their activities.

PISPs are regulated financial institutions that, through the regulatory framework set out by the FCA, are obliged to control risk and protect consumers. One foundational element of this is the FCA’s Principles for Business, which applies to any regulated firm, for example:


*   Principle 3: “A firm must take reasonable care to organise and control its affairs responsibly and effectively, with adequate risk management systems.”
*   Principle 6: “A firm must pay due regard to the interests of its customers and treat them fairly.”
*   Principle 8: “A firm must manage conflicts of interest fairly, both between itself and its customers and between a customer and another client.”

The regulator ensures these principles are adhered to through the license application process and the continual monitoring and supervision of PISP activity.

It is not the responsibility of regulators to prescribe specific approaches. Rather, it is the responsibility of the PISP to identify the relevant risk factors for their specific activities, and to develop appropriate risk controls that mitigate the relevant risk factors. The regulator’s role is to evaluate the approach proposed by a PISP, identify any potential flaws, and in cases where there is inadequate risk management, to use its powers to ensure that this is remedied by the firm.

The FCA leads the world in effective regulation; part of this reputation is built upon the consumer centric, outcomes based approach. As such, there are very strong assurances on consumer protections, and the control of risk, underpinning all PISP activity.

The remainder of this document, provides a framework on consumer protection for PISP payments that can be issued as additional guidance for regulated firms.


# Risk-based framework for consumer protections for PISP payments

The following is a framework, suitable for issuing as guidance to regulated firms, which lays out how they are expected to identify and control consumer protections for PISP activities, under supervision of the regulator.

It is based on the risk factors related to PISP payments and risk control mechanisms available to regulated actors. These elements were identified by [OBIE’s VRP Proposition consultation paper](https://www.openbanking.org.uk/wp-content/uploads/OBIE-VRP-Proposition.pdf).

Regulated actors must consider the risk factors as they apply to their specific activities, and mitigate them appropriately by employing the available risk control mechanisms. These risk considerations are a fundamental basis by which the FCA evaluates license applications and supervises ongoing activity.


## Risk Factors for PISP activity



*   Payments to a counterparty
*   Recoverability of funds
*   Money Laundering and Terrorist Financing (MLTF)
*   Misattribution of destination account ownership & APP scams


## Risk Factors for PISP VRP activity



*   Customer presence for VRP payments with an SCA Exemption
*   Permissiveness of consent parameters
*   Erosion of PSU consent over time


## Risk control mechanisms for PISP activity



*   PSD2 liability model
*   PISP-PSU contract
*   ASPSP-PSU contract
*   ASPSP-PISP contract
*   Non-repudiation between ASPSP and PISP for payment instruction
*   PISP attestations to nature of individual payment
*   Arbitration and dispute processes
*   Validation of destination account ownership


## Risk control mechanisms for PISP VRP activity



*   Consent parameters
*   Non-repudiation between ASPSP and PISP for granting of consent
*   PSU revocation of access at the ASPSP
*   PSU revocation of consent at the TPP
*   Monitoring and reporting on permissiveness of consent parameters
*   Monitoring for dormant consents
*   Consent and Access Dashboards
*   Notification of VRP Payments to PSU


## Risk Factor Considerations


### Customer presence for VRP payments with an SCA Exemption

If the use case requires that the customer is “not in session” for the instruction of an individual VRP payment (i.e. does not perform SCA of the PSU and relies on the application of an available SCA exemption), then there is increased risk of customer dispute because the PISP may instruct a payment on behalf of the PSU which the PSU would dispute. We note that this risk factor does not apply to VRP Payments with delegated SCA.


### Permissiveness of consent parameters

The more permissive a given VRP Consent’s consent parameters are, the greater the risk associated with managing that VRP Consent, for example:

*   a large maximum amount per payment
*   a very distant expiry date (or no expiry date at all)

PISPs should ensure that the consent parameters they negotiate with the PSU are not unnecessarily or unreasonably permissive. Consent parameters that are unreasonably permissive would be inappropriate for VRP Payments with an SCA exemption, since that would compromise the PISP’s ability to treat each payment as if it had explicit consent from the PSU.


### Payments to a counterparty

PISP Payments to a counterparty (i.e. where the payer is different from the payee) involve counterparty risks and therefore increased likelihood for dispute. This is particularly true for “consumer payment” use cases, where contracts should set out terms to both parties and establish a suitable dispute process with sufficient protections.

### Recoverability of funds

If the destination account of the PISP Payment carries with it more difficulty in recovering funds (e.g. long term savings accounts), then the increased challenge in reversing the flow of funds for payments made in error represents increased risk.

### Money Laundering and Terrorist Financing (MLTF)

PISPs are regulated financial institutions and are obligated to control all MLTF risks relating to their regulated activities.

### Erosion of PSU consent over time

The risk that a PSU loses awareness of a VRP Consent or is unable to manage it appropriately over time. This forms part of a PISP’s duty of care to customers, and they should ensure:

*   PSUs are notified appropriately of VRP Payments (before and/or after, dependent on use case)
*   PSUs are offered appropriate mechanisms for managing the VRP Consent over time (eg. by offering the consent dashboard interface defined in the OBIE VRP Standard)


### Misattribution of destination account ownership & APP scams

The risk that the ownership of the destination account is misattributed, a payment is made to an account that is not in the name of the recipient intended by the PSU, and the potential for customer detriment to arise as a result. Failing to control for this risk could facilitate APP scams. PISPs must develop risk controls that appropriately mitigate these risks as part of their duty of care to the customer.


## Risk Control Mechanism Considerations


### PSD2 liability model

PISP activity is regulated activity. PSD2/ PSRs provides a base liability framework.


### Consent parameters

The VRP consent that is granted by the PSU to the PISP can include a set of agreed parameters that constrain the use of the consent (e.g. specifying the destination account, limiting the amount, expiry date, etc). This provides transparency and assurance to the PSU by allowing them to agree to payments within specific limitations.


### PISP-PSU contract

A service contract between the PISP and PSU can provide additional protections and assurances to customers on top of the PSD2 liability model.


### ASPSP-PSU contract

A framework contract between the ASPSP and PSU can provide additional protections and assurances to customers.


### ASPSP-PISP contract

A contract between ASPSP and PISP can establish terms of liability, risk controls, consumer protection rules, and dispute processes.


### Non-repudiation between ASPSP and PISP for granting of consent and individual payments

Payments under the Open Banking standard require PISPs and ASPSPs to sign their API requests and responses. Message signing provides PISPs and ASPSPs with cryptographic attestation and proof of their interactions, which acts as a risk control by establishing non-repudiation between ASPSP and PISP.


### PISP attestations to nature of individual payment

When making a VRP Payment, PISPs can attest to the nature of the payment. This signalling helps assure ASPSPs that the nature of the activity is as agreed under the terms of access granted to the PISP.


### PSU revocation of access at the ASPSP

PSUs are granted full visibility and control over all the variable recurring payment access given by the PSU to all PISPs on the access dashboard. This enables the PSU to review and revoke specific access given to PISPs.


### PSU revocation of consent at the TPP

PSUs are granted full visibility and control over all VRP Consents given to an individual PISP at one or more ASPSPs via the consent dashboards. This enables the PSU to review and revoke specific VRP consents given at different ASPSPs.


### Arbitration and dispute processes

PISPs can establish processes that define how arbitration and dispute are managed for payments that involve counterparty risk. Consumer protections should be included in these processes and afforded by the PISP to PSUs under contract.


### Monitoring and reporting on permissiveness of consent parameters

PISPs should monitor and report metrics that indicate the degree to which consent parameters are exercised to help ensure that the limits are not unnecessarily or unreasonably permissive.


### Monitoring for dormant consents

PISPs should monitor for VRP Consents that are dormant and remain unused. When a dormant consent is identified, PISPs should make a risk based decision about whether to notify the customer and/or revoke the consent.


### Consent and Access Dashboards

To address the potential erosion of PSU consent over time, PSUs should be offered “dashboards” to review and manage VRP activities associated with their account. More specifically:

*   ASPSPs should offer the PSU an access dashboard to manage all VRP access to account.
*   PISPs should offer the PSU a consent dashboard to manage the VRP Consents granted to the PISP.


### Notification of VRP Payments to PSU

PISPs should notify the PSU of VRP Payments. Notifications may be issued before or after a VRP Payment, depending on what is most appropriate for the specific use case in question.


### Validation of destination account ownership

In order to mitigate the risk that the ownership of the destination account is misattributed, PISPs should take reasonable steps to ensure that the ownership of the destination account is in line with the expectations of the PSU. Failure to take appropriate steps exposes the PSU to risks such as APP scams, and would represent a dereliction in the PISP’s duty of care to customers.
