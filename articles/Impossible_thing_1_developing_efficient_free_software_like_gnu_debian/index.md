---
nid: '2771'
title: 'Impossible thing #1: Debian GNU/Linux'
authors: 'Terry Hancock'
published: '2008-01-24 4:03:01'
tags: 'free-software,gnu/linux,windows,economics,metrics'
license: verbatim_only
listed: 'true'
book: making_the_impossible_happen_the_rules_of_free_culture
book_weight: '-1'
layout: book.html

---
<!--Impossible Thing #1: Debian GNU/Linux -->

With any paradigm shift, it is difficult to see the new world from the old one, even though it is glaringly obvious once you've crossed over. Empirical evidence is one way to bridge the gap. Let's look at some solid evidence for the success of what is probably the most obvious "impossible" achievement of commons-based peer production: **free software**, as exemplified by the Debian GNU/Linux distribution.

<!--break-->

First, of course, we need to start with the myth, promulgated by a couple of decades of proprietary software dominance with an economic model founded an the manufacturing analogy:

=TEXTBOX_START=Myth #1=
# "Free software development can create simple programs and utilities, but it's useless for anything large scale"

This may seem almost comic in the pages of Free Software Magazine, but I *still* hear this myth spouted by otherwise intelligent people in other communities. It's such a strongly held belief because it is all that conventional wisdom allows for works created by "amateurs" in their "spare time". The professionalist belief is that only paid professionals can produce quality, well-engineered designs and that professionals cannot possibly be paid to work on something you can get "for free".
=TEXTBOX_END=

# How Big is "Big"?

It's difficult for people to compare the scale of free and proprietary products with each other. First of all, it's tempting to say that software is "worth what you charge"—that is to say, that you could evaluate it by its sale price. In that case, proprietary software is a multi-billion dollar industry, so how can you even compare it to the free-licensed software industry which doesn't charge per-copy costs?

=ZOOM=We don't value software for software's sake. We value using it to do stuff=

However, we don't value software for software's sake. We value using it to do stuff. Thus, _use value_ is the relevant metric, not sale value. Unfortunately, that too is hard to count, though you can look at the figures for how many people are using free software.

But there is another way to ask the question: if you had to start from scratch and re-build the existing body of software, using a proprietary development company, how much would it cost you? At the very least, free software must be worth the effort that people are putting into it (or they'd stop working on it). So, how much is that?

Measuring the size of "free software" is not easy. First of all, you have a hard time finding it all. Then there's deciding what is worth counting and what is just cruft. Fortunately, this has largely already been done for us—in the form of Debian GNU/Linux, the world's most complete free software GNU/Linux distribution.

There is a project being conducted by the LibreSoft Research Group[1] to collect and analyze metrics data for free software projects based on "source lines of code" (**SLOC**), a relatively easy-to-measure statistic for any kind of software. These data are generated by David Wheeler's SLOCCount[2] program, which uses COCOMO[3], a long-standing and fairly simple model, to estimate the costs of software projects under the assumptions of centralized, managed software development. Now this is probably not an accurate measure of the _actual_ effort cost of developing free software (although I leave it as an exercise for the reader to guess whether it's too high or too low), but it does provide an order-of-magnitude estimation and a consistent metric which allows for comparisons. Figure 1.1 shows the results of this estimation, showing the growth of the distribution with each release.

=IMAGE=c20080123_cost-deb-bar.jpg=Figure 1.1: Equivalent cost of producing Debian GNU/Linux if it were to be developed in a conventional centrally-managed development setting. This can be regarded as an approximate lower bound for its "use value" (because the community had to want it that much to spend that much effort on it).=

Now these are very large numbers. It's easy to lose perspective. So let's throw in some comparable project costs to give an idea of the scale of project we are talking about (Figure 1.2).

=IMAGE=c20080123_cost-debian-spaceshuttle.jpg=Figure 1.2: For scale comparison, here are the costs of Debian (as well as GNU and Linux, considered separately), along with the actual reported costs of NASA space mission development projects (these do not include extended operations costs and the cost for the Space Shuttle is only from initial design to the 1981 maiden flight of Columbia).=

Yes, that's right. The estimated equivalent cost of developing Debian 4.0 "Etch" is not quite _three-quarters_ of the actual development cost of the _Space Shuttle_[4]. And that's in _adjusted_ dollars[5] (inflation has been applied to these numbers to make for a fair comparison, otherwise Etch would seem much more expensive than the Shuttle). If that doesn't convince you that free software projects can be large and complex, I don't know what would.

