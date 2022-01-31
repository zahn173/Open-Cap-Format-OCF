# Object - Plan Security Exercise Transaction Schema

```txt
https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise
```

Object describing a plan security exercise transaction

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                             |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [PlanSecurityExercise.schema.json](../../schema/objects/transactions/exercise/PlanSecurityExercise.schema.json "open original schema") |

## Object - Plan Security Exercise Transaction Type

`object` ([Object - Plan Security Exercise Transaction](plansecurityexercise.md))

all of

*   [Object - BaseObject](issuer-allof-object---baseobject.md "check type definition")

*   [Primitive - Security Transaction](convertibletransfer-allof-primitive---security-transaction.md "check type definition")

*   [Primitive - Security Exercise Transaction](plansecurityexercise-allof-primitive---security-exercise-transaction.md "check type definition")

# Object - Plan Security Exercise Transaction Properties

| Property                                          | Type          | Required | Nullable       | Defined by                                                                                                                                                                                                                                  |
| :------------------------------------------------ | :------------ | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [object_type](#object_type)                       | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-object_type.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/object_type")                       |
| [quantity](#quantity)                             | `string`      | Required | cannot be null | [Object - Plan Security Exercise Transaction](ratio-properties-type---numeric-1.md "https://opencaptablecoalition.com/schema/types/numeric#/properties/quantity")                                                                           |
| [id](#id)                                         | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-id.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/id")                                         |
| [comments](#comments)                             | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-comments.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/comments")                             |
| [security_id](#security_id)                       | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-security_id.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/security_id")                       |
| [date](#date)                                     | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-date.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/date")                                     |
| [consideration](#consideration)                   | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-consideration.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/consideration")                   |
| [resulting_security_ids](#resulting_security_ids) | Not specified | Optional | cannot be null | [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-resulting_security_ids.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/resulting_security_ids") |

## object_type



`object_type`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-object_type.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/object_type")

### object_type Type

unknown

### object_type Constraints

**constant**: the value of this property must be equal to:

```json
"TX_PLAN_SECURITY_EXERCISE"
```

## quantity

Fixed-point string representation of a number (up to 10 decimal places supported)

`quantity`

*   is required

*   Type: `string` ([Type - Numeric](ratio-properties-type---numeric-1.md))

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](ratio-properties-type---numeric-1.md "https://opencaptablecoalition.com/schema/types/numeric#/properties/quantity")

### quantity Type

`string` ([Type - Numeric](ratio-properties-type---numeric-1.md))

### quantity Constraints

**pattern**: the string must match the following regular expression: 

```regexp
^[+-]?[0-9]+(\.[0-9]{1,10})?$
```

[try pattern](https://regexr.com/?expression=%5E%5B%2B-%5D%3F%5B0-9%5D%2B\(%5C.%5B0-9%5D%7B1%2C10%7D\)%3F%24 "try regular expression with regexr.com")

## id



`id`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-id.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/id")

### id Type

unknown

## comments



`comments`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-comments.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/comments")

### comments Type

unknown

## security_id



`security_id`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-security_id.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/security_id")

### security_id Type

unknown

## date



`date`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-date.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/date")

### date Type

unknown

## consideration



`consideration`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-consideration.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/consideration")

### consideration Type

unknown

## resulting_security_ids



`resulting_security_ids`

*   is optional

*   Type: unknown

*   cannot be null

*   defined in: [Object - Plan Security Exercise Transaction](plansecurityexercise-properties-resulting_security_ids.md "https://opencaptablecoalition.com/schema/objects/transactions/exercise/plan_security_exercise#/properties/resulting_security_ids")

### resulting_security_ids Type

unknown