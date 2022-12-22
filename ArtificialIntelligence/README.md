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

 ### Atomic Sentences
 - Atomic sentences are the most basic sentences of FOL. These sentences are formed ffrom a predicate symbol followed by praenthesis with a sequence of terms.
 
 - we can represent atomic sentences as predicate ( term1, term2,.... termn) <br>
 
 **Example1:** Yaya and Soso are brothers. <br>
 Terms: Yahya, Soso <br>Predicate: Brothers <br>Result: Brothers( Yaya, Soso)
 
 
  **Example2:** Tommy is a dog <br>
 Terms: Tommy <br>Predicate: Dog <br>Result: Dog(Tommy)
 
  ### Complex Sentences
- Complex sentences are made by comibining atomic sentences using **connectives**(or, and, implies etc..).

Real meaning: Predicate1(Term1, Term2, TermN..) "Connectivity"  Predicate2(Term1, Term2, TermN..)
 
 #### First Order Logic Statements divided into 2 parts.
 - Subject: it is the main part of the statement
 - Predicate: can be defined a relation which binds two atmos together in a statement
 
 
 **Example:** <br>
  State: "X is an integer"
  
 First part; X is a subject of the statement <br>
 Second part, is an integer is known as predicate
 
 ---
 
  ### Quantifiers
  - a quantifier is a language element which generates quantificator
  - these are the symboles that permit to determine or identitfy the range and the score of the variable in the logic expression.
  
  There are two type of quantifier:<br>
  #### a- Universal Quantifier ( for all, everyone, everything)  -- range in math "∀" 
  It is a symbol of logical representation which specifies that the statement within its range is true for everything or every instance of particular thing
  
  if x is a varibale, the qlqsoit X is read as: <br>
 for all x
<br> for each x<br>
for every x
  
  
**Example:** All men drink coffee <br>
  let x is variable <br>
  x1 drink coffee, Vma9louba(and) x2 drink coffee and xn drinkcoffee.
  
  So we can write it as 
 	∀x man(x) --> drink (x, cofee) 
  > if i'm not using the conectivity "->" than u could call it an atomic sentence ;)
  
  There are all x where x is a man who drink coffe <br> You say also, there is x where is is men who drink coffe!! smart me!!
  
  
<br>All birds fly, predicate is fly(bird)<br> ∀x bird(x) -> fly(x)
<br>
Every man respects his parent, predicate is respect (x,y) where x=man, y=parent <br>
∀x man(x) -> respects (x, parent)
  
  ##### b- Existential quantifier ( for some, atleast one)   --scope in math "∃"
  It is the type of quantifier which express that the start within its score is true for atleast one instance of something
  <br>here we always use, and or conjuction symbol Vma9louba<br>
  
  
  if x is a variable then existential quantifier will be 
  <br> ∃ (X) is read as:
  <br> there exists a x<br> for some "x"<br> for atleast an "x"
  
  
<br> Some more examples<br>
Some boys are intelligent.<br>
x1 is intelli or x2 is intelligent or xn is intelligent <br>
∃x:boy(x) and intelligent (x)


> note: IMPORTANTTTTTT

- the main connective for ∀ is "->'
- the main connective for ∃ is 'and'

##  Inference
Inference in FOL is used to dedce new facts sentences from, existing sentences. Before understanding First Logic Inference suite, let's understand some basic teminologies used in FOL.

1- Substitution <br>
It is a fundamentals operation performed on termas and forumas It occurs in all inference sys in FOL: F[a/x] F[b/x]
<br>substitute a constant "a" in the place of variable.

2- Equality <br>
FOL logic does not only use predicate and terms for making atomic sentence but also uses another way, whch is equality in FOL. <br> eq, brother (John)= smoth <br> here the obj reffered by brother (john) is smiliar to obj refered by smoth. The equality symbol can also be used with negation to represent that two terms are notn the same objects.
<br> eq, no(x=y) equivalent to x<>y



## Unification
  
## Resolution
  
## Forward chaining and backward chaining
  
  
## AI Techniques; Search, Knowledge &  Abstraction
  
## Score Playing - Scope of AI
  
## NLP - Scope of AI
  
## Expert Systems - Scope of AI
  
## Robotics - Scope of AI
  
  
## Learning from Observation
  
## Inductive Learning
  
## Decision Tree Learning Algo
  
## AI - Application
