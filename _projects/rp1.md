---
layout: default
title: "Corruption Robustness"
---

<h2>Corruption Robustness</h2>
<img src="/assets/research_img/rp1_hendrycks_corruptions.PNG" alt="Corruption Robustness" style="max-width:100%; height:auto;">
<p>Corruption Robustness, or statistical robustness, describes the ability of a model to cope with randomly distributed changes in its input data. Unlike adversarial robustness, the changes are not assumed to be worst-case. 
Corruption robustness is primarily concerned with real-world data errors, such as camera or sensor corruption in image data, but can theoretically be extended to any type or distribution of errors. Corruption robustness evaluation typically involves tests on corrupted benchmark datasets, such as the popular corrupted variants of the image classification datasets CIFAR-C and ImageNet-C (see image above, from reference [1]). 
    
    Research shows that vision models in particular suffer significant performance degradation when confronted with such real-world corruptions. One research question is therefore how to train models that are as robust as possible against all known types of random corruption. Approaches to solving this research question include model architecture and optimisation choices, and, prominently, training data augmentation. Even state-of-the-art training strategies have not yet closed the gap between model performance on clean and corrupted data. Many approaches achieve corruption robustness at the expense of accuracy on clean data. The holy grail of a training strategy is therefore to reliably improve corruption robustness and accuracy together on clean test data. 
    Below: Robust image model training pipeline with various data augmentation approaches
<img src="/assets/research_img/rp1_data_augmentation.png" alt="Corruption Robustness" style="max-width:80%; height:auto;">
    
    Another research question is how to comprehensively and expressively evaluate corruption robustness. The goal is to achieve corruption robustness against the entire relevant set of possible corruptions and for meaningful severities. Therefore, different realistic and challenging corruption types and meaningful corruption severities need to be developed and evaluated. The aim of this line of research is to produce reliable and interpretable measures of corruption robustness for given models. 
    Below: Left: 2D concept of testing statistical robustness with noise centred around the original data points [2]. Right: Various random noise distributions for statistical robustness testing [3].
    
    We focus on researching the robustness of corruption, as it goes hand in hand with the reliability of machine learning models. Please find below a selection of our publications in this area.</p>
<img src="/assets/research_img/rp1_statistical_robustness_testing.png" alt="Corruption Robustness" style="max-width:80%; height:auto;">

<h3>Links</h3>
<ul>
    Popular Literature:
    
    <li><a href="https://github.com/hendrycks/robustness" target="_blank">[1]: Benchmarking Neural Network Robustness to Common Corruptions and Perturbations</a></li>
    <li><a href="https://proceedings.neurips.cc/paper/2021/file/1d49780520898fe37f0cd6b41c5311bf-Paper.pdf" target="_blank">On interaction between augmentations and corruptions in natural corruption robustness</a></li>
    
    Our References:
    
    <li><a href="https://www.researchgate.net/publication/361562813_Utilizing_Class_Separation_Distance_for_the_Evaluation_of_Corruption_Robustness_of_Machine_Learning_Classifiers" target="_blank">[2]: Utilizing Class Separation Distance for the Evaluation of Corruption Robustness of Machine Learning classifiers</a></li>
    <li><a href="https://www.researchgate.net/publication/376723060_Investigating_the_Corruption_Robustness_of_Image_Classifiers_with_Random_p-norm_Corruptions" target="_blank">[3]: Investigating the Corruption Robustness of Image Classifiers with Random p-norm Corruptions</a></li>
</ul>