=ZOOM=The estimated equivalent cost of developing Debian 4.0 "Etch" is not quite three-quarters of the actual development cost of the Space Shuttle=

# But is it Better?

>"Measuring programming progress by lines of code is like measuring aircraft building progress by weight." —— _Bill Gates_

The large size of free software projects _could_ simply be due to inefficiency. After all, both Microsoft Windows and Mac OS X have been criticized on these grounds as being "bloated". However, comparing the size of Microsoft Windows to the entire Debian GNU/Linux distribution is like comparing an apple to an entire orchard: Debian is not an "operating system", it's a complete collection of software. The equivalent in the proprietary world would be something like "the entire software inventory of CompUSA".

So, to make things comparable, let's strip down the Debian numbers so that we only include the things that provide equivalent function to what comes out of the box with, say, Microsoft Windows "Vista" (estimated at 50 million SLOC). So, we'll need what _computer scientists_ (as opposed to marketing executives) call the "operating system"—which includes the Linux kernel, the GNU libraries, and the GNU utilities (_not_ the entire GNU project, which today is dominated by application software packages like Gimp). Then we'll also need the graphical windowing environment, which means the X server packages, and—since Microsoft continues to bundle it—the web browser, which is from the Mozilla project. Microsoft Office is not bundled with Windows, so we'll leave out OpenOffice.org.

This allows us to compare "equivalent stacks" of software:

=IMAGE=c20080123_comparable-stacks.jpg=Figure 1.3: The free software stack providing the same functionality as Microsoft Windows does "out of the box".  The left side compares by source lines of code, while the right compares COCOMO-estimated cost (based on the assumption that the free software projects are developed as independent projects and Windows is developed as one unit).=

Not only is the free software stack less than half the size of Windows, but, because it is factored into distinct packages, it is easier to maintain. It could be that the need to divide the work among independent projects forces engineering discipline to be followed, and it is apparent that this pays off in the long run in more compact code (it's also interesting to note that this Debian source code also supports _eleven_ binary builds for different CPU architectures, while Windows only supports one).

=ZOOM=The need to divide the work among independent projects forces engineering discipline to be followed=

So, not only does free software represent a vast amount of effort, but it is apparently very well-engineered and efficient effort leading to an even higher use value than equivalent proprietary products! Not only _can_ free software manage large, complex projects, but it appears to do it _better_ than proprietary methods.


# Notes

[1] [LibreSoft Research Group: Debian Counting](http://libresoft.es/debian-counting). The published numbers include the overall totals and the results for each Debian source package. I have grouped packages using dependency rules and string-searches (taking advantage of Debian's package naming conventions) in order to produce the aggregates used in the Windows comparison as well as the divisions in the bar charts.

[2] [SLOCCount (Software Package)](http://www.dwheeler.com/sloccount/). Program used by the Debian Counting project to generate their results.

[3] [COnstructive COst MOdel](http://en.wikipedia.org/wiki/COCOMO). Used by the SLOCCount program.

[4] [Space Shuttle Program Cost]() Testimony of Mr. Robert F. Thompson, taken from the Columbia Accident Investigation Board public hearing on Wednesday, April 23, 2003. Places the cost of the Shuttle at an estimated $5.15 billion in 1971 dollars or an actual $8.5 billion in 1981 dollars.

[5] [Measuring Worth](http://www.measuringworth.com/uscompare). Online source and calculator, demonstrating six different deflation formulae used to compare different kinds of cost over time. The one most appropriate for large government projects is the "GDP Deflator", which is what I used here to adjust space project costs. All of the cost numbers have been converted to year 2000 dollars for comparison purposes.


# Terms

**free software**: In this book, the expression "free software" is always used in the jargon sense of "software offered under a free license" as described in the Free Software Foundation's ["Free Software Definition"](http://www.fsf.org/licensing/essays/free-sw.html). This is a somewhat unfortunate choice of jargon, as it is frequently misunderstood, but it is generally the preferred term used _within_ the free software development community. For most practical purposes, the term is synonymous with "open source software".

**SLOC**: [Source Lines Of Code](http://en.wikipedia.org/wiki/Source_lines_of_code) are used as a metric of the size and complexity of a software package, and can, in bulk, be used to estimate the effort required to create it. It obviously can be inaccurate in specific cases, but is a good objective metric which is easy to measure.

