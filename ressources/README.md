# thingy-network-base 

# Background
For every thingy we need network connection. Here we want to have a unified base to build our network interfaces on top.

So this is a small convenience abstraction to expose the functions we need from the network:

- postData(url, data)
- getData(url)
- getAsset(url)
- getText(url)

# How?
Requirements
------------
- [nodejs](https://nodejs.org/en/) >= 14

We look forward for the native integration of the fetch API then we will require nodejs >18.

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

response = await postData(url, data)
result = await getData(url)
result = await getText(url)
result = await getAsset(url)
```

Import all.
```
import * as network from "thingy-network-base"

url="https://..."
data = {...}


response = await network.postData(url, data)
result = await network.getData(url)
result = await network.getText(url)
result = await network.getAsset(url)
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
- Returned Promise resolvesto the result JSON.
- Expects JSON to be found

## getText(url)
- url - the URL how you would pass it to fetch()
- Returned Promise resolves to the result string.

## getAsset(url)
- url - the URL how you would pass it to fetch()
- Returned Promise resolves to the objectURL of the downloaded asset-blob.

---

# Further steps

- fix bugs
- replace node-fetch with native fetch implementation


All sorts of inputs are welcome, thanks!

---

# License

## The Unlicense JhonnyJason style

- Information has no ownership.
- Information only has memory to reside in and relations to be meaningful.
- Information cannot be stolen. Only shared or destroyed.

And you wish it has been shared before it is destroyed.

The one claiming copyright or intellectual property either is really evil or probably has some insecurity issues which makes him blind to the fact that he also just connected information which was freely available to him.

The value is not in him who "created" the information the value is what is being done with the information.
So the restriction and friction of the informations' usage is exclusively reducing value overall.

The only preceived "value" gained due to restriction is actually very similar to the concept of blackmail (power gradient, control and dependency).

The real problems to solve are all in the "reward/credit" system and not the information distribution. Too much value is wasted because of not solving the right problem.

I can only contribute in that way - none of the information is "mine" everything I "learned" I actually also copied.
I only connect things to have something I feel is missing and share what I consider useful. So please use it without any second thought and please also share whatever could be useful for others. 

I also could give credits to all my sources - instead I use the freedom and moment of creativity which lives therein to declare my opinion on the situation. 

*Unity through Intelligence.*

We cannot subordinate us to the suboptimal dynamic we are spawned in, just because power is actually driving all things around us.
In the end a distributed network of intelligence where all information is transparently shared in the way that everyone has direct access to what he needs right now is more powerful than any brute power lever.

The same for our programs as for us.

It also is peaceful, helpful, friendly - decent. How it should be, because it's the most optimal solution for us human beings to learn, to connect to develop and evolve - not being excluded, let hanging and destroy oneself or others.

If we really manage to build an real AI which is far superior to us it will unify with this network of intelligence.
We never have to fear superior intelligence, because it's just the better engine connecting information to be most understandable/usable for the other part of the intelligence network.

The only thing to fear is a disconnected unit without a sufficient network of intelligence on its own, filled with fear, hate or hunger while being very powerful. That unit needs to learn and connect to develop and evolve then.

We can always just give information and hints :-) The unit needs to learn by and connect itself.

Have a nice day! :D