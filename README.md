## Simple LocalBitcoins API wrapper
![Code style: Black](https://img.shields.io/badge/code%20style-black-000000.svg)
![PyPI - License](https://img.shields.io/pypi/l/localbitcoins.svg)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/localbitcoins.svg)
![PyPI - Status](https://img.shields.io/pypi/status/localbitcoins.svg)
![PyPI](https://img.shields.io/pypi/v/localbitcoins.svg)


Without words, I'll get to the point.

## To install
`pip install localbitcoins`


## Usage examples
Client:
```python
from localbitcoins import Client

client = Client(hmac_key="<hmac_key>", hmac_secret="<hmac_secret>")
resp = client.request("POST", "/api/wallet-addr")
print(resp)

```
Wrapper:
```python
from localbitcoins import Client, Wrapper

client = Client(hmac_key="<hmac_key>", hmac_secret="<hmac_secret>")
wrapper = Wrapper(client)
wallet_addr_resp = wrapper.get.wallet_addr()
status_resp = wrapper.post.ad_delete(123)
```
