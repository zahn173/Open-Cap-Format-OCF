:house: [Documentation Home](/README.md)

---

### Object - Warrant Transfer Transaction

`https://opencaptablecoalition.com/schema/objects/transactions/transfer/WarrantTransfer.schema.json`

**Description:** _Object describing a transfer or secondary sale of a warrant security_

**Data Type:** `OCF Object - TX_WARRANT_TRANSFER`

**Composed From:**

- [schema/primitives/BaseObject](/docs/schema/primitives/BaseObject.md)
- [schema/primitives/transactions/BaseTransaction](/docs/schema/primitives/transactions/BaseTransaction.md)
- [schema/primitives/transactions/transfer/BaseTransfer](/docs/schema/primitives/transactions/transfer/BaseTransfer.md)

**Properties:**

| Property               | Type                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Required   |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| id                     | `STRING`                                                                                                         | Identifier for the object                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | `REQUIRED` |
| comments               | [`STRING`]                                                                                                       | Unstructured text comments related to and stored for the object                                                                                                                                                                                                                                                                                                                                                                                                                                             | -          |
| object_type            | **Constant:** `TX_WARRANT_TRANSFER`</br>_Defined in [schema/enums/ObjectType](/docs/schema/enums/ObjectType.md)_ | Object type field                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | `REQUIRED` |
| security_id            | `STRING`                                                                                                         | Identifier for the security (stock, plan security, warrant, or convertible) by which it can be referenced by other transaction objects. Note that while this identifier is created with an issuance object, it should be different than the issuance object's `id` field which identifies the issuance transaction object itself. All future transactions on the security (e.g. acceptance, transfer, cancel, etc.) must reference this `security_id` to qualify which security the transaction applies to. | `REQUIRED` |
| date                   | [schema/types/Date](/docs/schema/types/Date.md)                                                                  | Date on which the transaction occurred                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | `REQUIRED` |
| consideration          | [schema/types/Monetary](/docs/schema/types/Monetary.md)                                                          | Consideration for the security                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | -          |
| balance_security_id    | `STRING`                                                                                                         | Identifier for the security that holds the remainder balance (for partial transfers)                                                                                                                                                                                                                                                                                                                                                                                                                        | -          |
| resulting_security_ids | [`STRING`]                                                                                                       | Array of identifiers for new security (or securities) created as a result of the transaction                                                                                                                                                                                                                                                                                                                                                                                                                | `REQUIRED` |
| quantity               | [schema/types/Numeric](/docs/schema/types/Numeric.md)                                                            | Quantity of non-monetary security units cancelled                                                                                                                                                                                                                                                                                                                                                                                                                                                           | `REQUIRED` |

**Source Code:** [schema/objects/transactions/transfer/WarrantTransfer](/schema/objects/transactions/transfer/WarrantTransfer.schema.json)

**Examples:**

```json
[
  {
    "object_type": "TX_WARRANT_TRANSFER",
    "id": "test-warrant-transfer-minimal",
    "security_id": "test-security-id",
    "date": "2022-02-01",
    "resulting_security_ids": [
      "resultant-security-id-1"
    ],
    "quantity": "10000"
  },
  {
    "object_type": "TX_WARRANT_TRANSFER",
    "id": "test-warrant-transfer-full-fields",
    "security_id": "test-security-id",
    "date": "2022-02-01",
    "resulting_security_ids": [
      "resultant-security-id-1",
      "resultant-security-id-2"
    ],
    "quantity": "10000",
    "comments": [
      "Here is a comment",
      "Here is another comment"
    ],
    "consideration": {
      "amount": "0.50",
      "currency": "USD"
    },
    "balance_security_id": "balance-security-id"
  }
]
```