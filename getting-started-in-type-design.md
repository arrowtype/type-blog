# Getting started (or intermediate) in Type Design

## Main editors: Glyphs & RoboFont

Glyphs & RoboFont are the two editors I have familiarity with, and curently the two most-commonly used editors in type design. This post isn’t a comparison of the two. I 100% recommend either of them. Generally, Glyphs is more approacheable and feels more “Mac-like” as an app because it does some helpful things for you, while RoboFont is a bit more intimidating to get started with, but provides more flexibility because it is less “opinionated” about what tools you need.

I got started in Glyphs, and I now use RoboFont more. I use RoboFont largely because I like the way it encourages me to think about my workflow and consider what a given type family should be like. RoboFont is somewhat nicer for scripting (partly because it uses Python3), and its format is nicer for Git versioning. I also really like its approach to spacing. 

To be honest, more of my heroes use RoboFont, which was my initial motivation to use it, and I have since become slightly more fluent in drawing with it. But, there are many professionals who use Glyphs. Some studios even use both, though this takes some scripting to handle well. I have a lot of love for both programs!

## Getting started in Glyphs

Glyphs does an amazing job in tutorials & support. Check out https://glyphsapp.com/tutorials for advice on getting ready. The [Glyphs Forum](https://forum.glyphsapp.com/) provides excellent support, often faster than seems reasonably possible. There are great extensions for Glyphs, but I don’t really know much about these – see https://glyphsapp.com/extend for some good suggestions.

## Getting started in RoboFont

Due to its unopinionated nature, RoboFont can an intimidating program to get started in,. If you are just getting started (or if you’re just curious to see what I like), here’s some basic advice that may help get you off the ground.

The docs are pretty good at https://robofont.com/documentation/introduction/. Read through these, and keep clicking to the next page. Don’t get distracted by all the links in each page on the first read through – consider clicking them on subsequent reads.

If you have questions, the RoboFont Forum is very helpful: https://forum.robofont.com/. They usually answer questions within a day (many questions, of course, are already answered if you search for them).

### Tools

Find tools at https://robofontmechanic.com/.

Some of the free extensions I couldn’t work without:
- Mechanic, to handle extensions
- Add Overlap, to add corner overlaps to selected points
- Batch, to help you build fonts from RoboFont
- Glyph Browser, to make it easy to add specific glyphs with correct unicodes & naming
- DesignSpace Edit, to help set up designspace documents that you can build with FontMake
- EditThatNextMaster, to help working with multiple related fonts
- GlyphMirror, which I showed you
- Properties, to display distances in selected points, etc
- Ramsay St, to show related glyphs in the glyph view
- Shape Tool, to draw circles & rectangles
- SpeedPunk, as one way to consider the smoothness of curves
- word-o-mat, to create strings to judge type in the Space Center

Paid extensions:
- MetricsMachine is extremely worthwhile, to help with kerning. If you get this, MM2SpaceCenter is a nice (free) add-on extension.
- Prepolator is very worthwhile if you are working on fonts which you plan to interpolate.
- Skateboard is extremely helpful for planning & designing variable fonts.

You can get more-detailed documentation about RoboFont extensions at https://robofont.com/documentation/extensions/.

## Other useful tools:

- A really handy tool to create character sets: https://www.alphabet-type.com/tools/charset-builder/
- [FontGoggles](https://fontgoggles.org/) is a really good tool to quickly view fonts, useful to quickly test font builds. It can also be useful as a way to quickly compare how various fonts handle the design of certain characters, etc.

## General learning

- [Type Basics, by Underware](http://www.typeworkshop.com/index.php?id1=type-basics). Not a flashy layout, but a serious of extremely helpful drawings with important lessons for type design.
- [Type Mechanics, by Tobias Frere-Jones](https://frerejones.com/blog?tag=Education%20Mechanics). More useful explanations of some visual things that are important to know, but not always obvious.
- [Spacing](https://ohnotype.co/blog/spacing) & [Proofing](https://ohnotype.co/blog/proof-it) by James Edmonson (OHno Type) are two excellent, practical posts for subjects beyond shaping that are super significant to good type design. I also borrowed the first two suggestions from James’s post [Getting Started in Type Design](https://ohnotype.co/blog/getting-started).
- Books are good, too:
  - For the very basics of letter-shaping, the first book I read in type design was really helpful: [Designing Type, by Karen Cheng](https://yalebooks.yale.edu/book/9780300111507/designing-type). It goes through each letter, showing their general forms via classic typefaces.
  - For deeper reflections on theory, [The Theory of Type Design, by Gerard Unger](https://www.amazon.com/Theory-Type-Design-Gerard-Unger/dp/9462084408) is 

## Advanced topics

- **Version control:** Git is pretty challenging to get started with, but extremely useful for all areas of technical design & code. 
  - [Git for Humans](https://abookapart.com/products/git-for-humans) is a a great introduction to using Git. 
  - GitHub is the most popular Git website, and they also have a nice [getting-started guide](https://guides.github.com/introduction/git-handbook/).
- **Scripting:** scripting makes it possible to work efficiently with complex fonts, and not have to rely on someone else building everything for you. 
  - RoboFont has a good [guide to getting started](https://robofont.com/documentation/building-tools/), including a great guide to starting with Python, the most common scripting language used for font design & development (and many other things, like software development, data analysis, and more).
  - [DrawBot](https://www.drawbot.com/) makes it possible to create graphic designs & animations with Python. Not only is this a fun way to learn Python, but it can be a genuinely useful tool to generate proofs, books, or animations that (sometimes) would be impossible to create with more-general design tools
  - On the Glyphs side, they provide a very handy 4-part [Scripting Glyphs](https://glyphsapp.com/tutorials/scripting-glyphs-part-1) tutorial.
- **Mastering:** A topic as big as type design itself. Here are a few places you might get started.
  - [OpenType Cookbook](http://opentypecookbook.com/) is a friendly introduction to scripting OpenType features. It is very approacheable, and helps answer questions like “How can I add automatically-swapping alternates to a font?” and “How can I make ligatures work how I want?”
  - [The OpenType Spec](https://docs.microsoft.com/en-us/typography/opentype/spec/) answers basically every question about what is possible in fonts, such as “What are the possible [OpenType feature tags](https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags) and what do they mean?” and “What are the [valid values for font variation axes](https://docs.microsoft.com/en-us/typography/opentype/spec/dvaraxisreg)?”
  - [FontMake](https://github.com/googlefonts/fontmake/) is a great way to get started into building fonts in a way that gives you more control than tools like Batch can (you can even use shell scripting as a quick way to create handy workflows to build & sort fonts). 
  - [FontTools](https://fonttools.readthedocs.io/en/latest/) provides a bunch of Python-based tools to help handle font files – of note, TTX makes it easy to inspect built OTF/TTF font files, TTFont can make it efficient to edit font data, and 
