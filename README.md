#### Simple LocalBitcoins API wrapper

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
