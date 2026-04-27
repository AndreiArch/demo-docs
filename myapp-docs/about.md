---
title: About
docTags: 
createdAt: Fri Apr 17 2026 11:29:32 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Apr 27 2026 15:11:48 GMT+0000 (Coordinated Universal Time)
---

***

:inlineImage[]{src="https://api.archbee.com/api/optimize/511c8QBH-VHiwWnyzIwUb/55Mo9m-hmz3RtLRTQEXky_image1.png" alt caption}

**Links pointint to the same doc examples:**

:::Swagger
```json
{
  "jsonFileLocation": "https://petstore.swagger.io/v2/swagger.json",
  "headers": []
}
```
:::

Simple Link in the same doc: [About]() ⛔

her
Am adaugat niste content sa vad daca merge GitHub automatic sync
\:::
\:::

App Production

:::ApiMethodV2
```json
{
  "name": "Get Cakes",
  "method": "GET",
  "url": "https://api.cakes.com",
  "description": "Get a cake by its ID",
  "tab": "examples",
  "examples": {
    "languages": [
      {
        "id": "lgEglMMU_mIkoUHlop13g",
        "language": "javascript",
        "code": "var myHeaders = new Headers();\nmyHeaders.append(\"Accept\", \"application/json\");\nmyHeaders.append(\"Content-Type\", \"application/json\");\n\nvar raw = JSON.stringify({\n   \"id\": \"string\"\n});\n\nvar requestOptions = {\n   method: 'GET',\n   headers: myHeaders,\n   body: raw,\n   redirect: 'follow'\n};\n\nfetch(\"https://api.cakes.com\", requestOptions)\n   .then(response => response.text())\n   .then(result => console.log(result))\n   .catch(error => console.log('error', error));",
        "customLabel": ""
      }
    ],
    "selectedLanguageId": "lgEglMMU_mIkoUHlop13g"
  },
  "results": {
    "languages": [
      {
        "id": "_nM-NKlw6ALXNDGzMktm3",
        "language": "200",
        "code": "{\n  \"name\": \"Cake's name\",\n}",
        "customLabel": ""
      },
      {
        "id": "0xunyymEs0ijzlOHogb7c",
        "language": "404",
        "code": "{\n  \"message\": \"Ain't no cake like that.\"\n}",
        "customLabel": ""
      }
    ],
    "selectedLanguageId": "_nM-NKlw6ALXNDGzMktm3"
  },
  "request": {
    "pathParameters": [],
    "queryParameters": [],
    "headerParameters": [],
    "formDataParameters": [],
    "bodyDataParameters": [
      {
        "name": "id",
        "kind": "required",
        "type": "string",
        "description": "ID of the cake to get"
      }
    ]
  },
  "currentNewParameter": {
    "label": "Body Parameter",
    "value": "bodyDataParameters"
  },
  "hasTryItOut": false
}
```
:::

:::ContentSnippet{docRefId="0FP_tAWKMbokF52C3ER2g"}

:::

Link in the same doc with other anchor: :Link[About]{label="About" overridedLabel="About" spaceId docId="htOwdcg6odDIVZUxE583n" version="v2" docAnchorId="#item-separator-list" loadingMethod="dynamic" newTab="false" href="about.md"} ✅

Link in the same doc with another custom name: [custom name about]() ⛔

Link in the same doc with another custom name and another anchor: :Link[custom name anchor]{label="custom name anchor" overridedLabel="custom name anchor" spaceId docId="htOwdcg6odDIVZUxE583n" version="v2" docAnchorId="#item-separator-list" loadingMethod="dynamic" newTab="false" href="about.md"} ✅

Link in the same doc with all above + opening in a new tab: :Link[custom name with anchor and opening in a new tab]{label="custom name with anchor and opening in a new tab" overridedLabel="custom name with anchor and opening in a new tab" spaceId docId="htOwdcg6odDIVZUxE583n" version="v2" docAnchorId="#item-separator-list" loadingMethod="dynamic" newTab="true" href="about.md"} ⛔

**Links pointing to another docs from same space:**

Link to another doc from the same space: [Item separator list](syntax/an-item.md)  ✅

Link to another doc from the same space with custom details: [different title, different anchor](syntax/an-item.md) ✅

Link to an API doc from the same space: [get endpoint workers]()

link to an API doc from the same space opening in a new tab        ⛔

**Links to other spaces:**

Link to another space&#x20;

<table isTableHeaderOn="true" columnWidths="221,221,221">
  <tr>
    <td>
      <p>Turbine Platform Installer Guide</p>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a>Turbine</p>
      <p><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a></p>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a>Turbine</p>
      <p><a href="https://en.wikipedia.org/wiki/API">https://en.wikipedia.org/wiki/API</a></p>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="">get endpoint workers</a></p>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
</table>

**Links in other Archbee blocks:**

# [Item separator list](syntax/an-item.md)\* \*

- [Item separator list](syntax/an-item.md)&#x20;
- [custom name + anchor](syntax/an-item.md)&#x20;

1. [Item separator list](syntax/an-item.md)&#x20;
2. [./syntax/an-item.md](syntax/an-item.md)custom name + anchor + opening in a new tab&#x20;

- [x] [Item separator list](syntax/an-item.md)&#x20;

<table isTableHeaderOn="true" columnWidths="221,221,221">
  <tr>
    <td>
      <p><a href="syntax/an-item.md">Item separator list</a></p>
    </td>
    <td>
      <p><a href="syntax/an-item.md">Item separator list</a></p>
    </td>
    <td>
      <p><a href="syntax/an-item.md">customname</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="syntax/an-item.md">opening in a new tab</a></p>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
</table>

