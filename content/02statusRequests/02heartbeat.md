---
title: '2.1 Heart beat request'
taxonomy:
weight: 22
---
## Heart Beat Request

```shell
curl "http://127.0.0.1:7890/heartbeat"
```
> Example of returned JSON object:

```json
{
    "code": 1,
    "type": 2,
    "message": "ok"
}
```

| API path:    | Request type:   |
|--------------|:----------------|
| `/heartbeat` | `GET`           |

### Description:
Determines if NIS is up and responsive.

### No Parameter.



### Possible Errors:
If there is no response to this request, NIS is either not running or is in a state where it can't serve requests.
