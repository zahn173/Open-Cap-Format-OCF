:house: [Documentation Home](/README.md)

---

### Object - Stock Class

`https://opencaptablecoalition.com/schema/objects/stock_class`

**Description:** _Object describing a class of stock issued by the issuer_

**Data Type:** `OCF Object - STOCK_CLASS`

**Composed From:**

- [https://opencaptablecoalition.com/schema/primitives/base_object](/docs/schema/primitives/schema-primitives-base_object.md)

**Properties:**

| Property                        | Type                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Required   |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| object_type                     | **Constant:** `STOCK_CLASS`</br>_Defined in [schema/enums/object_type](/docs/schema/enums/schema-enums-object_type.md)_                   | Object type field                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | `REQUIRED` |
| name                            | `STRING`                                                                                                                                  | Name for the stock type (e.g. Series A Preferred or Class A Common)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | `REQUIRED` |
| class_type                      | `ENUM - STOCK CLASS TYPE`</br>_Description:_ Enumeration of stock class types</br>**ONE OF:**</br>&bull; COMMON</br>&bull; PREFERRED</br> | The type of this stock class (e.g. Preferred or Common)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | `REQUIRED` |
| default_id_prefix               | `STRING`                                                                                                                                  | Default prefix for certificate numbers in certificated shares (e.g. CS- in CS-1). If certificate IDs have a dash, the prefix should end in the dash like CS-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | `REQUIRED` |
| current_shares_authorized       | [schema/types/numeric](/docs/schema/types/schema-types-numeric.md)                                                                        | The most current number of shares authorized for this stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | `REQUIRED` |
| board_approval_date             | [schema/types/date](/docs/schema/types/schema-types-date.md)                                                                              | Date on which the board approved the stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | `REQUIRED` |
| votes_per_share                 | [schema/types/numeric](/docs/schema/types/schema-types-numeric.md)                                                                        | The number of votes each share of this stock class gets                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | `REQUIRED` |
| par_value                       | [schema/types/monetary](/docs/schema/types/schema-types-monetary.md)                                                                      | Per-share par value of this stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | `REQUIRED` |
| price_per_share                 | [schema/types/monetary](/docs/schema/types/schema-types-monetary.md)                                                                      | Per-share price this stock class was issued for                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | `REQUIRED` |
| seniority                       | [schema/types/numeric](/docs/schema/types/schema-types-numeric.md)                                                                        | Seniority of the stock - determines repayment priority. Seniority is ordered by increasing number so that stock classes with a higher seniority have higher repayment priority. The following properties hold for all stock classes for a given company: a) transitivity: stock classes are absolutely stackable by seniority and in increasing numerical order, b) non-uniqueness: multiple stock classes can have the same Seniority number and therefore have the same liquidation/repayment order. In practice, stock classes with same seniority may be created at different points in time and (for example, an extension of an existing preferred financing round), and also a new stock class can be created with seniority between two existing stock classes, in which case it is assigned some decimal number between the numbers representing seniority of the respective classes. | `REQUIRED` |
| conversion_rights               | [schema/types/stock_class_conversion_rights](/docs/schema/types/schema-types-stock_class_conversion_rights.md)                            | List of stock class conversion rights possible for this stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | -          |
| liquidation_preference_multiple | [schema/types/numeric](/docs/schema/types/schema-types-numeric.md)                                                                        | The liquidation preference per share for this stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | -          |
| participation_cap_multiple      | [schema/types/numeric](/docs/schema/types/schema-types-numeric.md)                                                                        | The participation cap multiple per share for this stock class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | -          |
| id                              | `STRING`                                                                                                                                  | Identifier for the object                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | `REQUIRED` |
| comments                        | [`STRING`]</br>                                                                                                                           | Unstructured text comments related to and stored for the object                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | -          |

**Source Code:** [schema/objects/StockClass.schema.json](/schema/objects/StockClass.schema.json)

**Examples:**

```

[
    {
        "object_type": "STOCK_CLASS",
        "id": "8d8371e8-d41d-4a49-9f42-b91758fd155d",
        "name": "Common Stock",
        "class_type": "COMMON",
        "default_id_prefix": "CS-",
        "current_shares_authorized": "1000000000.00",
        "board_approval_date": "2001-02-28",
        "votes_per_share": "1",
        "par_value": {
            "amount": "0.0001000000",
            "currency": "USD"
        },
        "price_per_share": {
            "amount": "0.0001000000",
            "currency": "USD"
        },
        "seniority": "1",
        "conversion_rights": [],
        "liquidation_preference_multiple": "1",
        "participation_cap_multiple": "1",
        "comments": []
    },
    {
        "object_type": "STOCK_CLASS",
        "id": "cc775778-7d6e-4f8a-93cf-4df2242d7d6d",
        "name": "Series Seed Preferred",
        "class_type": "PREFERRED",
        "default_id_prefix": "PS-",
        "current_shares_authorized": "10000000.00",
        "board_approval_date": "2021-01-28",
        "votes_per_share": "1",
        "par_value": {
            "amount": "0.0001000000",
            "currency": "USD"
        },
        "price_per_share": {
            "amount": "2.4700000000",
            "currency": "USD"
        },
        "seniority": "2",
        "conversion_rights": [
            {
                "ratio": {
                    "antecedent": "1",
                    "consequent": "1"
                },
                "converts_to_stock_class_id": "8d8371e8-d41d-4a49-9f42-b91758fd155d",
                "rounding_type": "NORMAL"
            }
        ],
        "liquidation_preference_multiple": "2",
        "participation_cap_multiple": "2",
        "comments": []
    }
]

```

---