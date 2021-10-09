 [![memo](https://github.githubassets.com/images/icons/emoji/memo.png) Edit this Page](https://github.com/mermaid-js/mermaid/blob/develop/docs/README.md)

**Mermaid lets you create diagrams using text and code.** This simplifies the maintenance of complex diagrams. It is a Javascript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.

> If you are familiar with Markdown you should have no problem learning [Mermaid's Syntax](https://mermaid-js.github.io/mermaid/#/./n00b-syntaxReference).

![banner](https://mermaid-js.github.io/mermaid/img/header.png)

**Edit this Page** [![NSolid](https://mermaid-js.github.io/mermaid/img/GitHub-Mark-32px.png)](https://github.com/mermaid-js/mermaid/blob/develop/docs/README.md)

[![Build Status](https://travis-ci.org/mermaid-js/mermaid.svg?branch=master)](https://travis-ci.org/mermaid-js/mermaid) [](https://www.npmjs.com/package/mermaid) [![Coverage Status](https://coveralls.io/repos/github/mermaid-js/mermaid/badge.svg?branch=master)](https://coveralls.io/github/mermaid-js/mermaid?branch=master) [](https://join.slack.com/t/mermaid-talk/shared_invite/enQtNzc4NDIyNzk4OTAyLWVhYjQxOTI2OTg4YmE1ZmJkY2Y4MTU3ODliYmIwOTY3NDJlYjA0YjIyZTdkMDMyZTUwOGI0NjEzYmEwODcwOTE) [![This project is using Percyio for visual regression testing](https://percy.io/static/images/percy-badge.svg)](https://percy.io/Mermaid/mermaid)

The main purpose of Mermaid is to help Documentation catch up with Development.

> Documentation-Rot is a Catch-22 that Mermaid helps to solve.

Diagramming and Documentation costs precious developer time and gets outdated quickly. But not having diagrams or docs ruins productivity and hurts organizational learning.

Mermaid addresses this Catch-22 by cutting the time, effort and tooling that is required to create modifiable diagrams and charts, for smarter and more reusable content. Mermaid, as a text-based diagramming tool allows for quick and easy updates, it can also be made part of production scripts (and other pieces of code), to make documentation much easier.

> Mermaid is a Diagramming tool for everyone.

Even non-programmers can create diagrams through the [Mermaid Live Editor](https://github.com/mermaid-js/mermaid-live-editor), Visit the [Tutorials Page](https://mermaid-js.github.io/mermaid/#/./Tutorials) for the Live Editor video tutorials.

Many editors, wikis and other tools also have mermaid integrations and plugins, making it easy to start using mermaid. A few of those are described in [Simple start to write diagrams](https://mermaid-js.github.io/mermaid/#/./n00b-gettingStarted).

Want to see what can be built with mermaid, or what applications already support it? Read the [Integrations and Usages for Mermaid](https://mermaid-js.github.io/mermaid/#/./integrations).

For a more detailed introduction to Mermaid and some of it's more basic uses, look to the [Overview for Beginners](https://mermaid-js.github.io/mermaid/#/./n00b-overview) and [Usage](https://mermaid-js.github.io/mermaid/#/./usage).

倹 [CDN](https://unpkg.com/mermaid/) | 当 [Documentation](https://mermaidjs.github.io/) | 剏 [Contribution](https://github.com/mermaid-js/mermaid/blob/develop/docs/development.md) | 糖 [Version Log](https://mermaid-js.github.io/mermaid/#/./CHANGELOG)

> 末 Keep a steady pulse: mermaid needs more Collaborators, [Read More](https://github.com/knsv/mermaid/issues/866).

![trophy](https://github.githubassets.com/images/icons/emoji/trophy.png) **Mermaid was nominated and won the [JS Open Source Awards (2019)](https://osawards.com/javascript/#nominees) in the category "The most exciting use of technology"!!!**

**Thanks to all involved, people committing pull requests, people answering questions and special thanks to Tyler Long who is helping me maintain the project 剌**

### [](https://mermaid-js.github.io/mermaid/#/README?id=flowchart)[Flowchart](https://mermaid-js.github.io/mermaid/#/flowchart?id=flowcharts-basic-syntax)

```
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

![Flowchart](https://mermaid-js.github.io/mermaid/img/flow.png)

### [](https://mermaid-js.github.io/mermaid/#/README?id=sequence-diagram)[Sequence diagram](https://mermaid-js.github.io/mermaid/#/sequenceDiagram)

```
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

![Sequence diagram](https://mermaid-js.github.io/mermaid/img/sequence.png)

### [](https://mermaid-js.github.io/mermaid/#/README?id=gantt-diagram)[Gantt diagram](https://mermaid-js.github.io/mermaid/#/gantt)

```
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```

![Gantt diagram](https://mermaid-js.github.io/mermaid/img/gantt.png)

### [](https://mermaid-js.github.io/mermaid/#/README?id=class-diagram)[Class diagram](https://mermaid-js.github.io/mermaid/#/classDiagram)

```
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

![Class diagram](https://mermaid-js.github.io/mermaid/img/class.png)

### [Git graph - experimental](https://mermaid-js.github.io/mermaid/#/README?id=git-graph-exclamation-experimental)

```
gitGraph:
options
{
    "nodeSpacing": 150,
    "nodeRadius": 10
}
end
commit
branch newbranch
checkout newbranch
commit
commit
checkout master
commit
commit
merge newbranch
```

![Git graph](https://mermaid-js.github.io/mermaid/img/git.png)

### [](https://mermaid-js.github.io/mermaid/#/README?id=entity-relationship-diagram-exclamation-experimental)[Entity Relationship Diagram - experimental](https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram)

```
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

![ER diagram](https://mermaid-js.github.io/mermaid/img/simple-er.png)

### [](https://mermaid-js.github.io/mermaid/#/README?id=user-journey-diagram)[User Journey Diagram](https://mermaid-js.github.io/mermaid/#/user-journey)

```
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```

![Journey diagram](https://mermaid-js.github.io/mermaid/img/user-journey.png)

**In depth guides and examples can be found in [Getting Started](https://mermaid-js.github.io/mermaid/#/n00b-gettingStarted) and [Usage](https://mermaid-js.github.io/mermaid/#/usage).**

**It would also be helpful to learn more about mermaid's [Syntax](https://mermaid-js.github.io/mermaid/#/n00b-syntaxReference).**

### [CDN](https://mermaid-js.github.io/mermaid/#/README?id=cdn)

```
https://unpkg.com/mermaid@<version>/dist/
```

To select a version:

Replace `<version>` with the desired version number.

Latest Version: [https://unpkg.com/browse/mermaid@8.8.0/](https://unpkg.com/browse/mermaid@8.8.0/)

## [Deploying Mermaid](https://mermaid-js.github.io/mermaid/#/README?id=deploying-mermaid)

To Deploy Mermaid:

```
1.You will need to install node v10 or 12, which would have npm

2. download yarn using npm.

3. enter the following command:
    yarn add mermaid

4. You can then add mermaid as a dev dependency using this command:
    yarn add --dev mermaid
```

## [](https://mermaid-js.github.io/mermaid/#/README?id=mermaid-api)[Mermaid API](https://mermaid-js.github.io/mermaid/#/./Setup):

**To deploy mermaid without a bundler, one can insert a `script` tag with an absolute address and a `mermaidAPI` call into the HTML like so:**

```
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
```

**Doing so will command the mermaid parser to look for the `<div>` tags with `class="mermaid"`. From these tags mermaid will try to read the diagram/chart definitons and render them into svg charts.**

**Examples can be found in** [Other examples](https://mermaid-js.github.io/mermaid/#/examples)

-   [Mermaid Live Editor](https://github.com/mermaid-js/mermaid-live-editor)
-   [Mermaid CLI](https://github.com/mermaid-js/mermaid-cli)
-   [Mermaid Webpack Demo](https://github.com/mermaidjs/mermaid-webpack-demo)
-   [Mermaid Parcel Demo](https://github.com/mermaidjs/mermaid-parcel-demo)

## [Request for Assistance](https://mermaid-js.github.io/mermaid/#/README?id=request-for-assistance)

Things are piling up and I have a hard time keeping up. To remedy this it would be great if we could form a core team of developers to cooperate with the future development of mermaid.

As part of this team you would get write access to the repository and would represent the project when answering questions and issues.

Together we could continue the work with things like:

-   Adding more types of diagrams like mindmaps, ert diagrams, etc.
-   Improving existing diagrams

Don't hesitate to contact me if you want to get involved!

## [For contributors](https://mermaid-js.github.io/mermaid/#/README?id=for-contributors)

### [Setup](https://mermaid-js.github.io/mermaid/#/README?id=setup)

```
yarn install
```

### [Build](https://mermaid-js.github.io/mermaid/#/README?id=build)

```
yarn build:watch
```

### [Lint](https://mermaid-js.github.io/mermaid/#/README?id=lint)

```
yarn lint
```

We use [eslint](https://eslint.org/). We recommend you installing [editor plugins](https://eslint.org/docs/user-guide/integrations) so you can get real time lint result.

### [Test](https://mermaid-js.github.io/mermaid/#/README?id=test)

```
yarn test
```

Manual test in browser: open `dist/index.html`

### [Release](https://mermaid-js.github.io/mermaid/#/README?id=release)

For those who have the permission to do so:

Update version number in `package.json`.

```
npm publish
```

Command above generates files into the `dist` folder and publishes them to npmjs.org.

## [Credits](https://mermaid-js.github.io/mermaid/#/README?id=credits)

Many thanks to the [d3](http://d3js.org/) and [dagre-d3](https://github.com/cpettitt/dagre-d3) projects for providing the graphical layout and drawing libraries!

Thanks also to the [js-sequence-diagram](http://bramp.github.io/js-sequence-diagrams) project for usage of the grammar for the sequence diagrams. Thanks to Jessica Peter for inspiration and starting point for gantt rendering.

_Mermaid was created by Knut Sveidqvist for easier documentation._

Here is the full list of the projects [contributors](https://github.com/knsv/mermaid/graphs/contributors).

