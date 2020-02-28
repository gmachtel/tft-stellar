## Activation of new accounts on Stellar

### Problem

New accounts on Stellar all need to have a trustline to an issuer. There is a cost linked to this creation of about 2.6 XLM (trustline, trustline trx fee). 
For converted accounts coming from tfchain, the funding of these accounts is part of the conversion process, funding comes from a fixed TF wallet. 

In 3Bot, there are different wallets offered: 
- a daily wallet, with seed key derived from 3bot seed
- a savings wallet, with seed key derived from 3bot seed
- a wallet can be imported with its own seed key

The reservation of XLM funds by a TF wallet is only supported for wallets that exist on the TFchain. 
New wallets (but that includes all 3bot wallets without transaction history on tfchain and zero balance) won't go through a conversion process.
That implies also that no trustlines will be created for these ones.

Also, any new 3Bot created will only be able to have an active wallet address once the trustline to the TFT issuer has been set up. Preliminary funding is needed for that. 

### Proposed solution: why ?

We want to avoid too many unnecessary reservations of XLM, as well as abuse of the TF XLM wallet funding by generating a multitude of Stellar accounts without real usage.

### Proposal

Any second address within a Threebot that is unused so far (i.e. does not show any transactions on TFchain and that does not hold a balance on Stellar) gets a "Activation" button. 
As cost for setting up such an address is about 2.6 XLM (is about 0.15 USD at current price), we could define a funding service against a cost of 1 TFT (to be agreed), to be funded by TFTs available on another account within the 3bot wallet.

The funding service would then pay the required XLMs to make the address active on Stellar. 
