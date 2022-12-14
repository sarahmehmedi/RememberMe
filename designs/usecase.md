# Account Recovery

>NOTE: Update title and remove all Template Instructions.
 
#### Table of Contents
- [Account Retrieval](#use-case-story-title) 
      - [Table of Contents](#table-of-contents)
  - [Acknowledgements](#acknowledgements)
  - [Business Challenge](#business-challenge)
    - [Concept](#concept)
    - [Approach](#approach)
  - [Vernacular](#vernacular)
  - [Assumptions](#assumptions)
  - [Persona](#persona)
  - [Story](#story)
  - [Demo Workflow](#demo-workflow)
    - [Step 1](#step-1)
    - [Step 2](#step-2)

 
## Acknowledgements

>Template Instructions: List any acknowledgements pertaining to the concepts and resources used in this use case story.
 
1. This scenario leverages a fictitious company called, _Acme Enterprise_. The <img src="./images/persona/acme-logo.png" width="50" height="40"> Acme Enterprise logo is borrowed from [Katie Wickens](https://steins_kake.artstation.com/projects/ebqgb), a graphics designer.
 
## Business Challenge
The Account Recovery process is a common target for fraudsters. If the process is too simple, then it will quickly result in an account take-over. At the same time, it is a common pain point for legitimate customers. Asking customers to enter lot of data is error prone and can lead to a frustrating experience, as can requiring them to go through numberous steps just to regain access to their account. 

Digital wallets are starting to gain acceptance. The Department of Motor Vehicles (DMV) in some states already allow the creation of digital driver's licenses. Imagine a time where a user has already created a digital driver's license which they can now use to effortlessly recover their account.
 
### Concept
The issuer which is DMV in our cases issues the verifiable Digital credential, the license for the customer. The credentials will be stored in the Digital wallet for the customer. During the account recovery process, Discover would verify the Credentials that are shared by the customer along with the public key of the issuer that will be available in the Block chain or any other public registry. 
 
### Approach
![trust-triangle](./images/misc/triangle.png)

Johnny Customer (Owner/Holder) - This is a customer that has registered an account with Discover and the DMV. They hold a Digital key in their Digital wallet that contains their driver???s license information.

DMV (Issuer) - This issuer is a DMV that has received Johnny Customer???s information to validate that they are who they say they are, and the issuer has issued a digital driver's license for them to be stored in their digital wallet for them to use.

Discover (Verifier) - This is Discover, we use a customer???s digital driver's license to link their identity to their account, since it comes from a credible issuer, we trust that information and let the user recover their account.

 
## Vernacular
 
1. **Digital Wallet**: A financial transaction application that runs on multiple device modalities (mobile, computer). These applications store, manage, and present payment and identity instruments.
2. **Account Recovery Process**: Discover Web/Mobile flow which kickstarts when the Customer Forgot Password/Forgot UserId/Forgot Both.
3. **Issuer**: A entity that makes assertions about information and delivers digital credentials containing attestations about those assertions.
4. **Credential Generator**: A software component used by the Issuer to manage the generation of new digital credentials.
5. **Credential Issuer Utility**: An Issuer would augment their Credential Generator with support by a vendor solution that allows Issuers to publish a digital credential to consumers.
6. **Public Registry**: A public utility that allows for the registration and discovery of Decentralized Identifiers (DIDs).
6. **Sovrin Network** : The first public-permissioned blockchain designed as a global public utility exclusively to support self-sovereign identity and verifiable claims.
 
## Assumptions
 
1. Use case assumes knowledge of the W3C Standards and open source software that supports the concepts outlined by the [Trust over IP Foundation](https://trustoverip.org/toip-model/).
2. Credential Issuer and Verifier Utility solutions are readily available from 3rd party vendors.
 
## Persona

| Actor | Role | Goals | Details |
| --- | --- | --- | --- |
| <img src="./images/persona/discover_logo.png" width="60" height="60"> | Verifier | Verify the Credentials that are shared by the customer along with the public key of the issuer that will be available in the Block chain or any other public registry. | Ensure that the customers are able to go through the account recovery process without providing their individual details and authenticating the customer with the digital credential provided  |
|  <img src="./images/persona/DMV.jpg" width="50" height="40">  | Issuer | Issue the verifiable credential which is nothing but Driver's License for the customer. | Capabale of providing the Driver's license as a digital credential with the help of the Digital trust vendors  |
| <img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny | Consumer | Accept the credential from the issuer and Share it with the Verifier to be authenticated during the account recovery.  | Registered Customer of Discover who has the ability to hold the Driver's license as a Digital crendential in the Digital wallet and also have the ability to access the Discover account recovery process and provide the credential when promped. |
 
## Story

### Step 1
<img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny Customer completes registration for an account with <img src="./images/persona/discover_logo.png" width="60" height="60"> Discover
 
 
### Step 2
 
After login, <img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny is prompted to set up a digital driver's license with <img src="./images/persona/DMV.jpg" width="50" height="40"> DMV
 
 
### Step 3

<img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny set up the digital driver???s license through the <img src="./images/persona/DMV.jpg" width="50" height="40"> DMV website and his driver???s license is saved to his digital wallet (ConnectMe)


### Step 4

<img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny forgets his login information for his <img src="./images/persona/discover_logo.png" width="60" height="60"> Discover account and decides to go through the forgot password flow


### Step 5

<img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny is prompted to scan a QR code with his digital wallet app (ConnectMe) to send his digital drivers license details to <img src="./images/persona/discover_logo.png" width="60" height="60"> Discover for verification


### Step 6

<img src="./images/persona/discover_logo.png" width="60" height="60"> Discover retrieves these digital attributes from ConnectMe and proceeds to verify on the backend that the information matches an account


### Step 7 

<img src="./images/persona/discover_logo.png" width="60" height="60"> Discover matches the digital credentials with an account and <img src="./images/persona/johnny.jpg" width="40" height="40"> Johnny is sent to reset his password - he is now a happy customer again



 
## Demo Workflow

![uml-diagram](./images/uml/UML-Diagram.png)

