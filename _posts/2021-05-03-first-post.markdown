---
layout: post
title:  "First post"
date:   2021-05-03 17:33:25 +0200
categories: category-theory
---

ROUGH DRAFT -- I hope to add some hand-drawn illustrations.

This blog will be dedicated to whatever I feel like writing about on any given
week. Some research notes, some musings on category theory and physics, and
even some more far out stuff, like baking or cooking. The emphasis will be on
quantity over quality---I want to write something at least every other week, no
matter how small. Any research notes I write will probably be incomprehensible
to anyone other than me and (maybe) my advisor anyway.

My research is, broadly speaking, about homotopy theory. I guess that makes me
a topologist of sorts, although I never formally learned any point-set
topology, and my intuition is pretty much useless outside of things which are
at least as nice as CW complexes. I'm really more of a category theory fanboy
than anything else, but I'm interested in the topological, homotopy-theoretic
notions of category theory.

Category theory has been fairly fashionable recently, and there is a lot of
effort going into making it pedagogically tractable. However, a lot of the
current teaching methods are still based on viewing categories as structured
containers for algebraic data: we think of the objects in our category as
algebraic gadgets of some sort; sets, groups, rings, or whatever, and the
morphisms as abstractions of maps between them. I think there's a lot to gain
by the homotopy-theoretic point of view: categories are simultaneously a
generalization of, and a special case of, topological spaces.  For me, many
things in category theory lose a lot of their mystery when viewed this way, and
there's a lot to be gained by playing these two points of view off each other.

I'd like to kick the blog off by giving a concrete example of this: the
definition of a natural transformation. The first definitions one is confronted
with when one studies categories are (1) categories themselves, and (2)
functors between categories. Both of these are easily digestible: anyone who is
learning about categories presumably wants to know what a category is, so the
definition of a category motivates itself. The definition of a functor is then
completely natural: functors are the structure-preserving maps between
categories. This fits in well with the way category theory presented.

Then comes the definition of a natural transformation:

Let $$\category{C}$$ and $$\category{D}$$ be categories, and $$F$$, $$G\colon C \to D$$ functors. A natural transformation
eta from F to G consists, for each object in c, a morphism eta_c such that for
each morphism phi: c -> c' in C, the square

SQUARE

commutes.

As is so often the case in math, no a priori reason is usually given for this
definition; the motivation comes from the examples one finds. In my experience,
and the experience of several people I know who have studied some category
theory as interested amateurs rather than as mathematicians, natural
transformations tend to be where people give up.

Note that we have a similar situation in topology:

Let X and Y be topological spaces, and f, g: X -> Y continuous maps. Let I
denote the interval [0,1]. A homotopy from f to g is a map H: X x I -> Y such
that H|0 = f and H|1 = g.

This definition has a nice geometric interpretation. We can view the interval I
as parametrized by some sort of 'time'. A homotopy then gives a continuous
deformation of the f into g. At time 0 we have f, and at time 1, we have g.

The claim is that we should think of categories as something like topological
spaces, and functors as something like continuous maps. Let us try to translate
the rest of the definition of a homotopy in the language of categories.

The first thing we need is the categorical version of the interval I. There is
an obvious choice when one is thinking geometrically: the category with two
objects 0 and 1, and three morphisms: the identity on 0, which we'll call 00,
the identity on 1, which we'll call 11, and the morphism 0 -> 1, which we'll
call 01. We will call this category [1].

We simply transcribe the rest of the definition with these modifications: 

A homotopy from F to G is a functor H: C x 1 -> D such that H|0 = F and H|1 =
G.

What information does a homotopy between functors F and G give us? In order to
give such a homotopy, we need to specify what H should do on objects and
morphisms. The objects in C x [1] are pairs (c, i), where c is an object in C and
i = 0 or 1. But the objects (c, 0) are specified by F, and the objects (c, 1)
are specified by G. So we get no choice.

Next, we need to specify what H does to morphisms. The category C x [1] has
three kinds of morphisms: those of the form (phi, 00), those of the form (phi,
01), and those of the form (phi, 11). The first type are specified by F and the
third type are specified by G. In fact, 

