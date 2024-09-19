Run a MFEV Validator
Setting up a node
Git clone Validator

Create an Account

chmod +x openethereum
./openethereum account new --config ./node.toml
Returned address like that 0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2

Copy result address to mode.toml Ex:

...
[account]
unlock = ["0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"]
password = ["password"]

[mining]
force_sealing = true
engine_signer = "0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"
reseal_on_txs = "none"
...
Run the authority nodes
./openethereum --config ./node.toml

Stake

Stake

To stake MFEV coin, all you should do is sending your MFEV coin to the MFEV Consensus contract address over the MBC network from the validator address. The MFEV Consensus contract address: 0xa0B4785393F6855b12F1bb99C58d8498E1E15cc2 The easiest way to do so, is to import your private key or key-store file to your favourite wallet (for example Metamask), switch network to MBC and send the MFEV coin to the Consensus contract address.

You can find your key-store (containing your private key) and the password for the created account in: /node/keys/MFEV/UTC--xxxx /node.pwd

Wait for 1 cycle (approximately 48 hours).

Wait until the next cycle gets started.
