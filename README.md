[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0) 

<span>![<span>Logo</span>](images/Logo.png)</span> 

**Open** **R**esidual **S**tress - a Python application for comparing and tabulating residual stress measurements from multiple sources, ranging from predictive finite element analyses, as well as experimental techniques.

# Functionality
This application seeks to ameliorate the current status quo for visualising residual stress fields in engineering components requiring a commercial finite element analysis package. In the same manner as computer aided design (CAD) employs interchange formats, such that component geometries can be shared between various commercial packages, there too is a need for the ability to share stress fields in these components with various stakeholders in the field of residual stress quantification.

The [Visualisation ToolKit (VTK)](http://www.vtk.org/overview/) is a powerful tool which has been leveraged for this purpose. Indeed, the free and open source FEA post processor [ParaView](https://www.paraview.org/) can be employed, and the present application makes use of VTK data structures, and extensions to navigate, interpolate and extrapolate residual stress predictions and measurements.

Primarily comprising a simplified viewer which allows a user to conduct arbitrary traces of scalar representation of stress fields in components, this repository is also populated with a series of case studies which exemplify how stresses can develop in components, and identify where further measurements need to be carried out.

# Overview
At the current stage of development, the application comprises a model viewer and the prototype of a diffraction volume viewer, existing as tabs in the main application. The main application can be launched at the command line with:

~~~
python -m OpenRS.main
~~~
This will run the OpenRS application as a script directly from the command line, with the two following sub-applications:
* [Model viewer](doc/model.md)
* [Point selector](doc/point_selector.md)

# Examples
Representative examples to be employed with the model viewer and how to generate them are available [here.](doc/examples.md)

# Installation
Python package dependencies are available through PyPI by running the following at the command line:
~~~
pip install OpenRS
~~~
If it is desired to generate finite element models, then it is recommended that either Dassault Systèmes' ABAQUS is available, with limited support for CalculiX. For more information on CalculiX, see http://www.dhondt.de/

Note that scripts for generating the examples are not included as part of the PyPI installer. These can be either copied from `OpenRS\examples` or from a cloned repository.
