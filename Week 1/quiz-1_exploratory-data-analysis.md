`Quiz 1` Exploratory Data Analysis
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
-   🌎 Rpubs: [Interactive
    Document](https://rpubs.com/AndersonUyekita/quiz-1_exploratory-data-analysis)

------------------------------------------------------------------------

## Question 1

Which of the following is a principle of analytic graphics?

-   [ ] Don’t plot more than two variables at at time
-   [x] Show multivariate data
-   [ ] Show box plots (univariate summaries)
-   [ ] Make judicious use of color in your scatterplots
-   [ ] Only do what your tools allow you to do

> According to six principles stated during the video
> <a href="./slides/1_1_1_PrinciplesofAnalyticGraphics.pdf"
> target="_blank" rel="noopener">Principles of Analytic Graphics</a>:
>
> -   Principle 1: Show comparisons
> -   Principle 2: Show causality, mechanism, explanation
> -   **Principle 3: Show multivariate data**
> -   Principle 4: Integrate multiple modes of evidence
> -   Principle 5: Describe and document the evidence
> -   Principle 6: Content is king

## Question 2

What is the role of exploratory graphs in data analysis?

-   [ ] Axes, legends, and other details are clean and exactly detailed.
-   [x] They are typically made very quickly.
-   [ ] They are made for formal presentations.
-   [ ] Only a few are constructed.

> According to the Summary of
> <a href="./slides/1_1_2_ExploratoryGraphs.pdf" target="_blank"
> rel="noopener">Exploratory Graphs</a> document.
>
> -   **Exploratory plots are “quick and dirty”**
> -   Let you summarize the data (usually graphically) and highlight any
>     broad features
> -   Explore basic questions and hypotheses (and perhaps rule them out)
> -   Suggest modeling strategies for the “next step”

## Question 3

Which of the following is true about the base plotting system?

-   [x] Plots are created and annotated with separate functions
-   [ ] Margins and spacings are adjusted automatically depending on the
    type of plot and the data
-   [ ] Plots are typically created with a single function call
-   [ ] The system is most useful for conditioning plots

> According to the Summary of
> <a href="./slides/1_2_2_PlottingBase.pdf" target="_blank"
> rel="noopener">The Base Plotting System</a> in R document.
>
> -   Plots in the base plotting system are created by calling
>     successive R functions to “build up” a plot
> -   **Plotting occurs in two stages:**
>     -   **Creation of a plot**
>     -   **Annotation of a plot (adding lines, points, text, legends)**
> -   The base plotting system is very flexible and offers a high degree
>     of control over plotting

## Question 4

Which of the following is an example of a valid graphics device in R?

-   [ ] The keyboard
-   [ ] A socket connection
-   [ ] A Microsoft Word document
-   [ ] A file folder
-   [x] A PNG file

> Based on slides 6 and 7 from
> <a href="./slides/1_3_GraphicsDevicesinR.pdf" target="_blank"
> rel="noopener">Graphics Devices in R</a> document.
>
> -   Vector formats: `pdf`, `svg`, `win.metafile`, and `postscript`,
>     and;
> -   Bitmap formats: `png`, `jpeg`, `tiff`, and `bmp`.

## Question 5

Which of the following is an example of a vector graphics device in R?

-   [x] Postscript
-   [ ] TIFF
-   [ ] JPEG
-   [ ] GIF
-   [ ] PNG

> Based on slide 6 from
> <a href="./slides/1_3_GraphicsDevicesinR.pdf" target="_blank"
> rel="noopener">Graphics Devices in R</a> document.
>
> -   Vector formats: `pdf`, `svg`, `win.metafile`, and `postscript`,
>     and;

## Question 6

Bitmapped file formats can be most useful for

-   [x] Scatterplots with many many points
-   [ ] Plots that are not scaled to a specific resolution
-   [ ] Plots that require animation or interactivity
-   [ ] Plots that may need to be resized

> According to the Summary of
> <a href="./slides/1_3_GraphicsDevicesinR.pdf" target="_blank"
> rel="noopener">Graphics Devices in R</a> in R document.
>
> -   Plots must be created on a graphics device
> -   The default graphics device is almost always the screen device,
>     which is most useful for exploratory analysis
> -   File devices are useful for creating plots that can be included in
>     other documents or sent to other people
> -   For file devices, there are vector and bitmap formats
>     -   Vector formats are good for line drawings and plots with solid
>         colors using a modest number of points
>     -   **Bitmap formats are good for plots with a large number of
>         points, natural scenes or webbased plots**

## Question 7

Which of the following functions is typically used to add elements to a
plot in the base graphics system?

-   [x] text()
-   [ ] plot()
-   [ ] boxplot()
-   [ ] hist()

> Based on slide 13 from
> <a href="./slides/1_2_2_PlottingBase.pdf" target="_blank"
> rel="noopener">The Base Plotting System in R</a> document.
>
> -   plot: make a scatterplot, or other type of plot depending on the
>     class of the object being plotted
> -   lines: add lines to a plot, given a vector x values and a
>     corresponding vector of y values (or a 2-
> -   column matrix); this function just connects the dots
> -   points: add points to a plot
> -   **text: add text labels to a plot using specified x, y
>     coordinates**
> -   title: add annotations to x, y axis labels, title, subtitle, outer
>     margin
> -   mtext: add arbitrary text to the margins (inner or outer) of the
>     plot
> -   axis: adding axis ticks/labels

## Question 8

Which function opens the screen graphics device for the Mac?

-   [x] quartz()
-   [ ] png()
-   [ ] bitmap()
-   [ ] pdf()

> Based on slide 2 from
> <a href="./slides/1_3_GraphicsDevicesinR.pdf" target="_blank"
> rel="noopener">Graphics Devices in R</a> document.
>
> -   A graphics device is something where you can make a plot appear
>     -   A window on your computer (screen device)
>     -   A PDF file (file device)
>     -   A PNG or JPEG file (file device)
>     -   A scalable vector graphics (SVG) file (file device)
> -   When you make a plot in R, it has to be “sent” to a specific
>     graphics device
> -   The most common place for a plot to be “sent” is the screen device
>     -   **On a Mac the screen device is launched with the quartz()**
>     -   On Windows the screen device is launched with windows()
>     -   On Unix/Linux the screen device is launched with x11()

## Question 9

What does the ‘pch’ option to par() control?

-   [ ] the orientation of the axis labels on the plot
-   [ ] the size of the plotting symbol in a scatterplot
-   [x] the plotting symbol/character in the base graphics system
-   [ ] the line width in the base graphics system

> Based on slide 9 from
> <a href="./slides/1_2_2_PlottingBase.pdf" target="_blank"
> rel="noopener">The Base Plotting System in R</a> document.
>
> -   **pch: the plotting symbol (default is open circle)**
> -   lty: the line type (default is solid line), can be dashed, dotted,
>     etc.
> -   lwd: the line width, specified as an integer multiple
> -   col: the plotting color, specified as a number, string, or hex
>     code; the colors() function gives
> -   you a vector of colors by name
> -   xlab: character string for the x-axis label
> -   ylab: character string for the y-axis label

## Question 10

If I want to save a plot to a PDF file, which of the following is a
correct way of doing that?

-   [ ] Construct the plot on the PNG device with png(), then copy it to
    a PDF with dev.copy2pdf().
-   [x] Construct the plot on the screen device and then copy it to a
    PDF file with dev.copy2pdf()
-   [ ] Open the screen device with quartz(), construct the plot, and
    then close the device with dev.off().
-   [ ] Open the PostScript device with postscript(), construct the
    plot, then close the device with dev.off().

> Based on slide 9 from
> <a href="./slides/1_3_GraphicsDevicesinR.pdf" target="_blank"
> rel="noopener">Graphics Devices in R</a> document.
>
> Copying a plot to another device can be useful because some plots
> require a lot of code and it can be a pain to type all that in again
> for a different device.
>
> -   dev.copy: copy a plot from one device to another
> -   **dev.copy2pdf: specifically copy a plot to a PDF file**
