heap-analytics-python-client
----------------------------

a Python client library for the Heap Analytics server-side API.

It supports both the **track** and **identify** APIs. See [Heap documentation](https://docs.heapanalytics.com/reference#track-1).

Installation
------------
```
pip install git+https://github.com/m-vdb/heap-analytics-python-client.git#egg=heapapi
```

Usage
-----

```python
from heapapi import HeapAPIClient

heap_client = HeapAPIClient("app_id")

heap_client.identify(
    identity="user@email.com",
    properties={"age": 30, "country": "USA"}
)

heap_client.track(
    identity="user@email.com",
    event="Purchase",
    properties={"cost": 20, "currency": "usd"}
)
```
