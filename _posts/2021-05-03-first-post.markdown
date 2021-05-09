---
layout: post
title:  "First post"
date:   2021-05-03 17:33:25 +0200
categories: category-theory
---

This blog will be dedicated to whatever I feel like writing about on any given
week. This will likely be some combination of research notes, musings on
category theory (especially basic category theory) and physics, and even some
more far out stuff, like baking or cooking. The emphasis will be on quantity
over quality---I want to write something at least every other week, no matter
how small. Any research notes I write will probably be incomprehensible to
anyone other than me and (if I'm having a good day) my advisor.

Broadly speaking, I'm interested in homotopy theory, especially higher category
theory. For tax purposes, that makes me a topologist of sorts, although I never
formally learned any point-set topology, and my intuition is pretty much
useless outside of things which are at least as nice as CW complexes. I'm
really more of a category theory fanboy.

Category theory has been fairly fashionable recently, and there is a lot of
effort going into making it easy to understand and teach. A lot of the current
teaching methods follow the historical development of category theory, treating
categories are structured containers for algebraic data. Viewed in this way,
the objects in our category are thought of as abstracted algebraic gadgets of
some sort; sets, groups, rings, or whatever; the morphisms are then
abstractions of maps between them.

There's a reason this is the norm, and I would never advocate for doing away
with it. However, I think there's a lot to gain by the homotopy-theoretic point
of view: categories are simultaneously a generalization of, and a special case
of, topological spaces. For me, many things in category theory lose a lot of
their mystery when viewed this way, and there's a lot to be gained by playing
these two points of view off each other.

![algebra and geometry]({{ site.url }}/assets/images/algebra_and_geometry.png){: .center-image }

My next blog post will be a concrete example of this: the definition of a
natural transformation. This is the first non-trivial definition you see when
you set out to learn category theory, and it's usually taught in a way that
seems kind of unfortunate to me. The definition usually isn't motivated in its
own right; rather, one is given a list of all of the (many!) familiar concepts
in algebra that turn out to be natural transformations. It's even often claimed
that it gives a formalization of the idea of 'naturality' or 'canonicalness',
which I think is overselling things a bit.

The definition is, in my opinion much easier to motivate if we think of
categories as directed topological spaces, and transport the definition of a homotopy directly from topological spaces to categories.

![Natural transformations as homotopies]({{ site.url }}/assets/images/functors_as_natural_xfos.png){: .center-image }

I'll be a bit cagy about what I mean by this at the moment, but we should have
the following rough dictionary.

| category theory                                                 | topology                      |
|-----------------------------------------------------------------|-------------------------------|
| category $$\category{C}$$                                       | topological space $$X$$       |
| functor $$F: \category{C} \to \category{D}$$                    | continuous map $$f: X \to Y$$ |
| natural transformations $$\eta: F \Rightarrow G$$               | homotopy $$H: f \sim g$$      |

But I'll write more about this next week.
