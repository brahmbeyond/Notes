# AI


## Propositional Calculus
This defines as the statements which are either true or false. They should be anyone, These are like saying the **sky is blue**, true or false, that's it and nothing else. Like **5 is less than 10** which is true, here its confirmed.



## First order predicate calculus
This also tells true or false, but it depends upon the variable values. Like **'x' is greater than 10.** so now it depends upon the value of 'x' that if this is true or not. 


#### - Quantifiers 
These are to define the scope , to express the statement if for all or for some.
- Universal Quantifiers (∀): for all or for every
- Existential Quantifiers (∃): for some

#### - Connectives
Predicate calculus also uses logical connectives like AND (∧), OR (∨), NOT (¬), and IMPLIES (→) to combine predicates and form more complex statements.


#### - example:
Like we represent Sonu with 'S' then -
LovesMath(S) = means (S) Sonu love math.
***Sentence*** -  ∀S LovesMath(S)      ( for all S , love math)
means all Sonu loves math

 - It  solves  Propositional Calculus shortcomings as it depends on variables to tell if they are true or not.

## Horn Clause
It is specific type of rule system used in logic programming, a branch of AI used in knowledge representation and reasoning. Named after alfred horns in 1950s.
It is made of at most one positive literal(+ve statement) and any number of negative literal like if A & B are true then C is true.
***Example:*** If it barks,its a dog. Horns clause uses simplifies version of this in AI.
***Example:*** If HasFever(patient) ^ HasCough(patient) -> HasFlu(patient)
#### Benefits -
 - easier to understand
 - efficient reasoning
 - used in NLP, expert systems etc.

## Prolog
It stands for Programming in Logic, is a logical and declarative programming language specially designed for AI.
- **Declarative lang** - its not like other languages in which whole steps are written , instead facts and rules and problem is given , prolog will find the solution.
- **Logic-based** = its based on logic, means facts and rules and based on that its derives answers.
#### - Key features:-
- **Facts** = means basic statements like bird(sparrow).
- **Rule** =  anything to express and combine facts like `loves(john, X) :- loves(X, john). % If X loves John, then John loves X (rule)`
- **Queries** - ask questions based on the facts and rules you defined. like `bird(sparrow) ? - is sparrow a bird ?`
- **Unification and Backtracking**: - prologs finds the Ans based on facts and rules and if finds i , returns solution known as unification. But if doesn't then finds another possible solution known as backtracking
#### -Benfits
- easy
- good for reasoning
- flxible
#### - Applications
- Expert based systems - best as to capture and reason with human expertise in specific domain
- NLP - symbolic representation helps to understand language easier.
- rule based.


## Semantic Nets
Imagine a giant web of connection where the ideas and concepts are linked to each , that what a semantic net in AI is , a graphical representation of relationship between knowledge.
- nodes/concepts
- structure/arches/connection/.relationships

 Semantic networks are alternatives to the predicate logic for the knowledge representation technique.
benefits- 
- easy to represent and read
- related knowledge is easily clustered
```mermaid
graph LR
A[Car] --> B{is a vehicle} --> C{Engine}
A --> D{Has} --> E{Doors}
A --> F{Has} --> G{Wheels}

```

## Partitioned Nets
As semantic net can get messy with complex knowledge, so partitioned nets ia like extension to it or can say to complete its shortcomings.
In this network is broken into smaller parts.
Each partition focuses on particular  view point.
Examples:
```mermaid
graph LR
A[Car]
  --> B{Engine}
  --> C{Wheels}
```

```mermaid
graph LR
A[Car] --> B{provides transportation} --> C{Person}

```


## Minskey frames
Minskey frames is a technique to represent knowledge in structured format similar to how humans understand and store information.
The data is stored in form of 'frames' and each frame has slots and those slots contains some values.
- frames = like cars
- slots = like name,model,color
- fillers= maruti,208,blue

#### benefits - 

- nlp
- flexibility
Example:
```
Frame: Restaurant 
Slot: Has menu 
- Can be filled with: Italian food menu, Sushi menu, etc. 
Slot: Has seating
 - Can be filled with: Tables, booths, etc.
Slot: Serves food
 - Can be filled with: Italian food, Sushi, etc.
Slot: Has staff
 - Can be filled with: Waiter, Chef, etc.
```
#### limitations:
- time consuming for complex
- can't capture all values










