# AI Fundamentals - My Notes

> [Machine Learning](soon) is a small scope of the HUGE Artificial Intelligence.

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
|         Quantifiers   |  ∀, ∃ | 

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
  
  if x is a varibale, the ∀soit X is read as: <br>
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


## FOL Inference rules for quantifiers
=> Pl, we also have inference rules for FOL.

### Universal generalization: ∀
It is a valid inference rule which states that if premise p(c) is true for any arbitrary element c in the universe of discourse, then we can have a concusions ∀x p(x)
<b>r It can be respresented as, P(c)/∀x P(x) <br> Example: Let's present , P(C): " a byte contains 8 bits" <br> so for ∀xp(x), " all bytes contain 8 bits" it will also be true

### Universal instantiation (eliminiation): ∀
  It can be appiled multipl times to add new sentences. The rule says that we can infer any sentence that is premisses of p(c) by substituting a ground term c  ( constant within domain x) for ∀x p(x) for any object in the universe of course we have <br> **∀x p(x)/p(c)** <br>Example: Every person like ice-cream => ∀xp(x) we can infer that " John like ice cream" => P(c).
  
  
### existential instantiation:(eliminiation) ∃
  which is a valid reference rule in FOL. It can only applied only once to replace the existential sentence. <br>this rule states that one can infer p(c) per the foruma given in the form il existe x p(x) for a new constant syn'c'a <br>  **∃xP(x)/P(c)**
  
### existential Introductions: ∃
  It is also called as existential generalization, this rule states that if there is some element c in the unverise of discourse which has a proerty P, then we can infer that there exists something in the unversie which has property P.
<br>  **P(c)/il ∃xP(x)** <br> Pinky(c) got good markes in math, therefore someone, got good marks in math, ∃ means(someone)



