# Simple Calculator

```python
simple_calculator_api = client.simple_calculator
```

## Class Name

`SimpleCalculatorApi`


# Calculate

Calculates the expression using the specified operation.

```python
def calculate(self,
             operation,
             x,
             y)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`OperationType`](../../doc/models/operation-type.md) | Template, Required | The operator to apply on the variables |
| `x` | `float` | Query, Required | The LHS value |
| `y` | `float` | Query, Required | The RHS value |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `float`.

## Example Usage

```python
operation = OperationType.SUM

x = 222.14

y = 165.14

result = simple_calculator_api.calculate(
    operation,
    x,
    y
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

