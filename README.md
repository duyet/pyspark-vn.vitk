# About pyspark-vn.vitk 

Vitk - A Vietnamese Text Processing Toolkit, is the third release of a Vietnamese text processing toolkit, which is called "Vitk", developed by [Phuong LE-HONG](http://mim.hus.vnu.edu.vn/phuonglh) at College of Science, Vietnam National University in Hanoi.

However, vn.vitk readily scalable for large data processing, build on top of Apache Spark. This working as command line tools, base on Spark running background, and cannot using as programming.

**pyspark-vn.vitk** is a small snippet code, modified source code of **vn.vitk** (custom version [vn.vitk-3.0.jar](lib/vn.vitk-3.0.jar)) to run on PySpark, using py4j calling to vn.vitk's Java code.

See the tutorial here in Vietnamese.

# Converted to PySpark 

* Tokenizer - See [pyspark-Tokenizer](pyspark-Tokenizer.ipynb)

# How to contribute

1. Fork the project on Github
2. Create a topic branch for your changes
3. Ensure that you provide documentation and test coverage for your changes (patches won’t be accepted without)
4. Create a pull request on Github (these are also a great place to start a conversation around a patch as early as possible)

### * Using Jupyter Notebook
See my blog how to using Notebook with Spark: http://blog.duyetdev.com/2016/09/chay-apache-spark-voi-jupiter-notebook.html

### ** Submit vn.vitk-3.0.jar to Spark in Notebook

```
export PYSPARK_DRIVER_PYTHON=ipython
export PYSPARK_DRIVER_PYTHON_OPTS="notebook --NotebookApp.open_browser=False --NotebookApp.ip='*' --NotebookApp.port=8880"
export SPARK_HOME=~/spark-1.6.2-bin-hadoop2.6 # Path to home of Spark

$SPARK_HOME/bin/pyspark --jars=./lib/vn.vitk-3.0.jar
```


# License

MIT License

Copyright (c) 2015 Van-Duyet Le

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.