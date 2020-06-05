# svm
opencv简单实践14：K means

练习1 1K means

data: 需要自动聚类的数据，一般是一个Mat。浮点型的矩阵，每行为一个样本。
k: 取成几类，比较关键的一个参数。
bestLabels: 返回的类别标记,整型数字。
criteria: 算法结束的标准，获取期望精度的迭代最大次数
attempts: 判断某个样本为某个类的最少聚类次数，比如值为3时，则某个样本聚类3次都为同一个类，则确
定下来。
flags: 确定簇心的计算方式。有三个值可选：KMEANS_RANDOM_CENTERS 表示随机初始化簇心。
KMEANS_PP_CENTERS 表示用kmeans++算法来初始化簇心, KMEANS_USE_INITIAL_LABELS 表示第一次
聚类时用用户给定的值初始化聚类，后面几次的聚类，则自动确定簇心。
centers: 用来初始化簇心的。与前一个flags参数的选择有关。如果选择KMEANS_RANDOM_CENTERS随机
初始化簇心，则这个参数可省略。
