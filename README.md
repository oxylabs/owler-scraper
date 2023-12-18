# Owler Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Owler Scraper](https://oxylabs.io/products/scraper-api/web/owler?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Owler website effortlessly. This brief guide explains how an Owler Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Owler results by providing your own URLs to our service. We can return the HTML for any Owler page you like.

#### Python code example

The example below illustrates how you can get HTML of Owler page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.owler.com/owlermax'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/owler-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html xmlns:og=\"http://opengraphprotocol.org/schema/\" xmlns:fb=\"http://www.facebook. ... </html>",
      "created_at": "2023-12-18 11:15:23",
      "updated_at": "2023-12-18 11:15:24",
      "page": 1,
      "url": "https://www.owler.com/owlermax",
      "job_id": "7142472409721873409",
      "status_code": 200
    }
  ]
}
```
With our Owler Scraper, you can seamlessly extract public data from any Owler web page. Gather the necessary company intelligence like revenue size, employee count, or competitors to scrutinize the business landscape and keep a step ahead of your rivals. If you have any questions, reach out to our support team via live chat or drop us an email at hello@oxylabs.io.