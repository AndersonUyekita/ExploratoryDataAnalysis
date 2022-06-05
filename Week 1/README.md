`Week 1` Exploratory Data Analysis
================

-   👨🏻‍💻 Author: Anderson H Uyekita
-   📚 Specialization: <a
    href="https://www.coursera.org/specializations/data-science-foundations-r"
    target="_blank" rel="noopener">Data Science: Foundations using R
    Specialization</a>
-   📖 Course:
    <a href="https://www.coursera.org/learn/exploratory-data-analysis"
    target="_blank" rel="noopener">Exploratory Data Analysis</a>
    -   🧑‍🏫 Instructor: Roger D Peng
-   📆 Week 1
    -   🚦 Start: Wednesday, 25 May 2022
    -   🏁 Finish: Wednesday, 25 May 2022

------------------------------------------------------------------------

#### Assignments & Deliverables

-   💻 Swirl
    -   Principles of Analytic Graphs
    -   Exploratory Graphs
    -   Graphics Devices in R
    -   Plotting Systems
    -   Base Plotting System
-   [📝 Quiz 1](./getting_and_cleaning_data_quiz_1.md)

------------------------------------------------------------------------

#### Slides

-   Lesson 1: Graphs <a href="" id="graphs"></a>
    -   [Principles of Analytic
        Graphics](./slides/1_1_1_PrinciplesofAnalyticGraphics.pdf)
    -   [Exploratory Graphs](./slides/1_1_2_ExploratoryGraphs.pdf)
-   Lesson 2: Plotting <a href="" id="plotting"></a>
    -   [Plotting Systems in
        R](./slides/1_2_1_Plotting%20Systems%20in%20R.pdf)
    -   [Base Plotting System](./slides/1_2_2_PlottingBase.pdf)
-   Lesson 3: Graphics Devices <a href="" id="graphics_devices"></a>
    -   [Graphics Devices in R](./slides/1_3_GraphicsDevicesinR.pdf)

------------------------------------------------------------------------

### Class Notes

#### [<kbd>Lesson 1</kbd>](#graphs) Principles of Analytic Graphics

**Summary**

-   Principle 1: Show comparisons

    > -   Evidence for a hypothesis is always relative to another
    >     competing hypothesis.
    > -   Always ask “Compared to What?”

-   Principle 2: Show causality, mechanism, explanation

    > -   What is your causal framework for thinking about a question?

-   Principle 3: Show multivariate data

    > -   Multivariate = more than 2 variables
    > -   The real world is multivariate
    > -   Need to “escape flatland”

-   Principle 4: Integrate multiple modes of evidence

    > -   Completely integrate words, numbers, images, diagrams
    > -   Data graphics should make use of many modes of data
    >     presentation
    > -   Don’t let the tool drive the analysis

-   Principle 5: Describe and document the evidence

    > -   A data graphic should tell a complete story that is credible

-   Principle 6: Content is king

    > -   Analytical presentations ultimately stand or fall depending on
    >     the quality, relevance, and integrity of their content

#### [<kbd>Lesson 1</kbd>](#graphs) Exploratory Graphs

> -   To understand data properties
> -   To find patterns in data
> -   To suggest modeling strategies
> -   To “debug” analyses
> -   To communicate results

The exploratory graphs are really about the **first four** things on
this list.

Characteristics of exploratory graphs:

> -   They are made quickly
> -   A large number are made
> -   The goal is for personal understanding
> -   Axes/legends are generally cleaned up (later)
> -   Color/size are primarily used for information

**Summary**

> -   Exploratory plots are “quick and dirty”
> -   Let you summarize the data (usually graphically) and highlight any
>     broad features
> -   Explore basic questions and hypotheses (and perhaps rule them out)
> -   Suggest modeling strategies for the “next step”

#### [<kbd>Lesson 2</kbd>](#plotting) Plotting Systems in R

**Summary**

There are three basic ways to plot a graph in R.

1.  Base Plotting System: “artist’s palette” model

    > -   Convenient, mirrors how we think of building plots and
    >     analyzing data
    > -   Can’t go back once plot has started (i.e. to adjust margins);
    >     need to plan in advance
    > -   Difficult to “translate” to others once a new plot has been
    >     created (no graphical “language”)
    > -   Plot is just a series of R commands

2.  Lattice: Entire plot specified by one function; conditioning

    > -   Plots are created with a single function call (xyplot, bwplot,
    >     etc.)
    > -   Most useful for conditioning types of plots: Looking at how y
    >     changes with x across levels of z
    > -   Things like margins/spacing set automatically because entire
    >     plot is specified at once
    > -   Good for putting many many plots on a screen
    > -   Sometimes awkward to specify an entire plot in a single
    >     function call
    > -   Annotation in plot is not especially intuitive
    > -   Use of panel functions and subscripts difficult to wield and
    >     requires intense preparation
    > -   Cannot “add” to the plot once it is created

3.  ggplot2: Mixes elements of Base and Lattice

    > -   Splits the difference between base and lattice in a number of
    >     ways
    > -   Automatically deals with spacings, text, titles but also
    >     allows you to annotate by “adding” to a plot
    > -   Superficial similarity to lattice but generally easier/more
    >     intuitive to use
    > -   Default mode makes many choices for you (but you can still
    >     customize to your heart’s desire)

#### [<kbd>Lesson 2</kbd>](#plotting) Base Plotting System

**Summary**

> -   Plots in the base plotting system are created by calling
>     successive R functions to “build up” a plot
> -   Plotting occurs in two stages:
>     -   Creation of a plot
>     -   Annotation of a plot (adding lines, points, text, legends)
> -   The base plotting system is very flexible and offers a high degree
>     of control over plotting

#### [<kbd>Lesson 3</kbd>](#graphics_devices) Graphics Devices in R

**Summary**

> -   Plots must be created on a graphics device
> -   The default graphics device is almost always the screen device,
>     which is most useful for exploratory analysis
> -   File devices are useful for creating plots that can be included in
>     other documents or sent to other people
> -   For file devices, there are vector and bitmap formats
>     -   Vector formats are good for line drawings and plots with solid
>         colors using a modest number of points
>     -   Bitmap formats are good for plots with a large number of
>         points, natural scenes or webbased plots
