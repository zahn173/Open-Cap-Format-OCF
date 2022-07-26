:house: [Documentation Home](/README.md)

---

### Primitive - Base Conversion Trigger Type

`https://opencaptablecoalition.com/schema/primitives/types/conversion_triggers/BaseConversionTrigger.schema.json`

**Description** _Abstract type representation of required fields require for conversion rights types._

**:warning: Primitives are Abstract and Should Not be Used for Data. They are used to enforce uniformity in OCF data types - specifically "types" and "objects". :warning:**

**Properties:**

| Property            | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Description                                                                                                                            | Required   |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| type                | `Enum - Trigger Type`</br></br>_Description:_ Enumeration of types of triggers common to various legal rights - e.g. does the satisfaction of a condition trigger an automatic conversion or merely a right to convert? If `UNSPECIFIED`, the system of record cannot represent this data in a structured form.</br></br>**ONE OF:** </br>&bull; AUTOMATIC_ON_CONDITION </br>&bull; AUTOMATIC_ON_DATE </br>&bull; ELECTIVE_IN_RANGE </br>&bull; ELECTIVE_ON_CONDITION </br>&bull; ELECTIVE_AT_WILL </br>&bull; UNSPECIFIED | When the trigger condition is met, is the conversion automatic, elective or automatic with an elective right not to convert            | `REQUIRED` |
| trigger_id          | `STRING`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Id for this conversion trigger, unique within list of ConversionTriggers in parent convertible issuance's `conversion_triggers` field. | `REQUIRED` |
| nickname            | `STRING`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Human-friendly nickname to describe the conversion right                                                                               | -          |
| trigger_description | `STRING`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Long-form description of the trigger                                                                                                   | -          |
| conversion_right    | **ONE OF the Following Types/Objs:**</br>&bull; [schema/types/conversion_rights/ConvertibleConversionRight](/docs/schema/types/conversion_rights/ConvertibleConversionRight.md)</br>&bull; [schema/types/conversion_rights/WarrantConversionRight](/docs/schema/types/conversion_rights/WarrantConversionRight.md)</br>&bull; [schema/types/conversion_rights/StockClassConversionRight](/docs/schema/types/conversion_rights/StockClassConversionRight.md)                                                                | When the conditions of the trigger are met, how does the convertible convert?                                                          | `REQUIRED` |

**Source Code:** [schema/primitives/types/conversion_triggers/BaseConversionTrigger](/schema/primitives/types/conversion_triggers/BaseConversionTrigger.schema.json)

Copyright © 2022 Open Cap Table Coalition.