# Topic Model Vizualization Kit (TMVK)

This repository contains a set of scripts and a directory structure


topic-viz.py - This script processes the output of nPLSA topic models and produces JSON files to drop into the static HTML directory (described below).

./data - put the data files produced by the nPLSA topic model in this directory. The script expects to find the following files:
- nplsa.topicSize.NUM 
- nplsa.model.NUM 

in this directory so that it can produce the JSON files needed for the visualizations. 

./html - This is a directory for holding the contents of a static HTML site built from the data generated by the topic model.


Once you have put the nPLSA model files in the ./data/ directory, you can run topic-viz.py. But before you do that, you need to install a few python packages. topic-viz.py relies on [Numpy](http://www.numpy.org/), [Scipy](http://scipy.org/), and [Scikit-learn](http://scikit-learn.org). These libraries are needed for the dimension reduction step that uses PCA in the scikit-learn package. The best way to install these packages is with ```easy_install```:

```
easy_instal numpy
easy_install scipy
easy_install scikit-learn
```

The installation of these packages might take a while, scipy has to compile FORTRAN. If you have difficulty or those installation steps don't work (which is highly likely), please let me know.
