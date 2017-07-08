# Denoising
    蒙特卡罗（Monte Carlo）光线追踪方法是进行图像渲染的一种重要方法，<br>
 而其基于光线追踪的方式使得采样后的图片或多或少会有噪声，在低采样率的图片中这种噪声更加明显，<br>
 甚至会使人无法分辨图片中的事物。近年来，为使用低采样率以获得最高渲染速度，对图像的降噪处理成为了一个热门话题。<br>
 滤除MC噪声的最成功方法是基于特征值的过滤器（例如：cross-bilateral过滤器和 non-local means过滤器）。<br>
 这种过滤器是利用额外的场景特征，
 如空间位置和阴影法线等，为过滤器中的每个部分找到最优的参数用于滤除噪声，而不是保留场景的细节。<br>
 对于这些最优参数，可以通过机器学习的方法来获取，这样可以使得设计出的过滤器能够适应不同类别的场景，比如景深或是运动模糊。<br>
 因此，通过机器学习的方法来设计过滤器可以获得更为接近真实场景的图像。<br>
   支持向量机（Support Vector Machine）是一种机器学习的数学方法，由Corinna Cortes和Vapnik等于1995年提出。<br>
 在解决小样本的模式识别问题上有很大优势，而后的支持向量回归（Support Vector Regression）提供了非线性预测问题的解决方案。<br>
 这里将采用支持向量机模型的分类方法根据Kalantari等人提出的图像像素的二级特征，<br>
 对图像像素进行分类，提取出需要处理的噪声像素输出到过滤器进行过滤，已达到减少过滤器工作量进而增加图像降噪速度。<br>
