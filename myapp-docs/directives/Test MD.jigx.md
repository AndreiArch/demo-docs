---
title: Getting started
slug: yFynhyFPo5iBOOUykBaa7
createdAt: Sat Sep 12 2020 07:08:20 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Mar 03 2023 08:05:09 GMT+0000 (Coordinated Universal Time)
---

:::hint{type="info"}
# 👋 Welcome to Archbee!

We're stoked to have you here :)
:::

# 🎸 Get rolling with the editor

*   [ ] Click anywhere and start typing
*   [ ] Highlight any text, and use the menu to **style** *your *~~writing~~ `however` *you like;* or use Markdown shortcuts to format,* like ## or \*\** &#x20;
*   [ ] Go to a new row and type **/ **to add blocks; add anything from **lists,** **tables** to **diagrams** and **API docs **(OpenAPI or GraphQL) or embed [30+ other software ](https://www.archbee.io/integrations)like Figma, Loom, Airtable;
*   [ ] Go to a new row and type @ to link documents or mention people in your workspace
*   [ ] To the left are your collections, an easy way to hierarchically organize your docs
*   [ ] Collections can be branded & shared on your own domain, and it looks like [docs.pathfix.com](https://docs.pathfix.com) or even our own docs [docs.archbee.io](https://docs.archbee.io).


'**[Usuarios](https://app-v2.fu.do/#!/admin/users)**'

>
>
> Now let's explore 
>
>

# ****💡 Diagrams

Below is a [Mermaid.js diagram, markdown based](https://mermaid-js.github.io/mermaid/#/).&#x20;

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

# 🔌  Endpoint docs

Below is a single endpoint descriptor. Great for describing webhooks or single endpoint APIs.

## Get Cakes&#x20;

This endpoint allows you to get free cakes.

### Code examples

:::codeblocktabs
```curl
curl --request GET
  --url https://api.cakes.com/v1/cakes/:id 
  --header 'Accept: application/json'
```

```javascript
fetch("https://api.cakes.com/v1/cakes/:id", {
  "method": "GET",
  "headers": {
    "Accept": "application/json"
  }
})
.then(response => {
  console.log(response);
})
.catch(err => {
  console.error(err);
});

fetch(input)  indexedDB
,EventTarget"get" 
headers move ByteLengthQueuingStrategy*
Accept*false
(
  .then .log response
)
StaticRange in Range for(AbortController)

ScreenOrientation cancelIdleCallback SpeechRecognitionAlternative
encodeURIComponent* in thrust innerWidth

StaticRange\*ReadableStreamDefaultReaderf
ReadableStreamDefaultReader
ReadableStreamDefaultReaderf\



IDBTransaction(addEventListene)
```

```nodejs
const fetch = require('node-fetch');

let url = 'https://api.cakes.com/v1/cakes/:id';
let options = {
  method: 'GET', 
headers: {
    Accept: 'application/json',
  }
};
fetch(url, options)
  .then(res => res.json())
  .then(json => console.log(json))
  .catch(err => console.error('error:' + err));
```

```python
import requests

url = "https://api.cakes.com/v1/cakes/:id"
headers = {"Accept": "application/json"}
response = requests.request("GET", url, headers=headers)
print(response.text)
```
:::

### Responses

:::codeblocktabs
```200
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```

```404
{
    "message": "Ain't no cake like that."
}
```
:::

# ⌨️  Code blocks

:::codeblocktabs
```go
package main

import "fmt"
import "time"

func worker(done chan bool) {
    fmt.Print("working...")
    time.Sleep(time.Second)
    fmt.Println("done")
    done <- true
}

```

```python
# Python3 program to demonstrate 
# the use of sample() function . 
  
# import random  
import random 
  
  
# Prints list of random items of 
# length 3 from the given list. 
list1 = [1, 2, 3, 4, 5, 6]  
print("With list:", random.sample(list1, 3)) 
  
# Prints list of random items of 
# length 4 from the given string.  
string = "GeeksforGeeks"
print("With string:", random.sample(string, 4)) 
  
# Prints list of random items of 
# length 4 from the given tuple. 
tuple1 = ("ankit", "geeks", "computer", "science", 
                   "portal", "scientist", "btech") 
print("With tuple:", random.sample(tuple1, 4)) 
  
  
# Prints list of random items of 
# length 3 from the given set. 
set1 = {"a", "b", "c", "d", "e"} 
print("With set:", random.sample(set1, 3)) 
```

```csharp
/*
 * C# Program to Check Whether the Entered Year is a Leap Year or Not
 */
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
 
namespace Program
{
    class leapyear
    {
        static void Main(string[] args)
        {
            leapyear obj = new leapyear();
            obj.readdata();
            obj.leap();
        }
        int y;
        public void readdata()
        {
            Console.WriteLine("Enter the Year in Four Digits : ");
            y = Convert.ToInt32(Console.ReadLine());
        }
        public void leap()
        {
            if ((y % 4 == 0 && y % 100 != 0) || (y % 400 == 0))
            {
                Console.WriteLine("{0} is a Leap Year", y);
            }
            else
            {
                Console.WriteLine("{0} is not a Leap Year", y);
            }
            Console.ReadLine();
        }
    }
}
```
:::

# 🌏 API Docs

You can add OpenAPI apis by typing `(swagger)`. You can also add GraphiQL allowing you to play with your GraphQL endpoints. Just type `(gql)` in the editor.&#x20;

# 💓 Changelogs

Need good looking changelogs?

:::changelog{title="Version 2.1.13"}
::changelog-item{type="added" description="Ability to foresee the future"}

::changelog-item{type="fixed" description="Bug that took you too far into the past by 2 days"}

::changelog-item{type="improved" description="Velocity of time rewind"}

::changelog-item{type="broken" description="Broken time forward"}

::changelog-item{type="knownIssue" description="You cannot stop time"}
:::

# 📣 Callouts

Need to draw attention quickly?

:::hint{type="danger"}
## 🔴 Danger

By philosophy, the library won't warn you when you modify your past, so you might delete your entire existence.
:::

:::hint{type="success"}
## 🔮 And of course, because it's the 2020s

Everything in this workspace is realtime!
:::

## 🧞‍♀️ We're great listeners, talk to us

👉 Have a question? Click the `?` at the bottom right for guides or to send us a message.

