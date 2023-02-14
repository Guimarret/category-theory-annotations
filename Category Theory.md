
Pure functions is the base of everything in programming 

functions Math special kinds of relations (Sets with elements that pairs)

Set of pairs forms the cartesian product

Function Domain is the Set in equivalence 
The set that is connected is the codomain this also have the image 

The direction is defined by possibility to exist a inverse function

- f  :: a -> b   
- g :: b -> a
_______
> g . f = id </br>
> f . g = id

The point between the functions are "after"

This is isomorphism 

![1](/images/Bartosz%20Milewski/Pasted%20image%2020230119230126.png)

	Extracting                                     Modeling

Injective functions dont colapse as it happen in "Extracting" (Monic)
- Monomorphism
	- ![Pasted image 20230119232842.png](/images/Bartosz%20Milewski/Pasted%20image%2020230119232842.png)

Surjective function colapse like the "Modeling" example (Isomorphism too btw) (Epic)
- Epimorphism
	- 	- ![Pasted image 20230119232406.png](/images/Bartosz%20Milewski/Pasted%20image%2020230119232406.png)

### Void
 
>F :: Void -> a
   id :: Void -> Void

This function is named absurd
Void by logic corresponds to False

### Unit

> ( ) :: ( ) -> True
   unit :: a -> ( )

one :: ( ) -> Int
two :: ( ) -> Int ...

#### Order

- Basically comparison
	- ![Pasted image 20230120092725.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120092725.png)
- 

Home-set: _The set or collection of all morphisms from A to B for some given ordered pair (A, B) of objects from some given category_

#### Monoid

_The Monoidal Category is **a Category in which you can “multiply” objects using some kind of a tensor product (⊗) and which also has a special object I that is the unit of multiplication**_

Binaries operation defines as a base every element in the monoid
Like a multiplication of natural numbers
String Contatenation

A monoid can be compared to a lightly typed language 

#### Kelisli category

Definition: _In category theory, a Kleisli category is **a category naturally associated to any monad T**. It is equivalent to the category of free T-algebras. The Kleisli category is one of two extremal solutions to the question Does every monad arise from an adjunction? The other extremal solution is the Eilenberg–Moore category._

Functions return ( < x >) proving in java/c++

![Pasted image 20230120120632.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120120632.png)

Functional programming we don't really stops in composing functions
We compose bunch of operations using function composion, but also use differents compositions making the code freedom more vast

![Pasted image 20230120121245.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120121245.png)

#### Terminal and initial Objects

Important definition: _Initial and terminal objects are not required to exist in a given category. However, if they do exist, they are essentially unique. Specifically, if I1 and I2 are two different initial objects, then there is a unique isomorphism between them. Moreover, if I is an initial object then any object isomorphic to I is also an initial object. The same is true for terminal objects. 

Arrows in Kleisli are differente from de other category types

(m = maps type to type)

![Pasted image 20230120121824.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120121824.png)

Implementation of Kleisli arrow in C category | 

In general the composition are differente even if is the "same" arrow just in different domains

The Id function are also differente:

![Pasted image 20230120122037.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120122037.png)

Remembering Monad is  : _In category theory, a branch of mathematics, a monad (also triple, triad, standard construction and fundamental construction) is a monoid in the category of endofunctors. An endofunctor is a functor mapping a category to itself, and a monad is an endofunctor together with two natural transformations required to fulfill certain coherence conditions._

### Singleton sets

definition: _In mathematics, a singleton, also known as a unit set or one-point set, is a set with exactly one element. For example, the set { 0 } is a singleton whose single element is 0._

![Pasted image 20230120124037.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120124037.png)

- _In Category theory the singleton is a terminal object in the category Sets of sets, and no other set are terminal_
- _Any singleton admits a unique topological space structure (both subsets are open). These singleton topological spaces are terminal objects in the category of topological spaces and continuous functions. No other spaces are terminal in that category._
-  _Any singleton admits a unique group structure (the unique element serving as identity element). These singleton groups are zero objects in the category of groups and group homomorphisms. No other groups are terminal in that category._

Event Bool as set can receive 2 arrows ( True and False) but singleton just receive one.

![Pasted image 20230120124733.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120124733.png)

1) Furst math representation - For all object A there exists a F thats goes from A to the terminologic

#### Initial Object

Definition: _In category theory, a branch of mathematics, an initial object of a category C is **an object I in C such that for every object X in C, there exists precisely one morphism I → X**._

Easier way to remember: Categorically initial object is as object that has an unique outgoing arrow to every other object

Disclaimer: Until now we just compare arrows to other arrows but don't  compare objects to other objects

#### Products

For every category there is another category that have the same objects with inverse arrow
![Pasted image 20230120131445.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120131445.png)
![Pasted image 20230120131559.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120131559.png)

 Partition products:

 ![Pasted image 20230120132548.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120132548.png)

