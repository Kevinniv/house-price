# 
1. 基于Kaggle平台提供的《Airbnb平台2019年纽约房价》数据集，预处理数据。训练了多种机器学习模型，以根据提供的多种数据来预测房价，并总结出最佳预测方案。

2. 使用基于python的NumPy, Pandas, Matplotlib, Seaborn, Plotly, Maps模块预处理及可视化数据。绘制Heatmap, Bar plot, Violin plot, Scatter Plot等图像来观察数据的分布和异常值，便于后续数据清洗。结合数据提供的信息可以绘制出房价分布图、房子类型分布图等，以便更直观的观察并分析数据。运用RobustScaler进行数据归约，平衡各特征的权重。

3. 基于预处理后的数据集，利用KFold交叉验证来调整模型的超参数进行模型调优。分别训练了Logistic Regression, Ridge Regression, LASSO Regression, Huber regression, Random Forest Regressor, XGBoost Regressor等模型并寻找最佳参数。利用LIME进行模型解释，增加可信度。计算并比较多个模型预测结果与实际数据的误差。通过均方误差MSE(Mean Squared Error), R方值(R2_score)来评价模型好坏。均方差降低50%，R方值最高提高240%，十分接近1。

4. 结论为：填补缺失数据，删除异常数据，可以使训练后的模型更加准确，房价预测结果更加精确；对样本不同特征进行取舍和转换，可以避免丢失数据，最大化利用现有信息；通过对多种模型寻参，可以提升模型精度，如本项目中LASSO Regression模型在最佳参数情况下，模型测试准确率提高了130%。由于XGBoost模型使用了梯度下降法来优化回归树，加入了正则项，用于控制模型的复杂度，并且防止过拟合，且算法中的并行计算提高了硬件的运行效率，使得该模型更加快速准确，更适合解决此种回归问题。
