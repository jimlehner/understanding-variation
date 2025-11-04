# Understanding Variation - The key to managing the chaos of manufacturing
This project serves as a repository for code, tables, tools, and examples that support the **Understanding Variation** effort piece of **The Broken Quality Initiative** [www.brokenquality.com](https://www.brokenquality.com/). The aim of this effort is to provide resources to those who are looking to further their understanding of variation both mathematically and practically.

## Table of Contents

1. [Projects](#projects)
2. [Bias Correction Factor Table](#bias-correction-factor-table)
3. [Scaling Factor Tables](#scaling-factor-tables)
3. [How to use this repository](#how-to-use-this-repository)
4. [Filing bigs](#filing-bugs)
5. [Contributing](#contributing)
6. [About Understanding Variation](#about-understanding-variation)
7. [Contact](#contact)

## Projects
- **Monte Carlo simulation of the bias correction factor (d2 & d3)**: Coming soon!
- **Manufacturing polygons vision system**: Coming soon!

## Bias Correction Factor Table
This table contains the values for the factors that convert the average ranges and median ranges into the appropriate measures of dispersion, namely, either *Sigma(X)*, *Sigma($\overline{X}$)*, or *Sigma(R)*. For details on how these values are calculated see [Monte Carlo simulation for determining bias correction factors](https://github.com/jimlehner/understanding-variation/projects).

## Scaling Factor Tables
There are two scaling factors tables: *average-range-chart-scaling-factors-using-average-range.csv* and *average-range-chart-scaling-factors-using-median-range.csv*. These tables should be used to determine the value of the respective scaling factors based on subgroup size.

### Scaling factors for Average and Range chart using the average range, $ \overline{R} $
Given *k* subgroups each with *n* observations with grand average, and average range, use the tabled constants in *average-range-chart-scaling-factors-using-average-range.csv*.

Limits for subgroup averages for an Average and Range chart using the **average range** are obtained from:

$$ \text{UAL}_{\overline{X}} = \overline{\overline{\text{X}}} + A_2 \cdot \overline{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{\overline{X}} $$
$$ \text{LAL}_{\overline{X}} = \overline{\overline{\text{X}}} - A_2 \cdot \overline{\text{R}} $$

Limits for subgroup ranges for an Average and Range chart using the **average range** are obtained using the formulas:

$$ \text{URL}_{R} = D_4 \cdot \overline{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{R} $$
$$ \text{LRL}_{R} = D_3 \cdot \overline{\text{R}} $$

Natural process limits for individual values may be obtained using the formulas:

$$ \text{UPL}_{X} = \overline{\overline{\text{X}}} + E_2 \cdot \overline{\text{R}} $$
$$ \text{CL}_{X} = \overline{\overline{X}} $$
$$ \text{LPL}_{X} = \overline{\overline{\text{X}}} - E_2 \cdot \overline{\text{R}} $$

The formulas for the scaling factors in *average-range-chart-scaling-factors-using-average-range.csv* are:

$$ \text{A}_{2} = \frac{3}{d_2 \sqrt{n}} $$
$$ \text{D}_{3} = 1 - (\frac{3\cdot\text{d}_3}{d_2}) $$
$$ \text{D}_{4} = 1 + (\frac{3\cdot\text{d}_3}{d_2}) $$
$$ \text{E}_{2} = \frac{3}{d_{2}} $$

### Scaling factors for Average and Range chart using the median range, $ \tilde{R} $
Given *k* subgroups each with *n* observations with grand average, and average range, use the tabled constants in *average-range-chart-scaling-factors-using-median-range.csv*.

Limits for subgroup averages for an Average and Range chart using the **median range** are obtained from:

$$ \text{UAL}_{\overline{X}} = \overline{\overline{\text{X}}} + A_4 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{\overline{X}} $$
$$ \text{LAL}_{\overline{X}} = \overline{\overline{\text{X}}} - A_4 \cdot \tilde{\text{R}} $$

Limits for subgroup ranges for an Average and Range chart using the **median range** are obtained using the formulas:

$$ \text{URL}_{R} = D_6 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{R} = \tilde{R} $$
$$ \text{LRL}_{R} = D_5 \cdot \tilde{\text{R}} $$

Natural process limits for individual values may be obtained using the formulas:

$$ \text{UPL}_{X} = \overline{\overline{\text{X}}} + E_5 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{X} = \overline{\overline{X}} $$
$$ \text{LPL}_{X} = \overline{\overline{\text{X}}} - E_5 \cdot \tilde{\text{R}} $$

The formulas for the scaling factors in *average-range-chart-scaling-factors-using-median-range.csv* are:

$$ \text{A}_{4} = \frac{3}{d_2 \sqrt{n}} $$
$$ \text{D}_{5} = 1 - \frac{d_{2} - 3\text{d}_3}{d_4} $$
$$ \text{D}_{6} = \frac{d_{2} - 3\text{d}_3}{d_4} $$
$$ \text{E}_{5} = \frac{3}{d_{4}} $$

## How to use this repository
Inside this repository you'll tables, code, and examples on topics related to the theory of understanding variation. find the datasets and code associated with the essays found on [](https://www.brokenquality.com/bookshelf). As outlined above, the datasets associated with each essay can be found in the [data folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/data) and are labeled in accordance with the naming convention `essay_name-dataset_name`. The code for each essay, found in the [code folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/code), is labeled in accordance with the naming convetion **essay_name_code**.

## Filing Bugs
Although we strive to realize it, we know perfection is difficult to attain. If you encounter any issues or errors in the book or code samples, please don't hesitate to file a bug in the [Issues](https://github.com/jimlehner/broken-quality-initiative/issues) section of this repository. When filing an issue please include as much detail as possible including the chapter, page, number, descirption of the issue, and, if relevant, a screenshot or code snippet.

## Contributing
Contributions from our readers are welcomed and appreciated. If you've discovered an error or a way to improve the code, feel free to create a pull request. For signficant changes, please open an issue first to discuss the proposed changes. 

## About Understanding Variation
**Understanding Variation** is a project of **The Broken Quality Inititiave**. The aim of this project is to reveal the mathematical underpinnings of process behavior charts in support of the broader effort to make manufacturing a science and quality a discipline. This is being achieved by building on the work of Walter Shewhart (the father of the process behavior chart (control chart)) and the quality control expert, Donald J. Wheeler. 

To learn more about The Broken Quality Initiative visit [BrokenQuality.com](https://www.BrokenQuality.com/bookshelf).

## Contact
If you have questions or would like to collaborate email **James.Lehner@gmail.com** or **qualityisbroken@gmail.com**.
