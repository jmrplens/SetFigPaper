[![View SetFigPaper on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://www.mathworks.com/matlabcentral/fileexchange/75507-setfigpaper)    [![View SetFigPaper on Mathworks Blog](https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/matlab-pick-of-the-week-02.svg)](https://blogs.mathworks.com/pick/2020/05/17/changing-figure-settings/)    [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate?hosted_button_id=BLP3R6VGYJB4Q) [![Donate](https://img.shields.io/badge/Donate-Ko--fi-brightgreen?color=ff5f5f)](https://ko-fi.com/jmrplens) 

# SetFigPaper

- [Introduction](#introduction)
- [Examples](#examples)
	- [Grayscale](#grayscale)
	- [Interpreter](#interpreter)
	- [FontName](#fontname)
	- [FontSize](#fontsize)
	- [LineWidth](#linewidth)
- [Troubleshooting](#troubleshooting)
- [Incompatibility Issues](#incompatibility)
- [Author](#author)


<a id="introduction"></a>
# Introduction
With this function it is possible to modify multiple style parameters of MATLAB graphic representations. It is only necessary to include the function call after the graphic representation code, that's all.

It can be used in two ways:

* Name-Value pair arguments: `setfigpaper('Width',[20,0.65],'Interpreter','Latex')`. Only the parameters you want to modify are necessary.
* Only values: `setfigpaper([20,0.65],10,'Helvetica','Latex')`. With explicit order: (Width,FontSize,FontName,Interpreter,Grayscale,LineWidth,Figure).

The available options are:

| Name        | Description         | 
| ------------- | ------------- |
| `Width`       | Simple: one integer. With aspect ratio: array with two elements, the width and the aspect ratio. |          
| `FontSize`    | The font size in all texts in the figure. |
| `FontName`    | Font family. |
| `Interpreter` | Text interpreter syntax, 'Latex', 'tex' or 'none'. If you don't want to modify the `interpreter` the value must be `[]` (empty value). |
| `Grayscale`   | Change all colours to grayscale. [boolean] |
| `LineWidth`   | Set line width only for axes, not for data. |
| `Figure`      | Apply to a specific figure. |
	
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
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot1a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot1b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('GrayScale',true)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Subplot (2) (https://www.mathworks.com/matlabcentral/fileexchange/35298-matlab-plot-gallery-subplot-2), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper         | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot2a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot2bb.png" width="100%"></img>  |


<a id="interpreter"></a>
## Interpreter

### Example 1
```matlab

setfigpaper('Interpreter','Latex')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Heatmap Chart (https://www.mathworks.com/matlabcentral/fileexchange/63457-matlab-plot-gallery-heatmap-chart), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper         | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot3a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot3bb.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('Interpreter','Latex')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Line Plot 2D (2) (https://www.mathworks.com/matlabcentral/fileexchange/35256-matlab-plot-gallery-line-plot-2d-2), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper           | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot4a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot4b.png" width="100%"></img>  |

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
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot3aa.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot3bc.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('FontName','Times New Roman')

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Heatmap Chart (https://www.mathworks.com/matlabcentral/fileexchange/63457-matlab-plot-gallery-heatmap-chart), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot3a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot6b.png" width="100%"></img>  |

<a id="fontsize"></a>
## FontSize

### Example 1
```matlab

setfigpaper('FontSize',6)

```

**Code:** https://www.mathworks.com/help/matlab/ref/parallelplot.html

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot7a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot7b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('FontSize',15)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Directed Graph Plot (https://www.mathworks.com/matlabcentral/fileexchange/63456-matlab-plot-gallery-directed-graph-plot), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot8a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot8b.png" width="100%"></img>  |


<a id="linewidth"></a>
## LineWidth

### Example 1
```matlab

setfigpaper('LineWidth',2)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Set Axes Positions (https://www.mathworks.com/matlabcentral/fileexchange/63458-matlab-plot-gallery-set-axes-positions), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper          | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot9a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot9b.png" width="100%"></img>  |

### Example 2
```matlab

setfigpaper('LineWidth',1.5)

```

**Code:** MathWorks Plot Gallery Team (2020). MATLAB Plot Gallery - Scatter Plot 3D (https://www.mathworks.com/matlabcentral/fileexchange/35288-matlab-plot-gallery-scatter-plot-3d), MATLAB Central File Exchange. Retrieved May 14, 2020.

| Original        | setfigpaper           | 
|:-------------:|:-------------:|
| <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot10a.png" width="100%"></img>      | <img src="https://github.com/jmrplens/SetFigPaper/blob/1717319927eddc12c527af971479c0d064716db3/.github/images/plot10b.png" width="100%"></img>  |


<a id="troubleshooting"></a>
# Troubleshooting
In some representations, it is necessary to carry out previous steps for the function to work correctly.

* **pie and pie3**: If you use **LaTeX** interpreter with default labels (percentage) you need to fix the plot before call setfigpaper. Solution:
	```matlab 
	p = pie([1 3 0.5 2.5 2]);
	txt = findobj(p,'Type','Text');
	arrayfun(@(x) set(x,'String',strrep(x.String,'%','\%')),txt,...
	'UniformOutput',false)
	setfigpaper
	```

* **pareto**: If you use **LaTeX** interpreter with default ticklabels (percentage) you need to fix the plot before call setfigpaper. Solution:
	```matlab 
	[H,ax]  = pareto([200 120 555 608], {'Fred','Ginger','Norman','Max'});
	ax(2).YTickLabel = arrayfun(@(x) strrep(x,'%','\%'),ax(2).YTickLabel);
	setfigpaper
	```

<a id="incompatibility"></a>
# Incompatibility Issues

*Setfigpaper* is developed in MATLAB 2020. In some versions not all options are available. The function checks the version so that the incompatible code is not executed.

*If you find any error or the modification does not apply to any item, please inform me and I will try to solve it.*

**Legend meaning:**
* ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) Fixed by version checking.
* ![#efb810](https://via.placeholder.com/15/efb810/000000?text=+) It runs but doesn't affect.


### MATLAB 2018b (9.5) and earlier

| &nbsp;&nbsp; | Axes/Object | Description | Line code |
| ------ | ------ | ------ | ------ |
| ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) | **Heatmap** | Unable to assign an interpreter to text within the map. | ` set(ax.Heatmap,'Interpreter',type); ` |
| ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) | **GraphPlot** | Cannot modify node font. | `set(grap,'nodefontname',...` |
| ![#efb810](https://via.placeholder.com/15/efb810/000000?text=+) | **Polar Axes** | Grayscale cannot be applied to all elements. |  |

<a id="author"></a>
# Author
Jose M. Requena Plens, 2020. (info@jmrplens.com   | joreple@upv.es)

Original concept: Noe Jimenez, 2014. (noe.jimenez@csic.es | nojigon@i3m.upv.es)

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate?hosted_button_id=BLP3R6VGYJB4Q)
[![Donate](https://img.shields.io/badge/Donate-Ko--fi-brightgreen?color=ff5f5f)](https://ko-fi.com/jmrplens) 

