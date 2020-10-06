Tuc
===

[Home](/) / Tuc

---

> **T**yped **U**se-**C**ase

## Table of contents
- [Syntax](/tuc/#syntax)
- [Structure](/tuc/#structure)
    - [Tuc Name](/tuc/#tuc-name)
    - [Participants](/tuc/#participants)
    - [Parts](/tuc/#use-case-parts)
- [Example](/tuc/example.html)

## Syntax
> We use a custom syntax to create a [PlantUML](https://plantuml.com/) diagram with ease.

Syntax is meant to be as **light-weight** as possible. It is also a **white-space significant**, so no other boilerplate symbols are needed.

### Indentation
Nested structure is indented by spaces.

**The first indented line** specifies the **indentation level** for the **entire file**.

> You determine number of spaces on your own, but you need to stick with it in the entire file.

```tuc
MainInitiator
    // here is the body (lifeline) of the initiator, currently indented by 4 spaces
```

### Comments
You can comment your tuc file with the simple syntax of `//`.
Everything behind `//` is ignored and the parser won't do anything with it (_at the moment_).

```tuc
// this is comment
```

There are no special multi-line comments.
```tuc
// this
// is
// multi-line
// comment
```

## Structure
Single tuc definition **must** consist of 3 parts:
* [Tuc Name](/tuc/#tuc-name)
* [Participants](/tuc/#participants)
* [Use-case Parts](/tuc/#use-case-parts)

Single tuc definition
```tuc
tuc Example     // tuc name

participants    // participants
    MyService MyDomain

MyService       // use-case parts
    do something
```

Tuc file can contain one or more tuc definitions.

### Tuc name
This is a start of a tuc definition. (_It will be a section in puml result._)

`tuc {NAME OF YOUR TYPED-USE-CASE}`

Example:
```tuc
tuc My use case definition
```

### Participants
All participants of the use case **must** be defined.

**NOTE**: Order in this definition determines the order of participants in puml result.

Their definition **must** start with `participants` key word.
Then there are participants defined as a name of the `Record` (or [`Initiator`](/domain/#initiator)) in the Domain Types and its Domain.

The minimal participants definition.
```tuc
participants
    MyService MyDomainName
```

**NOTE**: Participants are the first indented line(s) in the tuc file, so they determine the indentation level of the entire file.

Read more about [participants here](/tuc/participants.html).

### Use-Case Parts
There **must** be at lease one part of the use-case.

There is currently 13 available parts:
* [Lifeline](/tuc/parts.html#lifeline)
* [Section](/tuc/parts.html#section)
* [Service Method Call](/tuc/parts.html#service-method-call)
* [Post Data](/tuc/parts.html#post-data)
* [Read Data](/tuc/parts.html#read-data)
* [Post Event](/tuc/parts.html#post-event)
* [Read Event](/tuc/parts.html#read-event)
* [Handle Event In Stream](/tuc/parts.html#handle-event-in-stream)
* [Group](/tuc/parts.html#group)
* [If](/tuc/parts.html#if)
* [Loop](/tuc/parts.html#loop)
* [Do](/tuc/parts.html#do)
* [Left Note](/tuc/parts.html#left-note)
* [Note](/tuc/parts.html#note)
* [Right Note](/tuc/parts.html#right-note)

Read more about [parts here](/tuc/parts.html).
