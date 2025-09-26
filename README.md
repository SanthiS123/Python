Day2- script expalnation:
### 1️⃣ Variables

```python
name = "Shanti"
total_servers = 5
cpu_usage = 75.5
is_running = True
```

* `name` → a **string**
* `total_servers` → an **integer**
* `cpu_usage` → a **float** (decimal number)
* `is_running` → a **boolean** (`True` or `False`)

```python
print("Hello", name)
print("Total servers:", total_servers)
print("CPU Usage:", cpu_usage, "%")
print("Server running?", is_running)
```

* `print()` displays values in the terminal.
* You can separate items with commas `,` → Python adds a space automatically.

---

### 2️⃣ Lists

```python
aws_services = ["EC2", "S3", "RDS", "Lambda", "CloudWatch"]
```

* `aws_services` is a **list**, which is an ordered collection.
* Indexing starts from 0 (`aws_services[0]` → `"EC2"`).

```python
for service in aws_services:
    print("-", service)
```

* **Loop**: goes through each element in the list.
* Prints each AWS service with a `-` in front.

---

### 3️⃣ Dictionary for a single instance

```python
instance = {
    "id": "i-12345",
    "type": "t2.micro",
    "status": "running"
}
```

* `instance` is a **dictionary** → key-value pairs.
* Keys: `"id"`, `"type"`, `"status"`
* Values: `"i-12345"`, `"t2.micro"`, `"running"`

```python
instance["region"] = "us-east-1"
```

* Adds a new key-value pair to the dictionary.

```python
for key, value in instance.items():
    print(f"{key}: {value}")
```

* `.items()` returns **all key-value pairs**
* `f"{key}: {value}"` → **f-string formatting**, prints nicely like `id: i-12345`.

---

### 4️⃣ List of multiple instances

```python
instances = [
    {"id": "i-101", "type": "t2.micro", "status": "running"},
    {"id": "i-102", "type": "t2.small", "status": "stopped"},
    {"id": "i-103", "type": "t2.medium", "status": "running"}
]
```

* `instances` is a **list of dictionaries**.
* Each dictionary represents **one server/instance**.

```python
for inst in instances:
    print(f"ID: {inst['id']}, Type: {inst['type']}, Status: {inst['status']}")
```

* Loops through each dictionary in the list.
* Accesses values with `inst['key']`.

---

### 5️⃣ Filter running instances

```python
for inst in instances:
    if inst["status"] == "running":
        print(f"ID: {inst['id']}, Type: {inst['type']}")
```

* Checks **condition** using `if`.
* Only prints instances where `"status"` is `"running"`.

---

### 6️⃣ F-string formatting

```python
print(f"Hello {name}, you have {total_servers} servers, CPU usage is {cpu_usage}%, and server running status is {is_running}.")
```

* `f"..."` allows **embedding variables directly** in a string.
* `{name}`, `{total_servers}`, `{cpu_usage}`, `{is_running}` are replaced by their values.
* Output is **clean and readable** — perfect for scripts/logs in DevOps.

---

### ✅ Summary of concepts in this code

1. Variables (`str`, `int`, `float`, `bool`)
2. Lists + looping
3. Dictionaries + looping + adding keys
4. List of dictionaries (complex data structure)
5. Conditional statements (`if`)
6. Printing & string formatting (`f-strings`)

---

