# AI Fundamentals

- **Definition;** “the science of making machines do things that would require intelligence if done by men.” Marvin Minsky

- **Operational Definition;** “AI is the field of computer science that studies how to make computers do tasks for which humans are still the best today.” E.Rich

## Logial Representation
It is a language with some concrete rules that deals with propositions and havs no ambiguity in representation.

Consist of: 
- **Semantic:** well formed sentence
- **Syntaxe:** truth of the meaning to a sentence



# Logical Representation is

## 1- Proposional Logic
- PL is the simplest logic
- a proposition is a declarative statment that's either true or false. 

Propositinal logic cannot predicate or assmue, it can say either true or false.

### Connectivity
<img src="PLsymbols.png">

<br>

### Truth Table
<img src="PLtruth.png">

<br>

## Examples

A- It is HOT<br>
B- It is humid<br>
C- It is rainning

**Conditions:** <br>
1- If it is humid, then it is hot <br>
2- if it is hot and humid then it is not raining

|   Conditions |  Proposition Logic |
|---|---|
| Condition 1  |  B=>A | 
| Condition 2  |  A+B => C | 


### Limitation Of PL
- We cannot represent relations like **All**, **some**, or **none**.
  - **All** the girls are intelligent
  - **Some** apples are sweet.
- PL has limited expressive power.
- In PL, we cannot describe the statements in terms of their properties or logical relationships

## 2- First Order predicat logic
First order logic is another way of knowlege representation in A.I.
 It is an extension to PL (propostional Logic)
 
 - FOL is also known as predicate logic. It is a powerful language that develops information about the objects in a more easy way and can also express the relationship between those objects. not just (True/False).
 
 - FOL does not only assume that the world contains facts like "PL" but also assumes.<br>
 1- Objects, A, B, people, colors, pits,ettc<br>
 2- Relationships: It can be any relation such, sisters, brothers, has color<br>
 3- Functions: Father of, best friend, end of...<br>
 
 As a natural language, First order logic has two main parts<br>
 a- syntax <br><br>
 b- semantics<br>
 
 
 ### Semantic of FOL: Basic Elements

|   Elements |  Syntax|
|---|---|
|      Constant      |  1,2 A, Hiehaaa | 
|   Variables         |  x,y,z,a,b,c,d | 
|            Predicats| Brother, Father, >, <  | 
|          Functions  |  Sqrt, etc | 
|          Connectives  |  No, apply, and, or, <=> (AI syntax pls) | 
|          Equality  |  = | 
|         Quantifiers   |  Qlqsoit, il existe | 


