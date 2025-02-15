﻿# Roffild's Library

I am known to the MQL5 community by the name of Roffild and this is my open source library for MQL5.
An attempt to implement the features on MQL5, which have long become the standard for popular programming languages.
Each file has one idea. The library is replenished as needed for new capabilities.

Few people tried to put the project in Github. There is no single standard.
MetaQuotes does not use version control systems when creating a project.
For some reason, programmers from MetaQuotes believe that the project should be of the same type.
For small projects that are published in CodeBase on the MQL5.com site, this division is justified.
For medium and large projects, it is not possible to select one type of project.

I experimented with different structure of the project.
To use Git, I had to take the files out of the standard folder structure that MetaQuotes adopted.
Create a link to the staging folder (in this library, the folder "Roffild") - the best option.

MetaEditor can save code in UTF-16, but encoding UTF-8 with BOM is also supported.
To convert a file with the source code, you need to use a third-party editor (I recommend [Notepad++](https://notepad-plus-plus.org/)).

This library can be divided into interests:
* common tasks (ArrayList, Log4MQL, ToIndicator, etc.);
* experiments with AlgLib in machine learning;
* using Apache Spark with Amazon Web Services (EC2 and EMR), when the capabilities of AlgLib ceased to be enough;
* using TensorFlow or PyTorch via [PythonDLL](https://roffild.com/PythonDLL.html).

MQL5 is part of the trading platform MetaTrader 5 (MT5) for Forex, CFD and Futures. The version of MetaTrader 4 (MT4) with MQL4 is still used, but after the latest updates it is compatible with the MQL5 syntax. Officially, the version of MetaTrader 4 (MT4) is no longer supported, but for compatibility you can use ``` #property strict ``` at the beginning of the file.

### Documentation
[MQL5](https://roffild.com/mql5/)<br/>
[Java](https://roffild.com/java/)

### Links
[Roffild.com](https://roffild.com/)<br/>
[Github](https://github.com/Roffild/RoffildLibrary)<br/>
[GitLab](https://gitlab.com/Roffild/RoffildLibrary)<br/>
[BitBucket](https://bitbucket.org/Roffild/roffildlibrary/)<br/>
[MQL5.com: topic for discussion in English](https://www.mql5.com/en/forum/247134)<br/>
[MQL5.com: тема для обсуждения на Русском](https://www.mql5.com/ru/forum/245373)

-----------------
* [Experts/Roffild/](Experts/Roffild/)
  * [AmazonUtils](Experts/Roffild/AmazonUtils) - Can be used as an example of developing a project in Java.
  * [Alglib_MultilayerPerceptron.mq5](Experts/Roffild/Alglib_MultilayerPerceptron.mq5) - Create a neural network (Multilayer Perceptron) with two hidden layers.
  * [Alglib_RandomForest.mq5](Experts/Roffild/Alglib_RandomForest.mq5) - Create a random forest.
  * [Examples/](Experts/Roffild/Examples/)
    * [PythonDLL_Example.mq5](Experts/Roffild/Examples/PythonDLL_Example.mq5) and [PythonDLL_Example.py](Experts/Roffild/Examples/PythonDLL_Example.py) - The example of using [PythonDLL](https://roffild.com/PythonDLL.html).
    * [ToIndicator_Example.mq5](Experts/Roffild/Examples/ToIndicator_Example.mq5)
* [Include/Roffild/](Include/Roffild/)
  * [MLPDataFile.mqh](Include/Roffild/MLPDataFile.mqh) - Data format for Alglib_MultilayerPerceptron and Alglib_RandomForest. MLPDataFile = CSV in a binary format.
  * [ArrayList_macros.mqh](Include/Roffild/ArrayList_macros.mqh) - This variant is still used because of poor template support by the code editor.
  * [ArrayList.mqh](Include/Roffild/ArrayList.mqh) - ArrayList from Java.
  * [ArrayListClass.mqh](Include/Roffild/ArrayListClass.mqh) - ArrayList from Java for Class only.
  * [ForestSerializer.mqh](Include/Roffild/ForestSerializer.mqh) - Save and load data for the class CDecisionForest (Alglib).
  * [Log4MQL.mqh](Include/Roffild/Log4MQL.mqh) and [Log4MQL_tofile.mqh](Include/Roffild/Log4MQL_tofile.mqh) + [module](Include/Roffild/LogMX) ([download](https://roffild.com/Log4MQLParser.zip)) for [LogMX](http://www.logmx.com/) - Logger for MQL5 (Log4MQL).
  * [OrderData.mqh](Include/Roffild/OrderData.mqh) - Simulation of orders with attached data for research.
    * [OrderSql.mqh](Include/Roffild/OrderSql.mqh) - Record data of simulated orders (COrderData) in a file format MySQL.
  * [SqlFile.mqh](Include/Roffild/SqlFile.mqh) - Write data to a file format MySQL.
    * [CsvFile.mqh](Include/Roffild/CsvFile.mqh) - Write data to a file format CSV.
  * [Statistic.mqh](Include/Roffild/Statistic.mqh) - Counting data and printing out the accumulated information.
  * [TesterSql.mqh](Include/Roffild/TesterSql.mqh) - Record optimization results in SQL and CSV format files.
  * [ToIndicator.mqh](Include/Roffild/ToIndicator.mqh) - Displaying data from Expert or Script using functions for indicators.
  * [UnitTest.mqh](Include/Roffild/UnitTest.mqh) - Base class for UnitTest.
  * [Serialization.mqh](Include/Roffild/Serialization.mqh)
  * [RoffildJava/](Include/Roffild/RoffildJava/)
    * [AmazonUtils](Include/Roffild/RoffildJava/AmazonUtils/)
    * [RoffildLibrary](Include/Roffild/RoffildJava/RoffildLibrary/)
    * [Spark](Include/Roffild/RoffildJava/Spark/) - Reading from MLPDataFile.
    * [aws_ubuntu_user_data.sh](Include/Roffild/RoffildJava/AmazonUtils/src/main/resources/aws_ubuntu_user_data.sh) - Working script for raising test agents on Ubuntu in AWS. [The documentation is here.](https://roffild.com/agents.html)
  * [PythonDLL.mqh](Include/Roffild/PythonDLL.mqh) - Class for [PythonDLL](https://roffild.com/PythonDLL.html).
  * [RoffildPython/](Include/Roffild/RoffildPython/)
* [Indicators/Roffild/](Indicators/Roffild/)
  * [ToIndicator.mqh](Indicators/Roffild/ToIndicator.mqh)
  * [ToIndicator.mq5](Indicators/Roffild/ToIndicator.mq5)
  * [ToIndicator_window.mq5](Indicators/Roffild/ToIndicator_window.mq5)
* [Libraries/Roffild/](Libraries/Roffild/)
  * [PythonDLL/](Libraries/Roffild/PythonDLL/) - [PythonDLL](https://roffild.com/PythonDLL.html).
* [Scripts/Roffild/](Scripts/Roffild/)
  * [MLPDataFileSparkTest](Scripts/Roffild/MLPDataFileSparkTest) - Example project for Spark and MLPDataFile test.
  * [UnitTests](Scripts/Roffild/UnitTests)
* [buildall_and_tests.py](buildall_and_tests.py) - The script builds all components of the library and run tests.

## Installation

(Optionally)

``` mklink /j link where ``` - does not require administrator rights.

It makes sense to move the ``` %APPDATA%\MetaQuotes ``` folder to the root of the partition or to a larger partition.
Windows has a limit of 255 characters to the file path. The full path to the MQL5 folder I have is 88 characters.
When testing, the terminal copies history by the number of local agents that increases the size of this folder by several gigabytes.
1. Move the ``` %APPDATA%\MetaQuotes ``` to ``` D:\MQLProjects ```
2. ``` mklink /j %APPDATA%\MetaQuotes D:\MQLProjects ```
3. ``` mklink /j D:\MQLProjects\MQL5 D:\MQLProjects\Terminal\D0E8209F77C8CF37AD8BF550E51FF075\MQL5 ```

(Important)

Run the ``` create_links.bat ``` from the ``` MQL5\MyProjects\RoffildLibrary ``` folder after cloning the project.

## Code style

[Google Java Style](https://google.github.io/styleguide/javaguide.html)

Tab = 3 spaces

Column limit = 110

## License

[Apache License 2.0](LICENSE)