Real projection definition:

![Pasted image 20230120133042.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120133042.png)

![Pasted image 20230120133503.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120133503.png)

It becomes exponencially complex when we think about multi-arrows, because the arrows start to point at a multidimensional image, in this case a cube pointing to one point:

![Pasted image 20230120134230.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120134230.png)

In categorical products :

![Pasted image 20230120134520.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120134520.png)

it's important to point that the 
m ° p = q1 
m ° p = p1

as also told before
The C and C1 are set of rules and the C of  "p" and "q" are called the product of A and B

*Important: Not all category have products, but in a category of sets, all sets have products, including initial objects, terminal objects, etc*


#### Coproducts, sum types

Besides the product that makes projections, now what happens is injections
Coproduct ( C ) is a object with a pair of injections such as any other object that has a injection from A to C' and B to C' has a unique morphism M from C to C'

![Pasted image 20230120140115.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120140115.png)

C also is a perfect match from A and B images exactly like a Union and the M finds the exactly point of C' that also is part of the system.

The canonical way to describe a pair in haskell is ( a, b )

In the "Projection" that's the inverse system, the equivalent of I and J of the last image is called "Fst" and "Snd" while in the "Injection" is Left A and Right B

```Haskell
X :: Either Int Bool

F :: Either Int Bool -> Bool

F(Left I) = i > 0

F(Right b) = b
```

In other languages it's just < a, b > (Pairs)

The haskell representation for a pair of Projection

```Haskell
data Point = P Float Float
P { x :: Float
	y :: Float
   }
```

#### Algebraic data types

```Haskell
( a, b ) ( b, a )

swap :: ( a, b ) -> ( b, a )
swap p = ( snd p, fst p )

(( a , b ), c) ~ ( a, ( b , c))
assoc ((a, b ), c) = (a, ( b, c))

( a, () ) ~ a => a * 1 = a

mUnit ( x, () ) = x or mUnit = fst
mUnit_inv x = ( x, ())
```

- These are isomorph examples

Either a b ~ Either b a