:::hint{type="info"}
[Item separator list](syntax/an-item.md)  [custom name + anchor](syntax/an-item.md)&#x20;
:::

::::VerticalSplit{layout="middle"}
:::VerticalSplitItem
[Item separator list](syntax/an-item.md)&#x20;
:::

:::VerticalSplitItem
[anchor+different title](syntax/an-item.md)&#x20;
:::
::::

::::LinkArray{contentSource="CUSTOM"}
:::LinkArrayItem
[Item separator list](syntax/an-item.md)&#x20;
:::

:::LinkArrayItem
[./syntax/an-item.md](syntax/an-item.md)Different title + anchor +opening in a new tab&#x20;
:::
::::

:::CtaButton{label="Item separator list" openInNewTab="true" noFollow="false"}

:::

::::WorkflowBlock
:::WorkflowBlockItem
[Item separator list](syntax/an-item.md)&#x20;
:::

:::WorkflowBlockItem
[anchor +different title](syntax/an-item.md)&#x20;
:::

:::WorkflowBlockItem
[./syntax/an-item.md](syntax/an-item.md)Item separator list&#x20;
:::
::::

::::Tabs
:::Tab{title="Tab Name"}
[Item separator list](syntax/an-item.md)&#x20;

[./syntax/an-item.md](syntax/an-item.md)different title + opening in a new tab&#x20;
:::

:::Tab{title="Second Tab Name"}

:::
::::

Examples Jigx:

# Overview

:::hint{type="danger"}
🚧 **Notice: Documentation is currently unstable**
&#x20;Due to ongoing issues with Archbee, some content may be incomplete or missing. Jigx is aware of the situation and will be transitioning to a new documentation platform soon. We appreciate your patience and understanding.
:::

Welcome to the reference documentation for Jigx. This guide provides detailed information on the properties, actions, and states with practical code examples to help you effectively utilize our schema. This reference content is designed to be a comprehensive resource for all your needs, covering:

<table isTableHeaderOn="true" columnWidths="331,332">
  <tr>
    <td>
    </td>
    <td>
      <p><a href="">Jig Types</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="">Turbine Platform Installer Release Notes</a></p>
    </td>
    <td>
      <p><a href="">Actions</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="">About</a></p>
    </td>
    <td>
      <p><a href="">Custom templates</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="syntax/an-item.md">Item separator list</a></p>
    </td>
    <td>
      <p><a href="">Preview</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="">Swimlane Cloud</a></p>
    </td>
    <td>
      <p><a href="">Notifications</a></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><a href="">OpenAI integration</a></p>
    </td>
    <td>
      <p><a href="">Localization (Translation)</a></p>
    </td>
  </tr>
</table>

Our schema includes various properties that define the structure and characteristics of data entities. Each property is documented with its name, type, allowable values, and detailed description. This section ensures you have a clear understanding of how to use each property to successfully create a Jigx App.

We have included practical code examples to help you implement and integrate these properties, actions, and components. These examples demonstrate common use cases and best practices, helping you quickly get started and avoid common pitfalls.

The code examples are downloadable to guide your development process. The **jigx-samples** solution includes most examples featured in this documentation, offering a hands-on experience to understand how each feature and functionality works.

We provide three convenient options for accessing these resources, ensuring you have the flexibility to choose the method that best suits your needs. See [Setting up your solution]() for more information.

:::ApiMethodV2
```json
{
  "name": "Get Cakes",
  "method": "GET",
  "url": "https://api.cakes.com",
  "description": "Get a cake by its ID",
  "tab": "examples",
  "examples": {
    "languages": [
      {
        "id": "WITtL4JWSzMEQJNZyQtex",
        "language": "javascript",
        "code": "var myHeaders = new Headers();\nmyHeaders.append(\"Accept\", \"application/json\");\nmyHeaders.append(\"Content-Type\", \"application/json\");\n\nvar raw = JSON.stringify({\n   \"id\": \"String\"\n});\n\nvar requestOptions = {\n   method: 'GET',\n   headers: myHeaders,\n   body: raw,\n   redirect: 'follow'\n};\n\nfetch(\"https://api.cakes.com\", requestOptions)\n   .then(response => response.text())\n   .then(result => console.log(result))\n   .catch(error => console.log('error', error));",
        "customLabel": ""
      }
    ],
    "selectedLanguageId": "WITtL4JWSzMEQJNZyQtex"
  },
  "results": {
    "languages": [
      {
        "id": "pIMyUuQ51psElXIVsaLo0",
        "language": "200",
        "code": "{\n  \"name\": \"Cake's name\",\n}",
        "customLabel": ""
      },
      {
        "id": "QdAGsDxaAbxFMQcUSNF-Z",
        "language": "404",
        "code": "{\n  \"message\": \"Ain't no cake like that.\"\n}",
        "customLabel": ""
      }
    ],
    "selectedLanguageId": "pIMyUuQ51psElXIVsaLo0"
  },
  "request": {
    "pathParameters": [],
    "queryParameters": [],
    "headerParameters": [],
    "formDataParameters": [],
    "bodyDataParameters": [
      {
        "name": "id",
        "kind": "required",
        "type": "string",
        "description": "ID of the cake to get"
      }
    ]
  },
  "currentNewParameter": {
    "label": "Body Parameter",
    "value": "bodyDataParameters"
  },
  "hasTryItOut": false
}
```
:::

:::Swagger
```json
{
  "jsonFileLocation": "https://petstore.swagger.io/v2/swagger.json",
  "headers": []
}
```
:::

:::GraphiQL
```json
{
  "endpoint": "https://app.archbee.com/api/graphql",
  "query": "{\n  status,\n  people\n}"
}
```
:::

