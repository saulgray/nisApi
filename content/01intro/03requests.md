---
title: '1.3. Requests'
weight: 12
---

## Requests

NIS uses port 7890 to communicate with its clients. It accepts both HTTP GET and POST requests.

Assuming that the NIS is running locally, HTTP GET requests can be executed from a browser and have the form:

```shell
http://127.0.0.1:7890<path to API request>?<parameters>` for example:

curl "http://127.0.0.1:7890/account/get?address=TALICELCD3XPH4FFI5STGGNSNSWPOTG5E4DS2TOS"
```

HTTP POST request usually cannot be executed from within the browser unless you use a plugin which is able to do it. HTTP POST requests use JSON structures in the request body to supply data to NIS.

Both request types return (if any data is returned) data using JSON structures. [Appendix A: Description of the JSON Structures]() explains all JSON structures used in this document.
