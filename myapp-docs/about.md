# About

:::expandable-heading
# Expandable heading 1

bla bla bla


:::

::::expandable-heading
## Expandable heading 2

bla bla bla

:::hint{type="info"}
callout
:::




::::



:::cta-button{label="custom name button" docId docAnchorId externalHref="https://www.google.com" openInNewTab="true"}

:::

::::vertical-split{layout="middle"}
:::vertical-split-item
Left line

- [x] checked
:::

:::vertical-split-item
Right line

- [ ] unchecked
:::
::::

```tex
int_0^infty x^2 dx
```

:::api-method-v2{data="{&#x22;name&#x22;:&#x22;Get Cakes&#x22;,&#x22;method&#x22;:&#x22;GET&#x22;,&#x22;url&#x22;:&#x22;https://api.cakes.com&#x22;,&#x22;description&#x22;:&#x22;Get a cake by its ID&#x22;,&#x22;tab&#x22;:&#x22;examples&#x22;,&#x22;examples&#x22;:{&#x22;languages&#x22;:[{&#x22;id&#x22;:&#x22;AHCj1kym9VbKG75xKdS0C&#x22;,&#x22;language&#x22;:&#x22;javascript&#x22;,&#x22;code&#x22;:&#x22;var myHeaders = new Headers();\nmyHeaders.append(\&#x22;Accept\&#x22;, \&#x22;application/json\&#x22;);\nmyHeaders.append(\&#x22;Content-Type\&#x22;, \&#x22;application/json\&#x22;);\n\nvar raw = JSON.stringify({\n   \&#x22;id\&#x22;: \&#x22;String\&#x22;\n});\n\nvar requestOptions = {\n   method: 'GET',\n   headers: myHeaders,\n   body: raw,\n   redirect: 'follow'\n};\n\nfetch(\&#x22;https://api.cakes.com\&#x22;, requestOptions)\n   .then(response => response.text())\n   .then(result => console.log(result))\n   .catch(error => console.log('error', error));&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;},{&#x22;id&#x22;:&#x22;O2bD-M47IJN5NolDR5Yiv&#x22;,&#x22;language&#x22;:&#x22;curl&#x22;,&#x22;code&#x22;:&#x22;curl --location --request GET 'https://api.cakes.com' \\\n--header 'Accept: application/json' \\\n--header 'Content-Type: application/json' \\\n--data '{\&#x22;NAME1\&#x22;:\&#x22;String\&#x22;,\&#x22;NAM2\&#x22;:\&#x22;Boolean\&#x22;}'&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;},{&#x22;id&#x22;:&#x22;sb1LldrPPDKW7NHegtgOl&#x22;,&#x22;language&#x22;:&#x22;nodejs&#x22;,&#x22;code&#x22;:&#x22;var request = require('request');\nvar options = {\n   'method': 'GET',\n   'url': 'https://api.cakes.com',\n   'headers': {\n      'Accept': 'application/json',\n      'Content-Type': 'application/json'\n   },\n   body: JSON.stringify({\n      \&#x22;NAME1\&#x22;: \&#x22;String\&#x22;,\n      \&#x22;NAM2\&#x22;: \&#x22;Boolean\&#x22;\n   })\n\n};\nrequest(options, function (error, response) {\n   if (error) throw new Error(error);\n   console.log(response.body);\n});\n&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;},{&#x22;id&#x22;:&#x22;RqKlOxRqd4d5GZ4gbjkBL&#x22;,&#x22;language&#x22;:&#x22;javascript&#x22;,&#x22;code&#x22;:&#x22;var myHeaders = new Headers();\nmyHeaders.append(\&#x22;Accept\&#x22;, \&#x22;application/json\&#x22;);\nmyHeaders.append(\&#x22;Content-Type\&#x22;, \&#x22;application/json\&#x22;);\n\nvar raw = JSON.stringify({\n   \&#x22;NAME1\&#x22;: \&#x22;String\&#x22;,\n   \&#x22;NAM2\&#x22;: \&#x22;Boolean\&#x22;\n});\n\nvar requestOptions = {\n   method: 'GET',\n   headers: myHeaders,\n   body: raw,\n   redirect: 'follow'\n};\n\nfetch(\&#x22;https://api.cakes.com\&#x22;, requestOptions)\n   .then(response => response.text())\n   .then(result => console.log(result))\n   .catch(error => console.log('error', error));&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;},{&#x22;id&#x22;:&#x22;_2n50dgD7iTmDmIJNlKv2&#x22;,&#x22;language&#x22;:&#x22;python&#x22;,&#x22;code&#x22;:&#x22;import requests\nimport json\n\nurl = \&#x22;https://api.cakes.com\&#x22;\n\npayload = json.dumps({\n   \&#x22;NAME1\&#x22;: \&#x22;String\&#x22;,\n   \&#x22;NAM2\&#x22;: \&#x22;Boolean\&#x22;\n})\nheaders = {\n   'Accept': 'application/json',\n   'Content-Type': 'application/json'\n}\n\nresponse = requests.request(\&#x22;GET\&#x22;, url, headers=headers, data=payload)\n\nprint(response.text)\n&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;},{&#x22;id&#x22;:&#x22;hwnhSkxByWuWOZm3WqLLV&#x22;,&#x22;language&#x22;:&#x22;ruby&#x22;,&#x22;code&#x22;:&#x22;require \&#x22;uri\&#x22;\nrequire \&#x22;json\&#x22;\nrequire \&#x22;net/http\&#x22;\n\nurl = URI(\&#x22;https://api.cakes.com\&#x22;)\n\nhttps = Net::HTTP.new(url.host, url.port)\nhttps.use_ssl = true\n\nrequest = Net::HTTP::Get.new(url)\nrequest[\&#x22;Accept\&#x22;] = \&#x22;application/json\&#x22;\nrequest[\&#x22;Content-Type\&#x22;] = \&#x22;application/json\&#x22;\nrequest.body = JSON.dump({\n   \&#x22;NAME1\&#x22;: \&#x22;String\&#x22;,\n   \&#x22;NAM2\&#x22;: \&#x22;Boolean\&#x22;\n})\n\nresponse = https.request(request)\nputs response.read_body\n&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;}],&#x22;selectedLanguageId&#x22;:&#x22;O2bD-M47IJN5NolDR5Yiv&#x22;},&#x22;results&#x22;:{&#x22;languages&#x22;:[{&#x22;id&#x22;:&#x22;4hB2ddF-Kl47twS5Ri0R4&#x22;,&#x22;language&#x22;:&#x22;200&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;,&#x22;code&#x22;:&#x22;{\n  \&#x22;name\&#x22;: \&#x22;Cake's name\&#x22;,\n}&#x22;},{&#x22;id&#x22;:&#x22;tcD-JzCeYYamXkTJMVNZs&#x22;,&#x22;language&#x22;:&#x22;404&#x22;,&#x22;customLabel&#x22;:&#x22;&#x22;,&#x22;code&#x22;:&#x22;{\n  \&#x22;message\&#x22;: \&#x22;Ain't no cake like that.\&#x22;\n}&#x22;}],&#x22;selectedLanguageId&#x22;:&#x22;4hB2ddF-Kl47twS5Ri0R4&#x22;},&#x22;request&#x22;:{&#x22;pathParameters&#x22;:[],&#x22;queryParameters&#x22;:[],&#x22;headerParameters&#x22;:[],&#x22;bodyDataParameters&#x22;:[{&#x22;name&#x22;:&#x22;NAME1&#x22;,&#x22;kind&#x22;:&#x22;required&#x22;,&#x22;type&#x22;:&#x22;string&#x22;,&#x22;description&#x22;:&#x22;ANDREI&#x22;},{&#x22;name&#x22;:&#x22;NAM2&#x22;,&#x22;kind&#x22;:&#x22;optional&#x22;,&#x22;type&#x22;:&#x22;Boolean&#x22;,&#x22;description&#x22;:&#x22;TRUE&#x22;,&#x22;children&#x22;:[]}],&#x22;formDataParameters&#x22;:[]},&#x22;currentNewParameter&#x22;:{&#x22;label&#x22;:&#x22;Body Parameter&#x22;,&#x22;value&#x22;:&#x22;bodyDataParameters&#x22;},&#x22;response&#x22;:[{&#x22;name&#x22;:&#x22;WHAT?&#x22;,&#x22;kind&#x22;:&#x22;optional&#x22;,&#x22;type&#x22;:&#x22;string&#x22;,&#x22;description&#x22;:&#x22;YES&#x22;}]}"}

:::

:::iframe{iframeHeight="0" code="<!-- <p>TEST IFRAME</p> -->"}

:::

<a href="./syntax/an-item.md" target="_blank">custom name- dynamic link</a>&#x20;

::::workflow-block
:::workflow-block-item
line 1
:::

:::workflow-block-item
line 2


:::

:::workflow-block-item
line 3
:::
::::

