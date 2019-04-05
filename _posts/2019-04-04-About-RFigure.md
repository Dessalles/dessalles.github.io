---
layout: post
title:  "About RFigure"
---

For several years (started in 2013), I've developed the software [**RFigure**](https://github.com/grumpfou/RFigure). The idea at that time was to give an interface on Matplotlib that is inspired by Matlab figures: the idea is to create a container that separate the data that are to be plotted, and the instructions (in Matplotlib) needed to create the file.

As a scientist, my workflow was to produce data through long simulations, save them in a particular format (like a **.csv** file), then create a script in Python that will plot these data. Then through the long process of formatting articles, I updated this script to change colors, labels, titles, log-scale, etc.

I appears to me that this predure tends to be cumbersome:
* At the end, we have one of several files containing the data (especially we want to plot information of different size, like the results of simulations with thousands of points versus the experimental results with a dozen of points)
* The data and the instructions are in separated files even if their are linked .
* Need to work with a console to execute the instruction script file.
* I need to handle the different formats of the data to plot: is the  CSV is representing a 2D array where each row would be represented a one line, or is it representing and image?
* The CSV do not a natural way to python types: dictionaries, booleans, strings, etc.
* The difficulty to have commentaries associated to the figures that would help the user to remember what the figure is displaying.

**RFigure** gathers in a same file both the data and the instructions. The data can be of any basic types of Python (list, dict, strings float, int, Numpy arrays). Once the container is opened. The user can then open the **rfig** file and with a graphical interface and rapidly change the instructions. Then they can export the new file in pdf/eps/png directly. There is also the possibility to add some comments associated to the file to describe the figure.

![Example of the interface of RFigure](https://raw.githubusercontent.com/grumpfou/RFigure/master/ExampleGui.png)

After beeing a personnal tool, I tried for the last month to make it available for the community by putting it on Github ([code source](https://github.com/grumpfou/RFigure)). and I have also developed several IPython magics functions that directly handle RFigures via the Jupyter notebook interface.
