# Census Income Classification
*Instructions for compiling and executing my code:*
### Set up
* [python3.6]
* [pandas]
* [numpy]
* [sklearn]


[python3.6]: <https://www.python.org/downloads/release/python-360/>
[pandas]: <https://pandas.pydata.org/>
[numpy]: <https://github.com/numpy/numpy>
[sklearn]: <https://github.com/scikit-learn/scikit-learn>



### Classification Model
This model will predict whether a person have more than 50,000 dollars salary.
1. training process
```sh
Usage:
python train_classify.py -i <inputfile> -c <classifier> -f <selection_model> -o <model output>

Example:
python train_classify.py -i data/census-income.data  -c boot -f forest -o forest_model.sav

Options:
-i: input file
-c: classifier methods: kfold or boot
-f: classification model: logistic, forest, boosting
-o: output file of training model
```

2. prediction process
```sh
Usage:
python predict_classify.py -i <inputfile> -m <model file>

Example:
python predict_classify.py -i data/classification-test.data -m forest_model.sav

Options:
-i: input file
-m: model file
```

### Significant Features Selection
```sh
Usage:
python feature_FSS.py -i <inputfile> -f <feature_selection_model>

Example:
python feature_FSS.py -i data/census-income.data -f forest

Options:
-i: input file
-f: feature selection model: forward, forest, boosting
```

### Segementation Model
1. training process
```sh
Usage:
python train_seg.py -i <inputfile> -cluster <segementation_model> -n <number of clusters> -o <model output>

Example:
python train_seg.py -i data/census-income.data -cluster KNN -n 10 -o seg_model.sav

Options:
-i: input file
-cluster: segementation model: KNN or GMM
-o: output file of training model
```


2.  prediction process
```sh
Usage:
python predict_seg.py -i <inputfile> -m <model file>

Example:
python predict_seg.py -i data/segmentation-test.data -m seg_model.sav

Options:
-i: input file
-m: model file
```

3. Generating feature histogram for analysis
```sh
Usage:
python features_analysis.py -i <inputfile> -o <ouput file>

Example:
python features_analysis.py -i data/census-income.data -o features_analysis.txt

Options:
-i: input file
-o: output file
```
