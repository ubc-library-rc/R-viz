---
layout: default
title: Workshop content
nav_order: 5
has_children: true
has_toc: false
---
# Introduction to ggplot2

**ggplot2 is based on a *grammar of graphics*:**
"a tool that enables us to concisely describe the components of a graphic" [^1]

This allows us to build complex graphical representations of our data from consistent, essential building blocks. 

Once you understand the *logic* and *grammar* of ggplot, you can create almost any kind of plot you might need. 

The basic structure of ggplot code is as follows: 

```
  ggplot(aes(x, y), data) +     	#specifying your axes, data
  geom +				#indicating the type of plot, e.g scatter, line, etc. 
  additional geoms +   			#layering types of plots 
  thematic arguments  			#a number of arguments to modify theme/aesthetics
```

For example, 

this code: 

Input
{: .label .label-green }
```sh
$ ggplot(aes(x = Petal.Length, y = Sepal.Length), data = iris) +  #axes and data
$ geom_point() +  #plot type (point/scatter)
$  labs(x = 'Petal length (cm)',  #thematic arguments 
$       y = 'Sepal length (cm)', 
$       title = 'Petal length vs sepal length of irises')
```

creates this plot : 

Output
{: .label .label-yellow }

![](https://ubc-library-rc.github.io/R-viz/content/images/Rplot.png)

[^1]: Hadley Wickham. 2010. A Layered Grammar of Graphics. *Journal of Computational and Graphical Statistics* 19(1):3–28