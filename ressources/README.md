# thingy-network-base 

# Background
As we encounter the situation to retriev some data over the network quite frequently, I had the urge to make this a litle bit more convenient. 

The added convenience is:

- No need to define the options for POST
- Throws meaningful Error unless response.ok == true

The functions provided are:

- postData(url, data)
- getData(url)
- getAsset(url)
- getText(url)

The options for POST are:
```
{
    method: "POST"
    credentials: "omit"
    headers: { "Content-Type":"application/json" }
    body: JSON.stringify(data)
}
```

# Usage
Requirements
------------
- [nodejs](https://nodejs.org/en/) >= 18
- ESM importability

Installation
------------

Current git version:
```
npm install -g git+https://github.com/JhonnyJason/thingy-network-base-output.git
```
Npm Registry
```
npm install -g thingy-network-base
```

Usage
-----
Cherry-pick named import.
```
import { postData, getData, getText, getAsset } from "thingy-network-base"

url="https://..."
data = {...}

resultObj = await postData(url, data)
resultObj = await getData(url)
resultString = await getText(url)
resultObjectURL = await getAsset(url)
```

Import all.
```
import * as network from "thingy-network-base"

url="https://..."
data = {...}


resultObj = await network.postData(url, data)
resultObj = await network.getData(url)
resultString = await network.getText(url)
resultObjectURL = await network.getAsset(url)
```

Current Functionality
---------------------

All of our functions return a promise.
They will throw exceptions on unexpected behaviour and network issues.

## postData(url, data)
- url - the URL how you would pass it to fetch()
- JSON data to be sent
When the Promise resolves we will have the response as JSON.

## getData(url)
- url - the URL how you would pass it to fetch()
- Returned Promise resolves to the result JSON.
- Expects JSON to be found

## getText(url)
- url - the URL how you would pass it to fetch()
- Returned Promise resolves to the result string.

## getAsset(url)
- url - the URL how you would pass it to fetch()
- Returned Promise resolves to the objectURL of the downloaded asset-blob.

---

# Further steps
- observe in production for further ideas


All sorts of inputs are welcome, thanks!

---

# License
[Unlicense JhonnyJason style](https://hackmd.io/nCpLO3gxRlSmKVG3Zxy2hA?view)
