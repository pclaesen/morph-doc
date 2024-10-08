[**@morph-l2/sdk**](../globals.md) • **Docs**

***

[@morph-l2/sdk](../globals.md) / CrossChainMessenger

# Class: CrossChainMessenger

## Constructors

### new CrossChainMessenger()

> **new CrossChainMessenger**(`opts`): [`CrossChainMessenger`](CrossChainMessenger.md)

Creates a new CrossChainProvider instance.

#### Parameters

• **opts**

Options for the provider.

• **opts.backendURL?**: `string`

backend for withdraw proof gen.

• **opts.bridges?**: [`BridgeAdapterData`](../interfaces/BridgeAdapterData.md)

Optional bridge address list.

• **opts.contracts?**: [`DeepPartial`](../type-aliases/DeepPartial.md)\<[`OEContractsLike`](../interfaces/OEContractsLike.md)\>

Optional contract address overrides.

• **opts.l1ChainId**: [`NumberLike`](../type-aliases/NumberLike.md)

Chain ID for the L1 chain.

• **opts.l1SignerOrProvider**: [`SignerOrProviderLike`](../type-aliases/SignerOrProviderLike.md)

Signer or Provider for the L1 chain, or a JSON-RPC url.

• **opts.l2ChainId**: [`NumberLike`](../type-aliases/NumberLike.md)

Chain ID for the L2 chain.

• **opts.l2SignerOrProvider**: [`SignerOrProviderLike`](../type-aliases/SignerOrProviderLike.md)

Signer or Provider for the L2 chain, or a JSON-RPC url.

#### Returns

[`CrossChainMessenger`](CrossChainMessenger.md)

#### Source

src/cross-chain-messenger.ts:130

## Properties

### backendURL

> **backendURL**: `string`

Backend url for withdrawal prove server

#### Source

src/cross-chain-messenger.ts:76

***

### bridges

> **bridges**: [`BridgeAdapters`](../interfaces/BridgeAdapters.md)

List of custom bridges for the given network.

#### Source

src/cross-chain-messenger.ts:116

***

### contracts

> **contracts**: [`OEContracts`](../interfaces/OEContracts.md)

Contract objects attached to their respective providers and addresses.

#### Source

src/cross-chain-messenger.ts:111

***

### estimateGas

> **estimateGas**: `object`

Object that holds the functions that estimates the gas required for a given transaction.
Follows the pattern used by ethers.js.

#### approveERC20()

> **approveERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to approve some tokens to deposit into the L2 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L1 token address.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L2 token address.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of the token to approve.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### depositERC20()

> **depositERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to deposit some ERC20 tokens into the L2 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to deposit.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### depositETH()

