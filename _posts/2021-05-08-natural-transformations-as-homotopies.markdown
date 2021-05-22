---
layout: post
title:  "Natural transformations as homotopies"
date:   2021-05-08 17:33:25 +0200
categories: category-theory
---

As I wrote last time, I think that category theory has a lot to gain from
topological thinking. I would now like to make good on my threat to give an
example: natural transformations, as understood via homotopies.

First, the definition, so that we're all on the same page. 

**Definition.** Let $$X$$ and $$Y$$ be topological spaces, and $$f$$, $$g\colon
X \to Y$$ maps.  Denote by $$I$$ the closed interval $$I = [0, 1]$$. A _homotopy_
from $$f$$ to $$g$$ is a map $$H\colon X \times I \to Y$$ such that $$H|_{X
\times \{0\}} = f$$ and $$H|_{X \times \{1\}} = g$$.

We can draw $$f$$ and $$g$$, and their images in $$Y$$, like so.

![f and g]({{ site.url }}/assets/images/f_and_g.png){: .center-image }

The data of a homotopy $$H$$ from $$f$$ to $$g$$ then looks like this.

![f g and h]({{ site.url }}/assets/images/f_g_and_h.png){: .center-image }

If we view the interval $$I$$ as parametrizing some sort of time, then we can view a homotopy as providing a deformation of $$fX$$ into $$gX$$.

![homotopy]({{ site.url }}/assets/images/homotopy.gif){: .center-image }

My claim is that we can understand natural transformations in terms of
homotopies. Again, I'd better give the definition of a natural transformation
so we're all on the same page.

**Definition.** Let $$\category{C}$$ and $$\category{D}$$ be categories, and
$$F$$, $$G\colon C \to D$$ functors. A natural transformation $$\eta$$ from
$$F$$ to $$G$$ consists, for each object in $$\category{C}$$, a morphism
$$\eta_c$$ such that for each morphism $$\phi\colon c \to c'$$ in
$$\category{C}$$, the square

![square]({{ site.url }}/assets/images/commuting_square.png){: .center-image }

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

