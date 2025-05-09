# Requests - HTTP for Humans

> Effortlessly send HTTP requests in Python.

---

## What is Requests?

**requests** is a simple and elegant HTTP library for Python. It allows you to send HTTP/1.1 requests with methods like **GET**, **POST**, **PUT**, and more - all with minmal code.

---

## Installation

```bash
pip install requests
```

```python
import requests

response = requests.get("https://api.example.com/data")
print(response.status_code)
print(response.json())
```
---

## Common Methods

- **GET**: Fetch data
- **POST**: Submit data
- **PUT**: Update data
- **DELETE**: Remove data

```python
# POST examples
payload = {'name': 'john', 'age': 30}
res = requests.post("https://api.example.com/create", json=payload)
```

---

## Headers and Params

```python
headers = {'Authorization': 'Bearer TOKEN'}
params = {'q': 'python'}

res = requests.get("https://api.example.com/search", headers=headers, params=params)
```

---

## Handling Responses

```python
if reponse.statues_code == 200:
    data = response.json()
else:
    print("Request failed:", response.status_code)

```

---

## Summary
- Human-friendly API for making wen requests
- Works great with APIs and web scraping
- Easy to handle headers, cookies, sesions

---