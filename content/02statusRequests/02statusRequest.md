---
title: '2.2. Status Request'
weight: 23
---

## Status Request

```shell
curl "http://127.0.0.1:7890/status"
```
> Example of returned JSON object:

```json
{
    "code": 6,
    "type": 4,
    "message": "status"
}
```

| API path:    | Request type:   |
|--------------|:----------------|
| `/status`    | `GET`           |

### Description:
Determines the status of NIS.

### No Parameter


#### The code can be interpreted as follows:

- 0: Unknown status.
- 1: NIS is stopped.
- 2: NIS is starting.
- 3: NIS is running.
- 4: NIS is booting the local node (implies NIS is running).
- 5: The local node is booted (implies NIS is running).
- 6: The local node is synchronized (implies NIS is running and the local node is booted).
- 7: NIS local node does not see any remote NIS node (implies running and booted).
- 8: NIS is currently loading the block chain from the database. In this state NIS cannot serve any requests.

### Possible Errors:
If there is no response to this request, NIS is either not running or is in a state where it can't serve requests.
