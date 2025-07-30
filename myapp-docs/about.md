# About

**Links pointint to the same doc examples:**

Simple Link in the same doc: [About]() ⛔

Link in the same doc with other anchor: [About1]() ✅

Link in the same doc with another custom name: [custom name]() ⛔

Link in the same doc with another custom name and another anchor: [Custom name]() ✅

Link in the same doc with all above + opening in a new tab: [./#link-array---exampleasdasdasdsad]()different title  ⛔



**Links pointing to another docs from same space:**

Link to another doc from the same space: [Item separator list](./syntax/an-item.md)  ✅

Link to another doc from the same space with custom details: [different title, different anchor](./syntax/an-item.md) ✅

Link to an API doc from the same space: [List all pets some pets]()  ⛔



**Links to other spaces:**

Link to another space [Swimlane Content 2024 Release 2 Drop 1]()  ⛔



**Links in other Archbee blocks:**

# [Item separator list](./syntax/an-item.md)* *

- [Item separator list](./syntax/an-item.md)&#x20;
- [custom name + anchor](./syntax/an-item.md)&#x20;

1. [Item separator list](./syntax/an-item.md)&#x20;
2. <a href="./syntax/an-item.md" target="_blank">custom name + anchor + opening in a new tab</a>&#x20;

- [x] [Item separator list](./syntax/an-item.md)&#x20;

| [Item separator list](./syntax/an-item.md)   | [Item separator list](./syntax/an-item.md)  | [customname](./syntax/an-item.md)  |
| -------------------------------------------- | ------------------------------------------- | ---------------------------------- |
| [opening in a new tab](./syntax/an-item.md)  |                                             |                                    |
|                                              |                                             |                                    |
|                                              |                                             |                                    |

:::hint{type="info"}
[Item separator list](./syntax/an-item.md)  [custom name + anchor](./syntax/an-item.md)&#x20;
:::

::::VerticalSplit{layout="middle"}
:::VerticalSplitItem
[Item separator list](./syntax/an-item.md)&#x20;
:::

:::VerticalSplitItem
[anchor+different title](./syntax/an-item.md)&#x20;
:::
::::

::::LinkArray
:::LinkArrayItem{headerImage headerColor}
[Item separator list](./syntax/an-item.md)&#x20;
:::

:::LinkArrayItem{headerImage headerColor}
<a href="./syntax/an-item.md" target="_blank">Different title + anchor +opening in a new tab</a>&#x20;
:::
::::

:::CtaButton{url="docId:3xUWa0EkNdAeJQ5ZkxkaL" label="Item separator list"}

:::

::::WorkflowBlock
:::WorkflowBlockItem
[Item separator list](./syntax/an-item.md)&#x20;
:::

:::WorkflowBlockItem
[anchor +different title](./syntax/an-item.md)&#x20;
:::

:::WorkflowBlockItem
<a href="./syntax/an-item.md" target="_blank">Item separator list</a>&#x20;
:::
::::

::::Tabs
:::Tab{title="Tab Name"}
[Item separator list](./syntax/an-item.md)&#x20;

<a href="./syntax/an-item.md" target="_blank">different title + opening in a new tab</a>&#x20;
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

|                                                               |                                                                          |
| ------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [Data Providers](Data%20Providers.md)                         | [Jig Types](Jig%20Types.md)                                              |
| [Components](Components.md)                                   | [Actions](Actions.md)                                                    |
| [Custom components (Alpha)](Custom%20components%20_Alpha_.md) | [Custom templates](Custom%20components%20_Alpha_/Templates%20_Alpha_.md) |
| [widgets](Widgets.md)                                         | [Preview](Preview.md)                                                    |
| [Expressions](Expressions.md)                                 | [Notifications](Notifications.md)                                        |
| [OpenAI integration](OpenAI%20integration.md)                 | [Localization (Translation)](Localization%20_Translation_.md)            |

Our schema includes various properties that define the structure and characteristics of data entities. Each property is documented with its name, type, allowable values, and detailed description. This section ensures you have a clear understanding of how to use each property to successfully create a Jigx App.

We have included practical code examples to help you implement and integrate these properties, actions, and components. These examples demonstrate common use cases and best practices, helping you quickly get started and avoid common pitfalls.

The code examples are downloadable to guide your development process. The **jigx-samples** solution includes most examples featured in this documentation, offering a hands-on experience to understand how each feature and functionality works.

We provide three convenient options for accessing these resources, ensuring you have the flexibility to choose the method that best suits your needs. See [Setting up your solution](Overview/Setting%20up%20your%20solution.md) for more information.