( | in haskell are guardian that's basically a multi option like if else chain)
data triple a b c  = Left a | Right c | Middle b

Either a Void ~ a
a + 0 = a

a * 0 = 0
( a , Void ) ~ Void

a * ( b + c) = a * b + a * c
( a, Either b c ) ~ Either ( a , b ) ( a , c )

It is like a Ring, but mathmatically Ring has an inverse, what isn't the case now because we don't know the inverse of a Integer so we call it Rig.

2 = 1 + 1
We can think that 2 is a boolean and the 1 called the True or False

1 + a
data Maybe a = Nothing | Just a
Either ( ) a

![Pasted image 20230120182256.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120182256.png)

data List a = Nil | Cons a ( List a )

Infinit list definition

![Pasted image 20230120182559.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120182559.png)
![Pasted image 20230120182610.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120182610.png)
 
#### Functors

Definition: _A Functor is **kind of mapping of objects and morphisms that preserves composition and identity**. We have two Categories: A and B . In Category A we have two objects a and b with morphism f . Our Functor is a mapping of objects a and b to Fa and Fb and mapping of morphisms, in this case single morphism: f to Ff_

Pattern matching definition is basically the recognition of patterns between categorys

Functors must preservate the composition and identity:
![Pasted image 20230120204251.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120204251.png)
Injective functors on home-sets are called Faithfull

In Haskell objects becomes types and morphisms become functions and the type constructor is the mapping of types and also functions

 ![Pasted image 20230120204917.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120204917.png)

There is the object mapping too that is the mathematical way to the Morphism in haskell 

![Pasted image 20230120205850.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120205850.png)

data Maybe a = Nothin | Just a 

This is Morphism to and the f in haskell are the => fmap f so:

![Pasted image 20230120205635.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120205635.png)

Some haskell typing functor and examples: 

![Pasted image 20230120212802.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120212802.png)
![Pasted image 20230120213805.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120213805.png) 

The last image is the definition of the actual map function in haskell, it's a recursive function that verifies a list of T in the case, btw the Cons is a historical name for constructors 

![Pasted image 20230120214818.png](/images/Bartosz%20Milewski/Pasted%20image%2020230120214818.png)

This is kinda funny too because we find the Reader function is a ( . ) actually in a logical conclusion by removing repeated f g in the Fmap.

Definition: _The Reader monad is useful when you have a long chain of function invocations where only some of the functions in the chain make direct use of a piece of “shared environmental state”. This “environmental state” could be anything. It could be as simple as a primitive value or it could be a record containing configuration values your program needs in certain places. Doesn’t matter._

- Vector is a container of elements

Function can be seem as containers

- In Haskell all data types are thunks, there are functions that can be evaluated to return a value  
- Data arte really functions and functions are really data
- Applying a function to a value dont obligate him to be evaluated
- Sometimes the functions will only be applyied when the value appears, that doesnt mean that it's gonna be in the beggining

Definition of thunks: _A thunk is a value that is yet to be evaluated. It is used in Haskell systems that implement non-strict semantics by lazy evaluation.

Functoriality

 
![Pasted image 20230121112747.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121112747.png)

This representation is interesting because usually we don't think in the tail representation as a risk, but if naturally the function was [a]   -> Mayba [a] there wouldn't be any problem related to crash the program in execution, because would raise an exception for empty lists

Representation of a bifunctor:
 ![Pasted image 20230121113818.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121113818.png)

Is really game changer to start thinking that you can think of a set merge, in this case the CxD that generates a new conception in functors constructs

Applying to haskell, it's possible to project a class Bifunctor where we  get a bimap that accept two functions as represented:
![Pasted image 20230121114229.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121114229.png)

F is the bifunctor that gets the A and B, as a compiler it means that the F is getting two types as arguments (btw type constructor of two types)

- Basically taking two types that makes a third its a bifunctor

![Pasted image 20230121120625.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121120625.png)

Easy way to go from AxB -> A' x B'
And the logical representation of this is in the image  

By logic if we apply the equivalent for a comparison of A and unit() it becames even easier:  


![Pasted image 20230121121101.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121121101.png)  



Bifunctor with bifunctors inside:  
  

![Pasted image 20230121122137.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121122137.png)  

Practical situation would be something in this scheme:
	LANGUAGE DeriveFunctor
	Data Maybe = .....
			deriving Functor

Profunctor   

![Pasted image 20230121123526.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121123526.png)  

It's like the bifuntor but the category that compares C x C in this case have one of these C inverted to get the inverse value doing the basic a -> b
Sequence of the last image:

  
![Pasted image 20230121123727.png](/images/Bartosz%20Milewski/Pasted%20image%2020230121123727.png)
  
#### Function objects

Function creation in haskell and curry:

  
![Pasted image 20230123144131.png](/images/Bartosz%20Milewski/Pasted%20image%2020230123144131.png)  
  
![Pasted image 20230123144210.png](/images/Bartosz%20Milewski/Pasted%20image%2020230123144210.png)  
  
- It's possible to a type be exponential, if we think bool -> int , it means that technically there are 2 int's as value possibility.

Observations: 
  
![Pasted image 20230123183332.png](/images/Bartosz%20Milewski/Pasted%20image%2020230123183332.png)
  
#### Natural transformations
  
![Pasted image 20230124201220.png](/images/Bartosz%20Milewski/Pasted%20image%2020230124201220.png) 

Haskell equivalent:
```Haskel
alpha :: forall a. F a -> G a
```
  
![Pasted image 20230124230657.png](/images/Bartosz%20Milewski/Pasted%20image%2020230124230657.png)
   
#### 2 - Category / Bicategories
   
A category that have 2 categories inside and in this case are functors categories, that also get vertical and horizontal escalability:  
   
- ![Pasted image 20230124232555.png](/images/Bartosz%20Milewski/Pasted%20image%2020230124232555.png)
   
- [ C , D] = D^c => functor 

There are vertical compositions too

![Pasted image 20230124233222.png](/images/Bartosz%20Milewski/Pasted%20image%2020230124233222.png)

Kinda like a vertical escalation, this also get's exponencial possibilities

![Pasted image 20230124233628.png](/images/Bartosz%20Milewski/Pasted%20image%2020230124233628.png)

#### Monads

definition: _A monad is **an algebraic structure in category theory**, and in Haskell it is used to describe computations as sequences of steps, and to handle side effects such as state and IO. Monads are abstract, and they have many useful concrete instances. Monads provide a way to structure a program._

##### Fish operator:
![Pasted image 20230128191526.png](/images/Bartosz%20Milewski/Pastedimage20230128191526.png)

##### Monad specifically in haskell means:
![Pasted image 20230128192031.png](/images/Bartosz%20Milewski/Pastedimage20230128192031.png)

![Pasted image 20230128194807.png](/images/Bartosz%20Milewski/Pastedimage20230128194807.png)

![Pasted image 20230128194519.png](/images/Bartosz%20Milewski/Pastedimage20230128194519.png)

![Pasted image 20230128201546.png](/images/Bartosz%20Milewski/Pastedimage20230128201546.png)

![Pasted image 20230128201653.png](/images/Bartosz%20Milewski/Pastedimage20230128201653.png)

Changing symbols to the next annotation prints

![Pasted image 20230128204511.png](/images/Bartosz%20Milewski/Pasted%20image%2020230128204511.png)

Proving that Identity is the same data as T

![Pasted image 20230128210958.png](/images/Bartosz%20Milewski/Pasted%20image%2020230128210958.png)

Re-watch natural transformation and monads to understand better before going to the next chapter...











