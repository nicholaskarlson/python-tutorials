# Python Tutorials

This set of tutorials goes through basic to intermediate concepts of the Python Programming Language using the markdown and notebook aspects of the JupyterLab IDE. For illustration variables are explored using the Variable Explorer of the Spyder IDE as JupyterLab unfortunately falls behind in this area. The tutorials themselves are written in markdown, and therefore can be downloaded as a zip file, extracted and opened in JupyterLab if GitHub doesn't render images or equations correctly.

Please star the tutorials on GitHub and share with friends if you have found them useful.

## Installation

The Python ecosystem is very large and has multiple package managers for third-party libraries and numerous IDEs available for writing Python code. Installation is normally skimmed over briefly in other tutorials however configuring a Python environment using Mambaforge and the mamba package manager can be a good introduction to the Python programming language itself. Covering the basics of a package manager and examining what is going on behind the scenes in the file explorer early on will help later when configuring/troubleshooting custom Python environments and trying to install third-party packages which otherwise can be problematic for begineers. This tutorial also explains how to use Python from the Terminal, the IDLE IDE, the Spyder IDE, the JupyterLab IDE and the Visual Code IDE:

[Mambaforge Installation](https://github.com/PhilipYip1988/python-tutorials/blob/main/001_install/readme.md)

## Markdown

The JupyterLab IDE has the ability to write formatted notes in a Markdown file. This tutorial will cover the basics of Markdown syntax. All of these tutorials are written using this basic Markdown syntax. An Interactive Python Notebook File has Markdown cells and Code cells allowing one to create a detailed notebook to run Python Code from:

[Markdown Tutorial](https://github.com/PhilipYip1988/python-tutorials/blob/main/002_markdown/readme.md)

## Terminal

When running Python code from the Terminal, two progra	mming languages are used. In Linux and Mac there is the inbuilt programming language bash and in Windows there is PowerShell which closely resembles bash. The bash programming language is optimised for basic file operations within the operating system and is commonly used in conjunction with Python. bash however uses a different programming syntax to Python and this tutorial will cover basic file operating systems using bash. Familarity with bash before delving into Python will prevent later confusion when using the terminal with Python commands:

[Terminal Commands](https://github.com/PhilipYip1988/python-tutorials/blob/main/003_terminal/readme.md)

## Fundamental Data Types

There are 3 fundamental text data types, the unicode string, the bytes string and the bytearray. The Unicode string is the most widely used text data type in Python, however it is useful to know about the other two data types and establish a concept behind encoding:

[Text Data Types: str, bytes, bytearray](https://github.com/PhilipYip1988/python-tutorials/tree/main/004_text_datatypes/readme.md)

There are 6 fundamental numeric datatypes used in Python. The ```int``` class (whole number), ```bool``` class (```True``` or ```False```), the ```float``` class (number with a decimal point), the ```complex``` class (number with imaginary component $j=\sqrt{-1}$), the ```float``` class (number displayed with a decimal point but encoded in binary), ```Decimal``` class (higher accuracy number with decimal point encoded in decimal) and the ```Fraction``` class:

[Numeric Data Types: int, bool, float, complex, Decimal, Fraction](https://github.com/PhilipYip1988/python-tutorials/blob/main/005_numeric_datatypes/readme.md)

## Collections

Python has four collections the immutable tuple, which can be conceptualised as an archive of references. The mutable list, which can be conceptualised as being active current working directory of references. The set which can be conceptualised as a collection of unique references. And the dictionary which can be conceptualised as a mapping of immutable keys to values:

[Collections; tuple, list, set, dict](https://github.com/PhilipYip1988/python-tutorials/blob/main/006_collections/readme.md)

## Programming Constructs

Indentation and spacing is very important in Python and code is often grouped into a code block. Code blocks are used to direct code in response to a condition, to repeat an operation multiple times, to error handle and to create custom functions:

[Programming Constructs using Code Blocks](https://github.com/PhilipYip1988/python-tutorials/blob/main/007_programming_constructs_with_code_blocks/readme.md)

The builtins module contains the ```str```, ```list```, ```tuple```, ```set``` and ```dict``` collections. The collections module includes a number of additional collections which supplement these such as the ```NamedTuple``` which is a ```tuple``` subclass that has field names, ```deque``` (double ended queue) that is list like, ```defaultdict``` which is a ```dict``` subclass with default behaviour when new keys that don't exist are indexed, and ```Counter``` which is a ```dict``` subclass used for counting. A number of these collections almost became inbuilt identifiers themselves and therefore this is one of the closest modules to Python ```builtins```. Learning this module at this stage will build an understanding for subclassing:

[Collections Module](https://github.com/PhilipYip1988/python-tutorials/blob/main/008_collections_module/readme.md) 

The concept of an iterators was covered briefly when looking at programming constructs using code blocks. The ```builtins``` module contains commonly used iterators such as the ```zip```, ```filter``` and ```map``` iterator classes. Python also has an iterator module ```itertools``` that contains ```zip_longest```, ```filterfalse```, and ```starmap``` iterator classes which complement their similar counterpart in ```builtins```. The itertools module also has a ```cycle```, ```repeat``` and ```count``` iterator classes which are endless iterators. The ```cycle``` iterator can be used to continuously index around a collection, returning to the top after reaching the bottom. Like the collections module, the itertools module is one of the closest modules to Python builtins. Effective use of these two modules simplifies common programming tasks and generally makes the code more Pythonic and easier to read:

[Iterator Tools Module](https://github.com/PhilipYip1988/python-tutorials/blob/main/009_itertools_module/readme.md) 

## Math and Statistics

The ```math``` module is used to carry out common mathematical operations on scaler numeric data. Learning how to use this module and reinforcing the underlying mathematics is a perquisite when it comes to any data science tasks. There is an associated complex math module ```cmath``` which is designed to handle complex numbers:

[Math and Complex Math Modules](https://github.com/PhilipYip1988/python-tutorials/blob/main/010_math_module/readme.md) 

The ```random``` module is a pseudo random number generator which can be used to select a choice or choices from a list which are operations done with replacement. Alternatively it may be used to select a sample from a list which is done without replacement or to mutate the existing list by shuffling it. There are also a number of statistical distributions that a number can be generated from including the commonly used uniform, normal and exponential distributions:

[Random Module](https://github.com/PhilipYip1988/python-tutorials/blob/main/011_random_module/readme.md)

The ```datetime``` module is a module for working with dates and times. The associated ```zoneinfo``` module is for dealing with timezones. The ```time``` module is a module written in C and exists mainly for advanced use timing applications. There are a couple of the functions from the ```time``` module that are commonly used such as ```time``` which retrieves the time from the system hardware and ```sleep``` which is used to delay execution of a Python script:

[DateTime, ZoneInfo and Time Modules](https://github.com/PhilipYip1988/python-tutorials/blob/main/012_datetime_module/readme.md)

The ```statistics``` module is a module for working with basic statistics:

[Statistics Module](https://github.com/PhilipYip1988/python-tutorials/blob/main/013_statistics_module/readme.md)

## Programming Constructs Continued

The system module ```sys``` gives details about objects used or maintained by the Python interpreter. This gives details about the builtin modules, the standard modules and third-party modules. Custom user modules can also be added:

[The System Module and Working with Custom Modules](https://github.com/PhilipYip1988/python-tutorials/blob/main/014_system_module_custom_modules/readme.md)

This tutorial will look at the concept of a class, a subclass, using an Abstract Base Class (ABC) from the ```abc``` module to create a design pattern and ultimately creating a custom class where each instance has data attributes and instance methods:

[The Abstract Base Classes Module and Custom Classes](https://github.com/PhilipYip1988/python-tutorials/blob/main/015_abc_custom_classes/readme.md)

## Working with Files

The previous tutorials looked at programming constructs which compartmentalised Python code. In addition to code compartmentalisation, there is often data compartmentalisation. There are a number of file formats used to store data such as the text file (.txt), the comma seperated values file (.csv), and the JavaScript Object Notation file (.json). 

To work with files the Operating System module ```os``` is typically used to navigate around the Operating System and perform low level file and directory operations. This is supplemented by the Shell Utilties Module ```shutil``` for higher level operations such as copying. The file statistics module ```stat``` gives file statistics otherwise known as file properties. Note the ```stat``` module should not be confused with the ```statistics``` module and the ```shutil``` module (copying files or directories) should not be confused with the ```copy``` module (copying Python objects) which have previously been examined:

[The Operating System, Stat and Shell Utilities Modules](https://github.com/PhilipYip1988/python-tutorials/blob/main/016_operating_system_module/readme.md)

The Comma Separated Values Module ```csv``` allows basic reading and writing of ```csv``` files to ```builtins``` objects, in the form of lists of strings or nested lists of strings. Use of this basic module gives a good understanding of the file format. It is more routine to read the .csv file format into a more specialised data structure such as the ```DataFrame``` which the Python and Data Analysis Library revolves round. This will be discussed in a later tutorial:

[The Comma Separated Values Module](https://github.com/PhilipYip1988/python-tutorials/blob/main/017_comma_separated_values_module/readme.md)

Python objects can be serialized to a bytes object for data transfer. The ```pickle``` module is used to serialize Python data, because the serialized data is hard for a user to visualize, it is said to pickled. This serialized data can be saved to a bytes string or to a ```.txt``` file. The associated ```shelve``` module creates a database which consists of shelves of pickled data:

[Serializing Python Objects using the Pickle and the Shelve Modules](https://github.com/PhilipYip1988/python-tutorials/blob/main/018_pickle_module/readme.md)

### Data Science Libraries

The Numeric Python Library known as numpy is based around the ```ndarray```. The ```ndarray``` is a multi-dimensional numeric array that is configured for numeric data. The identifiers and data model identifiers for the ```ndarray``` are configured for numerical operations, math and statistics essentially allowing broadcasting of an operation over the size of the array. This allows for a much cleaner syntax and faster operation than the use of multiple for loops. The numpy library also has an associated random module that allows broadcasting of randomly generated numbers across an array and has a more accurate datetime and timedelta giving ns precision. The numpy library is the general foundation for all other scientific libraries:

[The Numeric Python Library](https://github.com/PhilipYip1988/python-tutorials/blob/main/021_numeric_python_library/readme.md)

The Matrix Plotting Library known as ```matplotlib``` is Pythons most commonly used plotting library, and the base library of other common plotting libraries. matplotlib as the name suggests is designed for plotting numeric data in 1d ndarrays and 2d ndarrays. This library is commonly used for an assortment of plots including, line plots, scatter plots, bar graphs, pie charts, histograms, box plots, violin plots, matrix color plots, contour plots, surface plots and wireframe plots:

[The Matrix Plotting Library](https://github.com/PhilipYip1988/python-tutorials/blob/main/022_matrix_plotting_library/readme.md)

Incomplete tutorial: Beginning Section Complete

The Seaborn Data Visualisation Library is a wrapper library around ```pyplot``` and allows easy visualisation from data within a ```pandas``` ```DataFrame``` instance. ```seaborn``` includes 1 line plot commands for the most commonly used data visualisations. In theory all the plots that can be created in ```seaborn``` can be produced directly using ```pyplot``` however the simplified syntax of ```seaborn``` is often more elegant and makes the code more readible, allowing more focus on the data visualisation:

[The Seaborn Library](https://github.com/PhilipYip1988/python-tutorials/blob/main/024_seaborn_library/readme.md)