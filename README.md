[![View SetFigPaper on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://www.mathworks.com/matlabcentral/fileexchange/75507-setfigpaper)
# SetFigPaper


<!-- MarkdownTOC autolink="true" levels="1,2" bracket="round" autoanchor="true" style="unordered" indent="\t" -->

- [Introduction](#introduction)
- [Examples](#examples)
	- [Grayscale](#grayscale)
	- [Interpreter](#interpreter)
	- [FontName](#fontname)
	- [FontSize](#fontsize)
	- [LineWidth](#linewidth)
- [Author](#author)

<!-- /MarkdownTOC -->


<a id="introduction"></a>
# Introduction
With this function it is possible to modify multiple style parameters of MATLAB graphic representations. It is only necessary to include the function call after the graphic representation code, that's all.

It can be used in two ways:

* Name-Value pair arguments: `setfigpaper('Width',[20,0.65],'Interpreter','Latex')`. Only the parameters you want to modify are necessary.
* Arguments only: `setfigpaper([20,0.65],10,'Helvetica','Latex')`. With explicit order: (Width,FontSize,FontName,Interpreter,Grayscale,LineWidth).

The available options are:

| Name        | Description         | 
| ------------- | ------------- |
| `Width`       | Simple: one integer. With aspect ratio: array with two elements, the width and the aspect ratio. |          
| `FontSize`    | The font size in all texts in the figure. |
| `FontName`    | Font family. |
| `Interpreter` | Text interpreter syntax, 'Latex', 'tex' or 'none'. If you don't want to modify the `interpreter` the value must be `[]` (empty value). |
| `Grayscale`   | Change all colours to grayscale. [boolean] |
| `LineWidth`   | Set line width only for axes, not for data. |
	
<a id="examples"></a>
# Examples
	
<a id="grayscale"></a>
## Grayscale

### Example 1
```matlab

setfigpaper('GrayScale',true)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Wind (https://www.mathworks.com/matlabcentral/fileexchange/35250-matlab-plot-gallery-wind), MATLAB Central File Exchange. Retrieved May 14, 2020.
	
| Original   | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot1a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot1b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('GrayScale',true)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Subplot (2) (https://www.mathworks.com/matlabcentral/fileexchange/35298-matlab-plot-gallery-subplot-2), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper         | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot2a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot2b.png" width="100%"></img>  |


<a id="interpreter"></a>
## Interpreter

### Example 1
```matlab

setfigpaper('Interpreter','Latex')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Heatmap Chart (https://www.mathworks.com/matlabcentral/fileexchange/63457-matlab-plot-gallery-heatmap-chart), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper         | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot3a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot3bb.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('Interpreter','Latex')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Line Plot 2D (2) (https://www.mathworks.com/matlabcentral/fileexchange/35256-matlab-plot-gallery-line-plot-2d-2), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper           | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot4a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot4b.png" width="100%"></img>  |

<a id="fontname"></a>
## FontName
* *Only work with 'Tex' interpreter*

### Example 1
```matlab

setfigpaper('FontName','Courier')

```

**Code:** https://www.mathworks.com/help/matlab/ref/wordcloud.html

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot3aa.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot3bc.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('FontName','Times New Roman')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Heatmap Chart (https://www.mathworks.com/matlabcentral/fileexchange/63457-matlab-plot-gallery-heatmap-chart), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot3a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot6b.png" width="100%"></img>  |

<a id="fontsize"></a>
## FontSize

### Example 1
```matlab

setfigpaper('FontSize',6)

```

**Code:** https://www.mathworks.com/help/matlab/ref/parallelplot.html

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot7a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot7b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('FontSize',15)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Directed Graph Plot (https://www.mathworks.com/matlabcentral/fileexchange/63456-matlab-plot-gallery-directed-graph-plot), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot8a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot8b.png" width="100%"></img>  |


<a id="linewidth"></a>
## LineWidth

### Example 1
```matlab

setfigpaper('LineWidth',2)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Set Axes Positions (https://www.mathworks.com/matlabcentral/fileexchange/63458-matlab-plot-gallery-set-axes-positions), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot9a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot9b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('LineWidth',1.5)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Scatter Plot 3D (https://www.mathworks.com/matlabcentral/fileexchange/35288-matlab-plot-gallery-scatter-plot-3d), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper           | 
|:-------------:|:-------------:|
| <img src="http://jmrplens.com/GitHub_setfigpaper/plot10a.png" width="100%"></img>      | <img src="http://jmrplens.com/GitHub_setfigpaper/plot10b.png" width="100%"></img>  |

<a id="author"></a>
# Author
Jose M. Requena Plens, 2020. (info@jmrplens.com   | joreple@upv.es)

Original concept: Noe Jimenez, 2014. (noe.jimenez@csic.es | nojigon@i3m.upv.es)