# Unification
It is all about making the expression look identical. So, far the given expressions to make them look idenntical we need to do substitution. <br> 
Eg: P(x, F(y)), p(a, F(g(z)), i can say these are identical why ? <br>Because x=a, y= g(z)<br> Unification gives, [a/x, g((z)/y]
<br>Because xin place of a, y in place of g(z) <br>

- with both the substituitons, the first expression will be identical to the second expression & the substitution set will be [a/x, g((z)/y]


### Unifcation Conditions
- Predicate symbol mst be same, atoms or expression with different predicate symbol can never be unified. ( p/p)
- number of arguments in both expressions must be identical (number of argument 2/2)
- unification will fail if there are two smiliar variables present in same expression

### Unification Algo
=> algorithm, unify (l1, l2)

#### STEP1
- If l1 or l2 is a variable or constant, then: <br> If l1 & l2 are identical return "NIL"
- Else if L1 is a variable, then if L1 occurs in L2 then return FAIL,<br> Else return {(L1/L2)}
- Else if L2 is a variable, then if l2 occrs in l1 then return Fail, <br> Else return {(L1/L2)}
- Else return FAIL

#### STEP2
If the initial predicate sumbol in l1&l2 are not identical, then return FAIL.

#### STEP3
If l1&l2 have different number of arguments, then return fail.

#### STEP4
Set SUBST to nil

#### STEP5 
Loop: <br>
for in<-1 to no f argments in l1: <br>a) call the unify with the ith argument of l1 and the ith argument of l2 putting result in s <br>b) if s=FAIL then return FAIL<br>if s is not equal to NIL Then<br> (i) apply s to the remaind of both l1&l2<<br>(ii) subs= append (s1,subst)

#### STEP6
return SUBST

###  Algo Implementation
#### Step1; Initialize the substituion set be empty
#### Step2; recursively unify atomic sentences <br>a) check for identical expression match<br>b)if one expression a variable and other is a term which does not contain variable vi then:<br> ->substitue ti/vi<br>-> add ti/vi to the substitution settlist<br>->if both the expressions are functions, then functions must be similar & number of arguments must be same in both expressions. <br> eg: p(x,f(y)) and   p(a,f(z) ===> f must stay f!!!

<img src="example-unification.png">


# Resolution
Resolution is a theorem proving technique that proof by contradictions.<br> It is used, if there are various stunts are fiven & need to prove a conclusion of those stunt. <br>Unification is key concept in proofs by resolutions<bbr>resolutions is a single reference rule which can efficiently operate on conjunctive normal form or clausal form.
> clause: dijunction of literals is called clause. 

> conjunctive NF: a sentence represented as a conjunction of clauses said to CNF.

## Steps for resolution
1- conversion of facts into FOL<br>
2- conver FOL stunt into CNF<br>
3- negate the stunt which eed to prove by contradiction<br>
4- draw  resoution graph (unification)<br>

Examples:
a- John likes all kind of food <br>
b- apple and vegetable are food <br>
c- anything anoyone eat and not killed is food <br>
d- anil eats peanuts and still alive.<br>
e- henry eats everything that hanry eats<br>
h- prove by resolution that  John likes peanuts<br>


## Step 1 conversion of facts into FOL
 a-  ∀x: food(x) -> likes (John, X) <br>
 b- food (apple) and food (vegetablees)<br>
 c- ∀x∀y: eats(x,y) and not killed(x) -> food(y)<br>
 d- eats(anit, peantu)and alive(anil)<br>
 e- ∀x: eats (anil,x) -> eats(hanry, x)<br>
 f- ∀x: not killed(x) -> alive<br>
 g- ∀x:alive(x)->killed(x) <br>BOTH ARE ADDED PREDICATES<br>
 h- likes(John, Peanuts)
 
## Step2: conversion of FOL int CNF
 This makes it easier for resulution proofs
 
 ### 1- Eliminiate all implications -> & rewrite
 
 -  The foruma: a->b= NotA or B
 
 a-  ∀x: Not food(x) OR likes (John, X) <br>
 b- food (apple) and food (vegetablees)<br>
 c- ∀x∀y: not[ eats(x,y) and not killed(x)] OR food(y)<br>
 d- eats(anit, peantu)and alive(anil)<br>
 e- ∀x: noteats (anil,x) or eats(hanry, x)<br>
 f- ∀x: not [not killed(x)] or alive<br> 
 g- ∀x:not[alive(x)] or killed(x) 
 h- likes(John, Peanuts)
 
 ### 2- Move negation (not) inwords (inside) "oncher el no"
 a-  ∀x: Not food(x) OR likes (John, X) <br>
 b- food (apple) and food (vegetablees)<br>
 c- ∀x∀y: not  eats(x,y) or  killed(x)] and food(y)<br>  //change
 d- eats(anit, peantu) and alive(anil)<br>
 e- ∀x: noteats (anil,x) or eats(hanry, x)<br>
 f- ∀x: not [not killed(x)] or alive(x)<br> 
 g- ∀x:not[alive(x)] or not killed(x) //changes dunno
 h- likes(John, Peanuts)
 
 ### 3- Rename variables or standardize variables
 
 a-  ∀x: Not food(x) OR likes (John, X) <br>
 b- food (apple) and food (vegetablees)<br>
 c- ∀y∀z: not  eats(y,z) or  killed(y)] and  food(z)<br>  //change
 d- eats(anit, peantu) and alive(anil)<br>
 e- ∀x: noteats (anil,x) or eats(hanry, x)<br>
 f- ∀g: not  killed(g)] or alive(g)<br> 
 g- ∀k:not[alive(k)] or not killed(k) //changes dunno
 h- likes(John, Peanuts)
 
 ### 4- Eliminate existential instantioation quantifier by eliminiation
But in our case there is no existential stuff, so all remain same

### 5- drop universal quantifiers: (qlqsoit x,y or ilexiste etc)
 a-   Not food(x) OR likes (John, X) <br>
 b- food (apple) and food (vegetablees)<br>
 c-  not  eats(y,z) or  killed(y)] and  food(z)<br>  //change
 d- eats(anit, peantu) and alive(anil)<br>
 e-  noteats (anil,x) or eats(hanry, x)<br>
 f-  not  killed(g)] or alive(g)<br> 
 g- not[alive(k)] or not killed(k) //changes dunno
 h- likes(John, Peanuts)
 

