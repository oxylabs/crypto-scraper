# Crypto Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Crypto Scraper](https://oxylabs.io/products/scraper-api/web/crypto-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any Crypto website effortlessly. This brief guide explains how an Crypto Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Crypto website results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of [crypto.com[(https://crypto.com/eaa) page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://crypto.com/eea'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/crypto-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta http-equiv=\"x-ua-compatible\" cont ... </html>",
      "created_at": "2023-12-18 11:36:15",
      "updated_at": "2023-12-18 11:36:17",
      "page": 1,
      "url": "https://crypto.com/eea",
      "job_id": "7142477660973724673",
      "status_code": 200
    }
  ]
}
```
With our Crypto Scraper, you can smoothly glean public data from any Crypto webpage. Accumulate vital cryptocurrency information, such as market prices, transaction volumes, or blockchain details, to evaluate the market trends and stay ahead of your competition. For any queries, connect with our support team via live chat or drop an email to us at hello@oxylabs.io.
