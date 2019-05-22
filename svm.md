#SVM

Definition: Hyperplane:
>It's the one that maxmizes the margins from both tags. In otehr words: the hyperplane whose distance to the nearest
element of each tag is the largest


Codes:
```
from sklearn.svm import SVC  #from sklearn family, SVC is a genous, as similar as others
classifier = SVC(kernel = 'linear', random_state = 0)
classifier.fit(X_train,Y_train)
output:SVC(C=1.0, cache_size=200, class_weight=None, coef0=0.0,
decision_function_shape='ovr', degree=3, gamma='auto_deprecated',
kernel='linear', max_iter=-1, probability=False, random_state=0,
shrinking=True, tol=0.001, verbose=False) # gamma can be used to justify model(to be specified;)

```
There are nine kenerls:

Name|Descripition
-|-
linear kernel|线性可分时，特征数量多时，样本数量多再补充一些特征时，linear kernel可以是RBF kernel的特殊情况
Polynomial kernel|image processing，参数比RBF多，取值范围是(0,inf)(-d：多项式核函数的最高次项次数，-g：gamma参数，-r：核函数中的coef0)
Sigmoid kernel|生成神经网络，在某些参数下和RBF很像，可能在某些参数下是无效的
Gaussian kernel and Laplace RBF kernel |通用，在没有先验知识时用	
Hyperbolic tangent kernel|neural networks中用
Bessel function of the first kind Kernel|可消除函数中的交叉项	
ANOVA radial basis kernel|回归问题
Linear splines kernel in one-dimension|text categorization，回归问题，处理大型稀疏向量

Result (rbf kernel and linear kernel):
<center>
    <img src="SVM rbf kernel.png"  width = "300" height = "260")/> <img src="SVM linear kernel.png" width = "300" height = "260")/>
S
</center>

Variable | Descripition
-|-
gamma|隐含地决定了数据映射到新的特征空间后的分布，gamma越大，支持向量越少，gamma值越小，支持向量越多。支持向量的个数影响训练与预测的速度。
 C（惩罚系数）即对误差的宽容度|C 越高，容易过拟合。C 越小，容易欠拟合。C过大或过小，泛化能力变差。


Definition | Used in
-|-
kernel|核函数对两个特征向量的内积进行变换，这样做等价于先对向量进行映射然后再做内积。通过核函数，支持向量机可以将特征向量映射到更高维的空间中，使得原本线性不可分的数据在映射之后的空间中变得线性可分。
Outlier | over the boundary
泛化|




![](https://github.com/Avik-Jain/100-Days-Of-ML-Code/raw/master/Info-graphs/Day%2012.jpg)












