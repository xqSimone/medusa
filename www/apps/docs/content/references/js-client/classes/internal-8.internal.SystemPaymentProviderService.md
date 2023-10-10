---
displayed_sidebar: jsClientSidebar
---

# Class: SystemPaymentProviderService

[internal](../modules/internal-8.md).[internal](../modules/internal-8.internal.md).SystemPaymentProviderService

## Hierarchy

- [`TransactionBaseService`](internal-8.internal.TransactionBaseService.md)

  ↳ **`SystemPaymentProviderService`**

## Properties

### \_\_configModule\_\_

• `Protected` `Optional` `Readonly` **\_\_configModule\_\_**: [`Record`](../modules/internal.md#record)<`string`, `unknown`\>

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[__configModule__](internal-8.internal.TransactionBaseService.md#__configmodule__)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:5

___

### \_\_container\_\_

• `Protected` `Readonly` **\_\_container\_\_**: `any`

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[__container__](internal-8.internal.TransactionBaseService.md#__container__)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:4

___

### \_\_moduleDeclaration\_\_

• `Protected` `Optional` `Readonly` **\_\_moduleDeclaration\_\_**: [`Record`](../modules/internal.md#record)<`string`, `unknown`\>

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[__moduleDeclaration__](internal-8.internal.TransactionBaseService.md#__moduledeclaration__)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:6

___

### manager\_

• `Protected` **manager\_**: `EntityManager`

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[manager_](internal-8.internal.TransactionBaseService.md#manager_)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:7

___

### transactionManager\_

• `Protected` **transactionManager\_**: `undefined` \| `EntityManager`

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[transactionManager_](internal-8.internal.TransactionBaseService.md#transactionmanager_)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:8

___

### identifier

▪ `Static` **identifier**: `string`

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:3

## Accessors

### activeManager\_

• `Protected` `get` **activeManager_**(): `EntityManager`

#### Returns

`EntityManager`

#### Inherited from

TransactionBaseService.activeManager\_

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:9

## Methods

### atomicPhase\_

▸ `Protected` **atomicPhase_**<`TResult`, `TError`\>(`work`, `isolationOrErrorHandler?`, `maybeErrorHandlerOrDontFail?`): `Promise`<`TResult`\>

Wraps some work within a transactional block. If the service already has
a transaction manager attached this will be reused, otherwise a new
transaction manager is created.

#### Type parameters

| Name |
| :------ |
| `TResult` |
| `TError` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `work` | (`transactionManager`: `EntityManager`) => `Promise`<`TResult`\> | the transactional work to be done |
| `isolationOrErrorHandler?` | `IsolationLevel` \| (`error`: `TError`) => `Promise`<`void` \| `TResult`\> | the isolation level to be used for the work. |
| `maybeErrorHandlerOrDontFail?` | (`error`: `TError`) => `Promise`<`void` \| `TResult`\> | Potential error handler |

#### Returns

`Promise`<`TResult`\>

the result of the transactional work

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[atomicPhase_](internal-8.internal.TransactionBaseService.md#atomicphase_)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:24

___

### authorizePayment

▸ **authorizePayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:8

___

### cancelPayment

▸ **cancelPayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:14

___

### capturePayment

▸ **capturePayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:12

___

### createPayment

▸ **createPayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:5

___

### deletePayment

▸ **deletePayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:11

___

### getPaymentData

▸ **getPaymentData**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:7

___

### getStatus

▸ **getStatus**(`_`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<`string`\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:6

___

### refundPayment

▸ **refundPayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:13

___

### shouldRetryTransaction\_

▸ `Protected` **shouldRetryTransaction_**(`err`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `err` | [`Record`](../modules/internal.md#record)<`string`, `unknown`\> \| { `code`: `string`  } |

#### Returns

`boolean`

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[shouldRetryTransaction_](internal-8.internal.TransactionBaseService.md#shouldretrytransaction_)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:12

___

### updatePayment

▸ **updatePayment**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:10

___

### updatePaymentData

▸ **updatePaymentData**(`_`): `Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `any` |

#### Returns

`Promise`<[`Record`](../modules/internal.md#record)<`string`, `unknown`\>\>

#### Defined in

packages/medusa/dist/services/system-payment-provider.d.ts:9

___

### withTransaction

▸ **withTransaction**(`transactionManager?`): [`SystemPaymentProviderService`](internal-8.internal.SystemPaymentProviderService.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionManager?` | `EntityManager` |

#### Returns

[`SystemPaymentProviderService`](internal-8.internal.SystemPaymentProviderService.md)

#### Inherited from

[TransactionBaseService](internal-8.internal.TransactionBaseService.md).[withTransaction](internal-8.internal.TransactionBaseService.md#withtransaction)

#### Defined in

packages/medusa/dist/interfaces/transaction-base-service.d.ts:11