数据处理：
python data_process.py

特征选择：
python FeatureSelecion.py

特征权重计算：
python FeatureWeight.py
python TestFeatureWeight.py

对train.svm文件数据进行缩放到[0,1]区间

svm-scale -l 0 -u 1 train.svm > trainscale.svm

对test.svm文件数据进行缩放到[0,1]区间

svm-scale -l 0 -u 1 test.svm > testscale.svm

对trainscale.svm 文件进行模型训练

svm-train -s 1 trainscale.svm trainscale.model

对testscale.svm 文件进行模型预测，得到预测结果，控制台会输出正确率

svm-predict testscale.svm trainscale.model testscale.result