> **depositETH**: (`amount`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to deposit some ETH into the L2 chain.

##### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to deposit.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### proveAndRelayMessage()

> **proveAndRelayMessage**: (`message`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to proveAndRelay a cross chain message. Only applies to L2 to L1 messages.

##### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to generate the proving transaction for.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### sendMessage()

> **sendMessage**: (`message`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to send a cross chain message.

##### Parameters

• **message**: [`CrossChainMessageRequest`](../interfaces/CrossChainMessageRequest.md)

Cross chain message to send.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### withdrawERC20()

> **withdrawERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to withdraw some ERC20 tokens back to the L1 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### withdrawETH()

> **withdrawETH**: (`amount`, `opts`?) => `Promise`\<`BigNumber`\>

Estimates gas required to withdraw some ETH back to the L1 chain.

##### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`BigNumber`\>

#### Source

src/cross-chain-messenger.ts:1600

***

### l1ChainId

> **l1ChainId**: `number`

Chain ID for the L1 network.

#### Source

src/cross-chain-messenger.ts:101

***

### l1CrossDomainMessenger

> **l1CrossDomainMessenger**: `Contract`

CrossDomainMessenger connected to the L1 chain.

#### Source

src/cross-chain-messenger.ts:91

***

### l1SignerOrProvider

> **l1SignerOrProvider**: `Provider` \| `Signer`

Provider connected to the L1 chain.

#### Source

src/cross-chain-messenger.ts:81

***

### l2ChainId

> **l2ChainId**: `number`

Chain ID for the L2 network.

#### Source

src/cross-chain-messenger.ts:106

***

### l2CrossDomainMessenger

> **l2CrossDomainMessenger**: `Contract`

CrossDomainMessenger connected to the L2 chain.

#### Source

src/cross-chain-messenger.ts:96

***

### l2SignerOrProvider

> **l2SignerOrProvider**: `Provider` \| `Signer`

Provider connected to the L2 chain.

#### Source

src/cross-chain-messenger.ts:86

***

### populateTransaction

> **populateTransaction**: `object`

Object that holds the functions that generate transactions to be signed by the user.
Follows the pattern used by ethers.js.

#### approveERC20()

> **approveERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?) => `Promise`\<`TransactionRequest`\>

Generates a transaction for approving some tokens to deposit into the L2 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L1 token address.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L2 token address.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of the token to approve.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`TransactionRequest`\>

#### depositERC20()

> **depositERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?, `isEstimatingGas`) => `Promise`\<`TransactionRequest`\>

Generates a transaction for depositing some ERC20 tokens into the L2 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to deposit.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

• **isEstimatingGas?**: `boolean`= `false`

##### Returns

`Promise`\<`TransactionRequest`\>

#### depositETH()

> **depositETH**: (`amount`, `opts`?, `isEstimatingGas`) => `Promise`\<`TransactionRequest`\>

Generates a transaction for depositing some ETH into the L2 chain.

##### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to deposit.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

• **isEstimatingGas?**: `boolean`= `false`

##### Returns

`Promise`\<`TransactionRequest`\>

#### proveAndRelayMessage()

> **proveAndRelayMessage**: (`message`, `opts`?) => `Promise`\<`TransactionRequest`\>

Generates a message proving and relaying transaction that can be signed and executed. Only
applicable for L2 to L1 messages.

##### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to generate the proving transaction for.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`TransactionRequest`\>

#### sendMessage()

> **sendMessage**: (`message`, `opts`?) => `Promise`\<`TransactionRequest`\>

Generates a transaction that sends a given cross chain message. This transaction can be signed
and executed by a signer.

##### Parameters

• **message**: [`CrossChainMessageRequest`](../interfaces/CrossChainMessageRequest.md)

Cross chain message to send.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

##### Returns

`Promise`\<`TransactionRequest`\>

#### withdrawERC20()

> **withdrawERC20**: (`l1Token`, `l2Token`, `amount`, `opts`?, `isEstimatingGas`?) => `Promise`\<`TransactionRequest`\>

Generates a transaction for withdrawing some ERC20 tokens back to the L1 chain.

##### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

• **isEstimatingGas?**: `boolean`

##### Returns

`Promise`\<`TransactionRequest`\>

#### withdrawETH()

> **withdrawETH**: (`amount`, `opts`?, `isEstimatingGas`?) => `Promise`\<`TransactionRequest`\>

Generates a transaction for withdrawing some ETH back to the L1 chain.

##### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

• **isEstimatingGas?**: `boolean`

##### Returns

`Promise`\<`TransactionRequest`\>

#### Source

src/cross-chain-messenger.ts:1304

## Accessors

### l1Provider

> `get` **l1Provider**(): `Provider`

Provider connected to the L1 chain.

#### Returns

`Provider`

#### Source

src/cross-chain-messenger.ts:193

***

### l1Signer

> `get` **l1Signer**(): `Signer`

Signer connected to the L1 chain.

#### Returns

`Signer`

#### Source

src/cross-chain-messenger.ts:215

***

### l2Provider

> `get` **l2Provider**(): `Provider`

Provider connected to the L2 chain.

#### Returns

`Provider`

#### Source

src/cross-chain-messenger.ts:204

***

### l2Signer

> `get` **l2Signer**(): `Signer`

Signer connected to the L2 chain.

#### Returns

`Signer`

#### Source

src/cross-chain-messenger.ts:226

## Methods

### approval()

> **approval**(`l1Token`, `l2Token`, `opts`?): `Promise`\<`BigNumber`\>

Queries the account's approval amount for a given L1 token.

#### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L1 token address.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L2 token address.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`BigNumber`\>

Amount of tokens approved for deposits from the account.

#### Source

src/cross-chain-messenger.ts:1214

***

### approveERC20()

> **approveERC20**(`l1Token`, `l2Token`, `amount`, `opts`?): `Promise`\<`TransactionResponse`\>

Approves a deposit into the L2 chain.

#### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L1 token address.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

The L2 token address.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of the token to approve.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the approval transaction.

#### Source

src/cross-chain-messenger.ts:1233

***

### depositERC20()

> **depositERC20**(`l1Token`, `l2Token`, `amount`, `opts`?): `Promise`\<`TransactionResponse`\>

Deposits some ERC20 tokens into the L2 chain.

#### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to deposit.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the deposit transaction.

#### Source

src/cross-chain-messenger.ts:1256

***

### depositETH()

> **depositETH**(`amount`, `opts`?): `Promise`\<`TransactionResponse`\>

Deposits some ETH into the L2 chain.

#### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to deposit (in wei).

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the deposit transaction.

#### Source

src/cross-chain-messenger.ts:1183

***

### encodeFunctionMessage()

> **encodeFunctionMessage**(`options`): `string`

L2CrossDomainMessenger contract encode message, such as hashCrossDomainMessagev1

#### Parameters

• **options**

• **options.message**: `string`

The message passed along with the cross domain message

• **options.messageNonce**: `BigNumber`

The cross domain message nonce

• **options.sender**: `string`

The sender of the cross domain message

• **options.target**: `string`

The target of the cross domain message

• **options.value**: `BigNumber`

The value being sent with the cross domain message

#### Returns

`string`

#### Source

src/cross-chain-messenger.ts:972

***

### estimateL2MessageGasLimit()

> **estimateL2MessageGasLimit**(`message`, `opts`?): `Promise`\<`BigNumber`\>

Estimates the amount of gas required to fully execute a given message on L2. Only applies to
L1 => L2 messages. You would supply this gas limit when sending the message to L2.

#### Parameters

• **message**: [`MessageRequestLike`](../type-aliases/MessageRequestLike.md)

Message get a gas estimate for.

• **opts?**

Options object.

• **opts.bufferPercent?**: `number`

Percentage of gas to add to the estimate. Defaults to 20.

• **opts.from?**: `string`

Address to use as the sender.

#### Returns

`Promise`\<`BigNumber`\>

Estimates L2 gas limit.

#### Source

src/cross-chain-messenger.ts:918

***

### getBackendTreeSyncIndex()

> **getBackendTreeSyncIndex**(): `Promise`\<`number`\>

#### Returns

`Promise`\<`number`\>

#### Source

src/cross-chain-messenger.ts:1122

***

### getBridgeForTokenPair()

> **getBridgeForTokenPair**(`l1Token`, `l2Token`): `Promise`\<[`IBridgeAdapter`](../interfaces/IBridgeAdapter.md)\>

Finds the appropriate bridge adapter for a given L1 - L2 token pair. Will throw if no bridges
support the token pair or if more than one bridge supports the token pair.

#### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

L1 token address.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

L2 token address.

#### Returns

`Promise`\<[`IBridgeAdapter`](../interfaces/IBridgeAdapter.md)\>

The appropriate bridge adapter for the given token pair.

#### Source

src/cross-chain-messenger.ts:378

***

### getCommittedL2BlockNumber()

> **getCommittedL2BlockNumber**(): `Promise`\<`any`\>

#### Returns

`Promise`\<`any`\>

#### Source

src/cross-chain-messenger.ts:995

***

### getDepositsByAddress()

> **getDepositsByAddress**(`address`, `opts`): `Promise`\<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

Gets all deposits for a given address.

#### Parameters

• **address**: [`AddressLike`](../type-aliases/AddressLike.md)

Address to search for messages from.

• **opts**= `{}`

Options object.

• **opts.fromBlock?**: `BlockTag`

Block to start searching for messages from. If not provided, will start
from the first block (block #0).

• **opts.toBlock?**: `BlockTag`

Block to stop searching for messages at. If not provided, will stop at the
latest known block ("latest").

#### Returns

`Promise`\<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

All deposit token bridge messages sent by the given address.

#### Source

src/cross-chain-messenger.ts:424

***

### getFinalizedL2BlockNumber()

> **getFinalizedL2BlockNumber**(): `Promise`\<`any`\>

#### Returns

`Promise`\<`any`\>

#### Source

src/cross-chain-messenger.ts:1017

***

### getMessageReceipt()

> **getMessageReceipt**(`message`, `opts`): `Promise`\<[`MessageReceipt`](../interfaces/MessageReceipt.md)\>

Finds the receipt of the transaction that executed a particular cross chain message.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to find the receipt of.

• **opts**= `{}`

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

#### Returns

`Promise`\<[`MessageReceipt`](../interfaces/MessageReceipt.md)\>

CrossChainMessage receipt including receipt of the transaction that relayed the
given message.

#### Source

src/cross-chain-messenger.ts:757

***

### getMessageStatus()

> **getMessageStatus**(`message`, `opts`): `Promise`\<[`MessageStatus`](../enumerations/MessageStatus.md)\>

Retrieves the status of a particular message as an enum.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Cross chain message to check the status of.

• **opts**= `{}`

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

#### Returns

`Promise`\<[`MessageStatus`](../enumerations/MessageStatus.md)\>

Status of the message.

#### Source

src/cross-chain-messenger.ts:634

***

### getMessagesByTransaction()

> **getMessagesByTransaction**(`transaction`, `opts`): `Promise`\<[`CrossChainMessage`](../interfaces/CrossChainMessage.md)[]\>

Retrieves all cross chain messages sent within a given transaction.

#### Parameters

• **transaction**: [`TransactionLike`](../type-aliases/TransactionLike.md)

Transaction hash or receipt to find messages from.

• **opts**= `{}`

Options object.

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

Direction to search for messages in. If not provided, will attempt to
automatically search both directions under the assumption that a transaction hash will only
exist on one chain. If the hash exists on both chains, will throw an error.

#### Returns

`Promise`\<[`CrossChainMessage`](../interfaces/CrossChainMessage.md)[]\>

All cross chain messages sent within the transaction.

#### Source

src/cross-chain-messenger.ts:244

***

### getProvenWithdrawal()

> **getProvenWithdrawal**(`withdrawalHash`): `Promise`\<[`ProvenWithdrawal`](../interfaces/ProvenWithdrawal.md)\>

Queries the L1CrossDomainMessenger contract's `provenWithdrawals` mapping
for a ProvenWithdrawal that matches the passed withdrawalHash

#### Parameters

• **withdrawalHash**: `string`

#### Returns

`Promise`\<[`ProvenWithdrawal`](../interfaces/ProvenWithdrawal.md)\>

A ProvenWithdrawal object

#### Source

src/cross-chain-messenger.ts:957

***

### getWithdrawMessageProof()

> **getWithdrawMessageProof**(`message`): `Promise`\<[`WithdrawMessageProof`](../interfaces/WithdrawMessageProof.md)\>

Generates the proof required to finalize an L2 to L1 message.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to generate a proof for.

#### Returns

`Promise`\<[`WithdrawMessageProof`](../interfaces/WithdrawMessageProof.md)\>

Proof that can be used to finalize the message.

#### Source

src/cross-chain-messenger.ts:1042

***

### getWithdrawalsByAddress()

> **getWithdrawalsByAddress**(`address`, `opts`): `Promise`\<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

Gets all withdrawals for a given address.

#### Parameters

• **address**: [`AddressLike`](../type-aliases/AddressLike.md)

Address to search for messages from.

• **opts**= `{}`

Options object.

• **opts.fromBlock?**: `BlockTag`

Block to start searching for messages from. If not provided, will start
from the first block (block #0).

• **opts.toBlock?**: `BlockTag`

Block to stop searching for messages at. If not provided, will stop at the
latest known block ("latest").

#### Returns

`Promise`\<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

All withdrawal token bridge messages sent by the given address.

#### Source

src/cross-chain-messenger.ts:458

***

### proveAndRelayMessage()

> **proveAndRelayMessage**(`message`, `opts`?): `Promise`\<`TransactionResponse`\>

Prove and relay a cross chain message that was sent from L2 to L1. Only applicable for L2 to L1
messages.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to finalize.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the finalization transaction.

#### Source

src/cross-chain-messenger.ts:1163

***

### sendMessage()

> **sendMessage**(`message`, `opts`?): `Promise`\<`TransactionResponse`\>

Sends a given cross chain message. Where the message is sent depends on the direction attached
to the message itself.

#### Parameters

• **message**: [`CrossChainMessageRequest`](../interfaces/CrossChainMessageRequest.md)

Cross chain message to send.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the message sending transaction.

#### Source

src/cross-chain-messenger.ts:1143

***

### toCrossChainMessage()

> **toCrossChainMessage**(`message`, `opts`?): `Promise`\<[`CrossChainMessage`](../interfaces/CrossChainMessage.md)\>

Resolves a MessageLike into a CrossChainMessage object.
Unlike other coercion functions, this function is stateful and requires making additional
requests. For now I'm going to keep this function here, but we could consider putting a
similar function inside of utils/coercion.ts if people want to use this without having to
create an entire CrossChainProvider object.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

MessageLike to resolve into a CrossChainMessage.

• **opts?**

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

#### Returns

`Promise`\<[`CrossChainMessage`](../interfaces/CrossChainMessage.md)\>

Message coerced into a CrossChainMessage.

#### Source

src/cross-chain-messenger.ts:491

***

### toLowLevelMessage()

> **toLowLevelMessage**(`message`, `opts`?): `Promise`\<[`LowLevelMessage`](../type-aliases/LowLevelMessage.md)\>

Transforms a CrossChainMessenger message into its low-level representation inside the
L2ToL1MessagePasser contract on L2.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to transform.

• **opts?**

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

#### Returns

`Promise`\<[`LowLevelMessage`](../type-aliases/LowLevelMessage.md)\>

Transformed message.

#### Source

src/cross-chain-messenger.ts:326

***

### waitBatchFinalize()

> **waitBatchFinalize**(`transactionHash`): `Promise`\<`void`\>

#### Parameters

• **transactionHash**: `string`

#### Returns

`Promise`\<`void`\>

#### Source

src/cross-chain-messenger.ts:600

***

### waitForMessageReceipt()

> **waitForMessageReceipt**(`message`, `opts`): `Promise`\<[`MessageReceipt`](../interfaces/MessageReceipt.md)\>

Waits for a message to be executed and returns the receipt of the transaction that executed
the given message.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to wait for.

• **opts**= `{}`

Options to pass to the waiting function.

• **opts.confirmations?**: `number`

Number of transaction confirmations to wait for before returning.

• **opts.pollIntervalMs?**: `number`

Number of milliseconds to wait between polling for the receipt.

• **opts.timeoutMs?**: `number`

Milliseconds to wait before timing out.

#### Returns

`Promise`\<[`MessageReceipt`](../interfaces/MessageReceipt.md)\>

CrossChainMessage receipt including receipt of the transaction that relayed the
given message.

#### Source

src/cross-chain-messenger.ts:802

***

### waitForMessageStatus()

> **waitForMessageStatus**(`message`, `status`, `opts`): `Promise`\<`void`\>

Waits until the status of a given message changes to the expected status. Note that if the
status of the given message changes to a status that implies the expected status, this will
still return. If the status of the message changes to a status that exclues the expected
status, this will throw an error.

#### Parameters

• **message**: [`MessageLike`](../type-aliases/MessageLike.md)

Message to wait for.

• **status**: [`MessageStatus`](../enumerations/MessageStatus.md)

Expected status of the message.

• **opts**= `{}`

Options to pass to the waiting function.

• **opts.direction?**: [`MessageDirection`](../enumerations/MessageDirection.md)

• **opts.pollIntervalMs?**: `number`

Number of milliseconds to wait when polling.

• **opts.timeoutMs?**: `number`

Milliseconds to wait before timing out.

#### Returns

`Promise`\<`void`\>

#### Source

src/cross-chain-messenger.ts:840

***

### waitRollupSuccess()

> **waitRollupSuccess**(`transactionHash`): `Promise`\<`void`\>

#### Parameters

• **transactionHash**: `string`

#### Returns

`Promise`\<`void`\>

#### Source

src/cross-chain-messenger.ts:552

***

### waitSyncSuccess()

> **waitSyncSuccess**(`transactionHash`): `Promise`\<`void`\>

#### Parameters

• **transactionHash**: `string`

#### Returns

`Promise`\<`void`\>

#### Source

src/cross-chain-messenger.ts:576

***

### withdrawERC20()

> **withdrawERC20**(`l1Token`, `l2Token`, `amount`, `opts`?): `Promise`\<`TransactionResponse`\>

Withdraws some ERC20 tokens back to the L1 chain.

#### Parameters

• **l1Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L1 token.

• **l2Token**: [`AddressLike`](../type-aliases/AddressLike.md)

Address of the L2 token.

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the withdraw transaction.

#### Source

src/cross-chain-messenger.ts:1282

***

### withdrawETH()

> **withdrawETH**(`amount`, `opts`?): `Promise`\<`TransactionResponse`\>

Withdraws some ETH back to the L1 chain.

#### Parameters

• **amount**: [`NumberLike`](../type-aliases/NumberLike.md)

Amount of ETH to withdraw.

• **opts?**: [`IActionOptions`](../interfaces/IActionOptions.md)

Additional options.

#### Returns

`Promise`\<`TransactionResponse`\>

Transaction response for the withdraw transaction.

#### Source

src/cross-chain-messenger.ts:1198
