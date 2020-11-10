# Exploring Non-Linear Interpolation (NLI)

→ Full post at [github.com/arrowtype/NLI-test](https://github.com/arrowtype/NLI-test/)

→ Web demo of [NLI in variable TTFs](https://arrowtype.github.io/NLI-test/)

→ Discussion on Twitter: [Part 1](https://twitter.com/ArrowType/status/1325648820101853184), [Part 2](https://twitter.com/ArrowType/status/1326011356605272065)

Ever since [Underware Type started exploring what they call HOI (Higher-Order Interpolation)](https://underware.nl/case-studies/hoi/), I’ve been amazed by the creative possibilities of this approach to interpolation, and I’ve wanted to try it myself.

For a long time, I didn’t get it. Then, I started to understand it, but felt like actually making it work would be nearly impossible (or super inefficient, at best). But, I’ve taken another look and got a functional test working, so I’ve documented & shared my findings. I *still* feel like it would be nearly impossible to use in designing full typefaces, so I am doubly impressed, and hope that Underware might eventually license their internal tools to allow others to put HOI into practice.

One possibility I hadn’t considered until recently: using a slightly-simplified “quadratic” approach, non-linear interpolation now feels more within reach – but maybe the results of the “cubic” approach are so much better, it is worth the extra complexity.

I’ve made some tests sources, a web demo, and a written explanation of the theory from my perspective & understanding (links above).

![NLI](web-demo.gif)

Hopefully this helps someone else understand NLI a little better, too!