## Step3: Negate the statement to be proved
On this stunt, we will apply negation to the conclusion stunt, which will written as (not likes(job, peanuts)

## Step4: Draw resolution Graph
Now, in this step, we will solve the problem by resolution tree using substitution, for the above problem it wll be given as
 
<img src="GRAPH-IDK-YET.png" > 

{} Hence Proved (empty)

### Examples of Resolution<br>
  
#### Structue:Stp1:step2
  
- If it is sunny & warm day you will enjoy: sunny and warn -> enjoy: not sunny or warn or enjoy:<br>
- if it is rainy you will get wet: raining ->wet: not raining or wet:<br>
-  it is a warn day: warn<br>
- it is rainning: rain<br>
- it is sunny: sunny <br>
  
  
- goal; u will enjoy, **STEP 3**. Negate the statement that u need to prove so? => Not enjoy
  
  **step4**: draw the graph
  
  <br>Not enjoy ( take frist statement with it cause it's contraduction to it) <br>
  <br>
  Not enjoy-----------Not sunny or not worm or enjoy ( apply unification method))  equal <br>not sunny or not warm ( now fine where there is not warm and not sunny but dont take the one with exact ex the second NO!)
  
  <br> take the third step with it( it is warm day) <br> notsunny or not warm ---- warm equals not sunny<br>
  
  Check where there is contradiction(the negative of it) so find where there sunny ( last option)
  not sunny -- sunny = {} contrdiction proved.
  
  

# Forward chaining/Reasoning
It is a form of reasoning which starts with atomic sentences in the knowledge base and applies inference rules in the gorward direction to extract more ddata until  a goal is reached.  

## Properties
  - it moves from bottom to top
  - it is a process of making a conclusion based on knownn facts or data, by starting from the initial state and reach the goals
- forward chaining approach is alson called a s data driven as we reach to the goal using availablen data
- forward chaining approach is commonl used in the expert system.
  
## Example1
Rule1: if A and C hen F: a&c->f <br>
Rule2: if a and e then a: A&E->A<br>
Rule3: if b then E: B->E <br>
Rule4: if a then d: C->D <br>
  
 
 **Database: AB <br>
  Problem: Proove if a and B true, then d is true: meaning i have to prove A&B->D 
  
  <img src="chaining.png" >
  
  
  ## Example2
  
  oal state: Z <br>Termination condition; Stop if z is derived or no further rule can be applied.
  
  <br>facts: a e b c <br>
  rules: f&b->z<br>c&d->f<br>a->d
  
  <img src="chaining2.png" >

  
# backward chaining
A backward chaining algorithm is a form of reasoning which starts with the goal and works backward, chaining through rules to find know facs to support the goal.
  
## Properties of backward chaining
- It is known as a top down approach
- Backward chaining is based on modus ponens inference rule
- in backward chaining,  the goal is broken inton sub goal or sub goals to prove the facts true.
- it is also called goal driven approach "while the above is data driven approach" as a list of goal decides which rules are selected or used.
- The algorithm is used in game theory, automatic theory proving tools , inference engines, proof assistans and various apps
- The backward chaining method mostlyb used a depth first search strategy for prrof
  
 ## EXAMPLE1 
<img src="backward1.png" >

 ## Compare Forward and backwward
<img src="compare1.png" >
  
  <img src="compare2.png" >
  
<img src="compare3.png" >


  
# AI Techniques

## Search
This technique provides a way of solving problems far no more direct approach is available as well as a framwework into which any direct techniques that are can be embedded.
  
## Use of Knowledge 
This technique provides a way solving complex problem by explointing the structures of the object that are involved.
  
## Abstraction
This technique provides a ay of separating important features and variations from the many **unimportant ones** , it hides the details of something.  
<br>Eg; if we wan to compute the square root of a no: then simply we call the fun tion sort in c. we do not need to know the implementation details of tis function. <br> eg, #include<stdio.h>; math.h etc.

## Conclusion
  AI technique is a method that exploits knowledge that should be represented in:
-  the knowledge captures generalizations
-  it can be understood by people who must provide it
-  it can easily be modified to correct erros and to reflect changes in the world and our world view.
-  IT CAN be used in great many situations even if it is not totally accurate.
  
---
  
# Scopes of Artificial Intelligence
  
## Game Playing | Scope of AI
Game playing is a search problem designed by, 
  - initial state
  - succesor function
  - goal test
  - path cast/utility/pay off function
AI has continued to improve with aims set on a player being unable to tell the difference between computer and human player.  
  
<br>A game must feel Natural
  - Obey laws of the game
  - characters aware of the environement
  - path findings (a algo)
  - decision making
  - planning

The Game AI is about the illusion of human behavior
  - smart to a certain existent
  - non repeating-behavior
  - emotional influences ( irrationality, personality)
  - body language and communicate emotions
  - being integrated in the environment
  
  
Game AI needs various computer science disciplines:
  - Knowledge based systems
  - Machine learning
  - Multi Agent systems
  - Computer Graphics and animation
  - data structures
  
### Computer Games Type 
#### 1- Strategy Games
  - Real time strategy (RTS)
  - Turn based strategy (TBS)
  - Helicopter view
#### 2- Role playing Games
  - Single player
  - Multi player
#### 3- Action Games
  - First person shotter
  - first person sneaks
#### 4- Sport Games
#### 5- Simulations Games
#### 6- Adventure Games
#### 7- Puzzle Games
#### 8- ETC your innovation ;)

  
  
## Natural Language Processing NLP | Scope of AI
 We use the englsh lang to communcate between an intelligent system and NLP. Processing of NL plays an important role in various systems. <br>
  
  Example: 
  - Robot, it is used to perform as per your instructions
  - the input and output of an NLP system can be. speech or writen text.
  
  
  ### Components of NLP
  #### 1- Natural language understanding
  - basically, the mapping to given input output in NL into usefull representation.
  - analying different aaspects of the language
  
  #### 2- Natural language generation NGL 
  We have to produce meaningfu phraes and sentences that is in the form of Natural language from internal representation  
  - text planning
  - sentence planning
  - text realization
  
  ### Difficulties of NL unit
#### 1- Lexical ambiguity  
  It is a predefined at a very primitive level such as world-level
#### 2- Sytax level
It this, we can define a sentence in a parsed way or in a different way
  
#### 3- Refrential ambiguity  
  It says that we have to refer ti something using pronouns
  
### Step in NLP 
#### 1- Lexical analysis
we have to analyze the structure of the words. the collection of words and phrases in lang is lexicon of a lang.
  
#### 2-  Syntactic analysis (Parsing)
  we use parsing to the analysis of the word. Although, have to arrange words in an particular manner to show the relationship between the words.
  
#### 3- Semantic analysis 
  it describes a dicitonnary meaning which is leaning in the last domain. mapping syntatic structrure and objects
  
#### 4- Discourse Integration
  It this step, the meaning of any sentence depends upon the meaning of the previous sentence. In addion, it brings the meaning to immedaiattlt succeeding sentence
  
#### 5- Programtic Analysis
 In this step data is interpreted on what is actually meant. although we have to derive aspects of the language which reqiuires real world knowledge.
  
---
 
  
## Expert Systems | Scope of AI
The expert systems are the computer applications developed to solve complex problems in a particular domain, at the level of extraordinary human intelligence and expertise.
### Characterestics of Expert Systems  
 - high performance
 - understanable
 - reliable
 - highly responsive 
  
### Characterestics of Expert Systems  
  
#### Capable of
- Advising
- Introducing and assting human in decison making
- Demonstrating
- Deriving a solution
- Epxplaining
- Interpreting input/output
- Predicting results 
- suggesting alternative options to a problem
  
#### INCapable of
- substituting human decision makers
- processing human capabilities  
- produce accurate o/p for inadequate knowledge base  
-  Refining their own knowledge
  
### Components of Expert Systems
  - knowledge base
  - inference engine
  - user interface
  
<img src="componentsES.png" >
  
#### 1- Knowledge base
- It contains domain specific and high quality knowledge
- Knowledge is required to exhibit intelligence
- the success of any expert system depends upon the collection of highly accurate and precose knowledge  

#### 2- Inference Engine
 It is the brain of the epert system. It contains rules to solve a specific problem. It selects facts and rules  to apply when trying to answer the user query. It provies reasoning about the information in the knowledge base. Inference enginer helps in deducing th problem to find the solution. This comonent is also helpful for formatiting conclusions.
  
#### 3- User Interface
- The user interface is the most crucial part of the expert system. This component takes the user uery in a readable form and passes it to the inference engine.
  
-  After that, it displays the result to the user. Onn other world its an interface that helps the user communicate with the expert system.
  
### The process of building an Expert Systems
- Determining the characterestiics of the problem
- KNowledge engineer and domain expert work in coherence to define the problem
- the knowledge engineer translates the knowledge into a computer understandabe language. He designs an inference engine in a reasoning strcucture, which can use knowledge when needed
- the knowledge expert also determines how to integrate the use of uncertain knowledge in the reasoning process and what type of explanation would be useful.
 
### Expert Systems Applications
- Information management
- Hospitals and mediical facilities  
- help desks management  
- **employee performance evaluation**  
- loan analysis  
- virus detection  
- warehouse optimization  
- planning and scheduling
- process monitoring and control
- stock market trading
- airline scheduling and cargo scheduling

---
  
## Robotics | Scope of AI
  
  
## Learning from Observation 
  
## Inductive Learning
  
## Decision Tree Learning Algo
  
# AI - Application
