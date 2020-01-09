# Radish34 SNARK circuit
Given a commitment `C` to a universal data structure and its public inputs, the SNARK proves the following:
- 1. Well formation of the commitment
- 2. Knowledge of the secret key of the sender based on his public key provided inside `C`
- 3. Verification of the recipient's signature (without revealing his identity) of some data inside `C`

The number of public inputs and their sizes is defined in the sequel following the buisiness logic and technical choices rationales.

## The commitment
The commitment `C` is the following:

`C = {ø, id, idEntangled, metada, logicVerifier, state, ownerAddress, recipientAddress, recipientSignature}`

where:
- `ø`: a random salt
- `id`: the identifier of the document (RFQ, MSA, PO, invoice)
- `idEntangled`: the identifier of the entangled document (`Null`, RFQ, MSA, PO for respectivele RFQ, MSA, PO, invoice)
- `metada`: the tx metada (cf. Radish34 design document)
- `logicVerifier`: the opcode for a function of the smart contract
- `state`: to know what the ability to reference a comitment in the entangle id is
- `ownerAddress`: the public key of the sender
- `recipientAddress`: the public key of the recipient
- `recipientSignature`: the recipient's signature of `(ø||id||idEntangled||metada||logicVerifier||state)` where `||` stands for concatenation

the sizes of these field will be defined in the sequel according to the technical choices rationale.

## Buisiness logic rationale

## Technical choices rationale

## Security considerations
