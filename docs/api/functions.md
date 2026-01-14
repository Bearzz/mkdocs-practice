# Functions Reference

Complete reference for all available functions in the API.

## Core Functions

### `get_data()`

Retrieves data from the specified resource.

**Signature:**
```python
get_data(resource_id: str, options: dict = None) -> dict
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resource_id` | string | Yes | Unique identifier for the resource |
| `options` | dict | No | Optional configuration parameters |

**Returns:**

| Type | Description |
|------|-------------|
| dict | Resource data with metadata |

**Example:**

```python
from api import get_data

# Basic usage
data = get_data("12345")

# With options
data = get_data("12345", options={
    "include_metadata": True,
    "format": "json"
})

print(data)
# Output:
# {
#     "id": "12345",
#     "name": "Example Resource",
#     "created_at": "2026-01-14T09:00:00Z"
# }
```

**Errors:**

- `ValueError`: If resource_id is empty or invalid
- `ResourceNotFoundError`: If resource doesn't exist
- `PermissionError`: If user lacks access rights

---

### `create_resource()`

Creates a new resource with the specified data.

**Signature:**
```python
create_resource(data: dict, validate: bool = True) -> dict
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `data` | dict | Yes | Resource data to create |
| `validate` | bool | No | Whether to validate input (default: True) |

**Returns:**

| Type | Description |
|------|-------------|
| dict | Created resource with generated ID |

**Example:**

```python
from api import create_resource

# Create a new resource
new_resource = create_resource({
    "name": "My Resource",
    "type": "document",
    "tags": ["important", "draft"]
})

print(new_resource)
# Output:
# {
#     "id": "new-id-67890",
#     "name": "My Resource",
#     "type": "document",
#     "tags": ["important", "draft"],
#     "created_at": "2026-01-14T09:00:00Z"
# }
```

**Errors:**

- `ValidationError`: If data doesn't meet schema requirements
- `DuplicateError`: If resource with same name exists
- `QuotaExceededError`: If account limit reached

---

### `update_resource()`

Updates an existing resource with new data.

**Signature:**
```python
update_resource(resource_id: str, data: dict, partial: bool = False) -> dict
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resource_id` | string | Yes | Resource identifier to update |
| `data` | dict | Yes | Updated field values |
| `partial` | bool | No | Allow partial updates (default: False) |

**Returns:**

| Type | Description |
|------|-------------|
| dict | Updated resource data |

**Example:**

```python
from api import update_resource

# Full update
updated = update_resource("12345", {
    "name": "Updated Name",
    "type": "document",
    "tags": ["updated"]
})

# Partial update
updated = update_resource("12345", {
    "name": "New Name"
}, partial=True)
```

---

### `delete_resource()`

Deletes a resource permanently.

**Signature:**
```python
delete_resource(resource_id: str, force: bool = False) -> bool
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resource_id` | string | Yes | Resource identifier to delete |
| `force` | bool | No | Force deletion even if in use (default: False) |

**Returns:**

| Type | Description |
|------|-------------|
| bool | True if deleted successfully |

**Example:**

```python
from api import delete_resource

# Standard deletion
success = delete_resource("12345")

# Force deletion
success = delete_resource("12345", force=True)

if success:
    print("Resource deleted successfully")
```

**Warnings:**

!!! danger "Permanent Action"
    Deletion is permanent and cannot be undone. Always backup important data.

---

## Utility Functions

### `validate_input()`

Validates input data against a schema.

**Signature:**
```python
validate_input(data: dict, schema: dict) -> tuple[bool, list]
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `data` | dict | Yes | Data to validate |
| `schema` | dict | Yes | Validation schema |

**Returns:**

| Type | Description |
|------|-------------|
| tuple | (is_valid, error_list) |

**Example:**

```python
from api import validate_input

schema = {
    "name": {"type": "string", "required": True, "min_length": 3},
    "age": {"type": "integer", "required": False, "min": 0}
}

data = {"name": "John", "age": 30}
is_valid, errors = validate_input(data, schema)

if is_valid:
    print("Data is valid")
else:
    print(f"Validation errors: {errors}")
```

---

### `format_response()`

Formats API response data according to specified format.

**Signature:**
```python
format_response(data: dict, format_type: str = "json") -> str
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `data` | dict | Yes | Data to format |
| `format_type` | string | No | Output format: "json", "xml", "yaml" |

**Returns:**

| Type | Description |
|------|-------------|
| string | Formatted data string |

**Example:**

```python
from api import format_response

data = {"name": "Example", "value": 123}

# JSON format (default)
json_output = format_response(data)

# XML format
xml_output = format_response(data, format_type="xml")

# YAML format
yaml_output = format_response(data, format_type="yaml")
```

---

## Batch Operations

### `batch_create()`

Creates multiple resources in a single operation.

**Signature:**
```python
batch_create(items: list[dict], continue_on_error: bool = False) -> list[dict]
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `items` | list[dict] | Yes | List of resources to create |
| `continue_on_error` | bool | No | Continue if one fails (default: False) |

**Returns:**

| Type | Description |
|------|-------------|
| list[dict] | List of created resources |

**Example:**

```python
from api import batch_create

items = [
    {"name": "Resource 1", "type": "document"},
    {"name": "Resource 2", "type": "image"},
    {"name": "Resource 3", "type": "video"}
]

results = batch_create(items, continue_on_error=True)
print(f"Created {len(results)} resources")
```

!!! tip "Performance"
    Batch operations are significantly faster than individual calls. Use them when creating/updating multiple resources.

---

## Next Steps

For more information:

- Review [API Overview](overview.md) for authentication and rate limiting
- Check the [User Guide](../user-guide/overview.md) for tutorials
- Explore code examples in each function's documentation
