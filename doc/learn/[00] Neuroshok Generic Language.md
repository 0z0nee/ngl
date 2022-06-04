# Neuroshok Generic Language

## [0.1] Overview

### [0.1.1] Language concepts

- **Data**
    - Concept: a concept is a ngl:data described by an entity stored in the entity storage
    - Concrete: a concrete is a materialisation of a concept
        - Entity: an entity is a data able to process logic

- **Rule**: describes an internal logic or external interactions
      
- **Storage**: stores *data* with logic (rules)
    - Environment: a storage containing all the *data* from an entity perspective
    - Element: an atomic ngl:data  from an entity perspective
    
- **Shape**: a shape describes logic between *ngl:element*
    
- **Edge**: creates interactions between *data*

- **Entity**: logical data that can create **ngl:edge** to interact

### [0.1.2] Language ecosystem

- **compiler**: *nc*
- **build system**: *nc* with ngl:ecosystem:project
- **libraries/packages**: *nc* with ngl:cluster
- **tests/benchs/docs**: *nc*
- **versionning**: *nc* with the ngl vcs configuration
- **standard library**: *ncc*, the ngl concept cluster
- **collaborative libraries/packages location**: ngl.neuroshok.com/cluster/collaborative/

## [0.2] Introduction

ngl is designed upon a **description** principle. An entity will describe a new data from a previously described data wich belong to this entity by creating an edge of a customisable type.

So the first description we will do, is the description of ngl itself and of the concepts it contains.

The internal representation of ngl code is a graph. A generic edge will be represented by `:` and a parameterized edge *contains* will be created for each data in a description bloc.

The description of ngl will look like:

```
ngl ngl
{
    concept
    entity
    storage
    data
    environment
    rule
    edge
    ...
}
```

ngl is an entity describing itself. It represents a theoretical entity used to describe every existing data of our world in the most generic and formal way through its concepts.

## [0.2.1] Starting from nothing

To understand ngl, let's start from nothing with an analogy with our world.

You are a human able to describe things, an **ngl:entity**.

You are stored in the universe, an **ngl:storage**.
The universe contains everything from your perspective so it's a specific storage, an **ngl:environment**.

But what is a *thing* ? A **ngl:data**.

In this universe, there are rules (gravity, subatomic interactions, speed limits...), those are **ngl:rule**.

Things can be different from one to another, they have a shape you can identify, a **ngl:shape**.

There are interactions between those things(a thing moving in the universe, a collision...), 
those interactions are represented by **ngl:edge**.

Now we have a *living* universe, so let's be more specific about us.

You are a **ngl:entity** (a **ngl:data** able to act). 
You create **ngl:edge** with other **ngl:data**.
Those data are, from your perspective, **ngl:concrete** (physical). 
The representation of those concrete data are **ngl:concept**. For example, when you observe
Mars (a concrete data ), you will identify a planet in your mind (a concept).

From your perspective, a planet in the universe is a concrete data, a planet in your mind is
a concept. But the concept of the planet in your mind is a concrete data from the universe
perspective, it physically exists in your brain.

## [0.2.2] Programming perspective

- You are a **ngl:entity**
- A compiler is a **ngl:entity**
- Your program idea is a **ngl:concept**
- Your OS is the **ngl:environment** of your program
- Your source code is the **ngl:concrete** of your **ngl:concept**
- The compiler will read your concrete source code, its internal representation is the concept
- The compiler will write its concept to a **ngl:storage** (filesystem)
