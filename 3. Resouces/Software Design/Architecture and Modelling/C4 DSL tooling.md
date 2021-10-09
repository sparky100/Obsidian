C4 models ([[C4 Modelling]]) are defined using [Structurizr - DSL](https://structurizr.com/dsl) , the web site provides a language definition and tools for rendering the models. 

A DSL model can be created in Visual Studio using the extension [C4 DSL Extension - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=systemticks.c4-dsl-extension), this provides for syntax highlighting and auto completion as well as diagram generation. The extension generates [[PlantUML Diagrams]] graphs. The model contains the architecture definition as well as the view definitions. The syntax highlighter could be better as it allows for syntax not supported by the C4 definition, and although the plantUML file generation is logged, it can be difficult to determine what is causing model diagrmas not to render, some of the diagrams whilst  previewing correctly do not generate an equivalent diagram, this was addressed by setting the scaling width.  

An alternative to creating a DSL model is to create C4 diagrams using  [plantuml-stdlib/C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML). This extension contains C4-PlantUML includes macros, stereotypes, and other goodies (like VSCode Snippets) for creating C4 diagrams with PlantUML. More information below

-   [Getting Started](https://github.com/plantuml-stdlib/C4-PlantUML#getting-started)
-   [Supported Diagram Types](https://github.com/plantuml-stdlib/C4-PlantUML#supported-diagram-types)
-   [Snippets for Visual Studio Code](https://github.com/plantuml-stdlib/C4-PlantUML#snippets-for-visual-studio-code)
-   [Layout Options](https://github.com/plantuml-stdlib/C4-PlantUML#layout-options)
-   [Samples](https://github.com/plantuml-stdlib/C4-PlantUML#advanced-samples)
