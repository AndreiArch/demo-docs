# Demo directives

Sometimes this ↓ text isn't redered properly because of directives

something:something
something: something

This is a bold **text**

http://www.archbee.io

## Headings and expandable headings

## title

:::expandable-heading

## title

We would love you to contribute to `@octokit/rest`, pull requests are very welcome! Please see CONTRIBUTING.md for more information.

Second paragraph.
:::

## Tabs

:::::tabs
::::tab{title="Tab 1"}
Some content for Tab 1

:::hint{style="info"}
Pull requests are very welcome! Please see CONTRIBUTING.md for more information.
Tthis is really nice
:::

- [x] This is a checkbox list
- [x] This is a checkbox list
- [ ] This is done
- [ ] This is a checkbox list

::::
::::tab{title="Tab 2 Photos"}

![](https://placehold.co/600x400)

We would love you to contributeaaa
::::
:::::

---

## Hints

:::hint ## 2asdasdas
asdas asd We would love you to contribute to `@octokit/rest`, pull requests are very welcome! Please see CONTRIBUTING.md for more information.
:::

:::hint{style="info"}
We would love you to contribute to `@octokit/rest`, pull requests are very welcome! Please see CONTRIBUTING.md for more information.
:::

:::hint{style="warning"}
We would love you to contribute to @octokit/rest, pull requests are very welcome! Please see CONTRIBUTING.md for more information.
:::

:::hint{style="success"}
We would love you to contribute to @octokit/rest, pull requests are very welcome! Please see CONTRIBUTING.md for more information.
:::

---

## Link Array

::::link-array
:::link-array-item{headerType="IMAGE" headerImage="https://placehold.co/600x400"}

- list item 1
- list item 2
- asdasd

:::
:::link-array-item{headerType="COLOR" headerColor="#ff00FF"}

- [ ] unchecked list box
- [x] checked list box
- [ ]

:::
::::

---

## Code block

```nodejs
dadada
```

---

## Code blocks

:::codeblocktabs
title1.js

```javascript
js blaa
```

title2.txt

```none
blaa
```

:::

:::::codeblocktabs

```
// code block not specified
```

```
// code block not specified
```

```
// code block not specified
```

:::::

---

## Demo Code Blocks

:::::codeblocktabs

```php
// PHP is the best.
```

```java
// and JAVA too
```

```go
// demo go
```

```javascript
// demo js
```

:::::

---

{% hint style="info" %}
some hint
{% endhint %}

---

{% tabs %}
{% tab title="tab 2" %}some tab fasdfasdfasdfasdfads {% endtab %}
{% tab title="tab 2" %}some tab fasdfasdfasdfasdfads {% endtab %}
{% tab title="tab 2" %}some tab fasdfasdfasdfasdfads {% endtab %}
{% tab title="tab 2" %}some tab fasdfasdfasdfasdfads
{% endtab %}
{% endtabs %}

## embed url

::embed{url="https://youtu.be/G333Is7VPOg"}

::embed{url="https://miro.com/app/board/uXjVMDfwCOY=/?share_link_id=143348000351"}

::embed{url="https://www.loom.com/share/ddfb1f37982545a49a4c98225742c082"}

::embed{url="https://docs.google.com/spreadsheets/d/1hCSE4ycyC8JZ_oKqUsy-nTKo5H4314pCp97OHdXBndw/edit#gid=788504372"}

:::embed{url="https://youtu.be/G333Is7VPOg"}
:::

:::embed
https://youtu.be/G333Is7VPOg
:::

---

## Changelog import example import via directive

:::changelog{title="../header.md"}
::changelog-item{type="added" description="asfdasdfadsa aa"}
::changelog-item{type="improved" description="asfdasdfads 22"}
::changelog-item{type="fixed" description="asfdasdfads 4"}
::changelog-item{type="fixe123123123d" description="asfdasdfads 1s"}
::changelog-item{description="asfdasdfads aa"}
:::

## Code drawer example import via directive

::::codedrawer{title="Code Section Title"}
:::codeblocktabs-examples

```javascript
// this is javascript
const wow = 'none'
```

```none
    some text
```

:::
:::codeblocktabs-responses

```
403 - forbidden
```

:::
::::
