**Current Version:** 2.0 (updated October 2013)

**Stencils**

- [Omnigraffle](SoarML.gstencil.zip)
- [Visio](SoarML%20v2.0.vss)

## Overview

**See Also:** [October 2013 Tuesday Lunch Slides](Tank%20Soar%20Design.pdf)

SoarML is a visual design language for Soar-based systems. 

SoarML can be used for both the creative design process and for post-implementation documentation.  In either case, it provides for a consistent, expressive way to visualize Soar-based designs.  SoarML typically can represent the structure and functioning of hundreds of lines of Soar code, spread out over several files, in a single page.  Thus, SoarML is a great way to brainstorm and review Soar designs.

Soar itself provides a very terse language and its dynamic execution often makes following a Soar program difficult, even for experts.  Soar's only syntactical construct is the production.

**A Note on Design and Abstraction**

Designs are intended to show the big picture, not the details. For details look at the code. Thus a well constructed diagram hides the accidental and irrelevant details to allow the reader to focus on the essential elements - the fundamental structure of the design. SoarML does not tell you which elements to leave out when you create a design. In fact the level of abstraction used in a design is a function of how you intend to use it. Therefore, as a designer, one of the most important decisions you make when constructing a SoarML diagram is what you are trying to communication and, from this, deciding what you will leave out.

**SoarML Diagrams and Their Elements**

SoarML can be used to create three types of diagrams:
1. *Static structure diagrams*: used to represent working memory _structure_. Static structure can also be used to represent semantic and episodic memory structure.
1. *Goal hierarchy diagrams*: used to represents the goals and their relationships. Goal hierarchy diagrams are similar to the task decomposition diagrams often used to describe older Soar agents.
1. *Soar process diagrams*: used to represent the interaction between goals, working memory structure, and operators - process flow - within a Soar agent. These diagrams are the most unique and complex of the diagrams that can be produced with SoarML.

**Static Structure Diagrams**

Static structure diagrams are derived from UML's static structure (class) diagrams. Because of this, pretty much anything that you do with a UML static structure diagram can be used in a SoarML static structure diagram. However, SoarML's static structure diagrams define a couple of minor modifications to UML that make them more useful to Soar systems.

1. SoarML static structure uses the "^" symbol to denote attributes.
1. SoarML static structure defines a section for "tags." More on this further down.
1. SoarML static structure allows the definition of constant values for attributes when appropriate.

There are many things in UML static structure diagrams that are not typically useful, though if they are needed, they can be used. These include common elements such as interfaces, static attributes, method definitions. The most commonly useful elements are as follows:

1. Classes
1. Attributes/property definitions
1. Tags
1. Is-a relationships (inheritance)
1. Has-a relationships (aggregation/composition)

*Mapping Soar Working Memory to an Object Representation*

SoarML's static structure language is an object-based representation. Soar's core representation is a working memory element (WME) based representation. Though these two representations are isomorphic, many new developers have difficulty understanding how to map one representation to another. Here we describe how to do this with an example.

There are two important equivalencies to keep in mind while reading these examples:

1. Objects in object-oriented programming are equivalent to symbols in Soar
1. Attributes/properties in object-oriented programming are equivalent to WMEs in Soar
