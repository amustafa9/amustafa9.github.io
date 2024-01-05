<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        /* Initially hide the additional content */
        #more-content {
            display: none;
        }

        /* Style the text as a link or regular text */
        #show-more-link {
            color: darkblue;
            text-decoration: underline; /* Add underline for a link-like appearance */
            cursor: pointer; /* Add cursor pointer to indicate interactivity */
        }
    </style>
    <title>Show More Text</title>
</head>

<h1 id="research"></h1>
<h2 style="margin: 60px 0px 10px;">Research</h2>



<h3 style="margin: 0px 10px 10px 0px;">Efficient Training Sample Selection for Seismic Interpretation using Active Learning</h3>
<img src="./assets/teaser/geo-al.png" class="teaser img-fluid z-depth-1" style="width=100%;height=100%">
Machine learning-assisted seismic interpretation tasks require large quantities of labeled data annotated by expert interpreters, which is a costly and time-consuming process. Where existing works to minimize dependence on labeled data assume the data annotation process to already be completed, active learning---a field of machine learning---works by selecting the most important training samples for the interpreter to annotate in real time simultaneously with the training of the interpretation model itself, thereby reducing cost and effort to produce annotated training samples while minimizing the negative impact on performance. We develop a unique and first-of-a-kind active learning framework for seismic facies interpretation using the manifold learning properties of deep autoencoders. 

<p id="show-more-link" onclick="toggleContent()">Show more</p>
<div id="more-content">
By jointly learning representations for supervised and unsupervised tasks and then ranking unlabeled samples by their nearness to the data manifold, we are able to identify the most relevant training samples to be labeled by the interpreter in each training round. This is shown in the figure below. On the popular F3 dataset, we obtain close to 10 percentage point difference in terms of interpretation accuracy between the proposed method and the baseline with only three fully annotated seismic sections.

<h4 style="margin: 10px 10px 10px 0px;">Results</h4>
Performance of the facies segmentation model is recorded in terms of the mean intersection-over-union (mIOU) at the end of every cyle and plotted for the proposed sampling method as well as other sampling techniques. This includes the well known active learning method based on entropy as well as non-active learning techniques commonly used by seismic interpreters. These plots for both training and test splits are given below.

<figure>
    <img src="./assets/img/miou_train.png" alt="Alt Text for Image 1">
    <figcaption>Performance curves for the proposed and baseline sampling techniques on the training split.</figcaption>
</figure>

<figure>
    <img src="./assets/img/miou_test.png" alt="Alt Text for Image 1">
    <figcaption>Performance curves for the proposed and baseline sampling techniques on the test split.</figcaption>
</figure>

<h4 style="margin: 10px 10px 10px 0px;">Codes</h4>
Codes related to this project can be found at <a href="https://github.com/olivesgatech/active-learning-interpretation">this GitHub repository</a>. Detailed instructions regarding the running of the codes and installing related dependencies are provided.
<h4 style="margin: 10px 10px 10px 0px;">Related Publications</h4>
More information on this work can be found in the following publidations: 
<br>
1. Mustafa, Ahmad, and Ghassan AlRegib. "Man-recon: Manifold learning for reconstruction with deep autoencoder for smart seismic interpretation." In 2021 IEEE International Conference on Image Processing (ICIP), pp. 2953-2957. IEEE, 2021. <a href="https://ieeexplore.ieee.org/abstract/document/9506657"> [Link] </a> <a href="https://arxiv.org/pdf/2212.07568.pdf"> [PDF] </a> 
<br>
2. Mustafa, Ahmad, and Ghassan AlRegib. "Active learning with deep autoencoders for seismic facies interpretation." Geophysics 88, no. 4 (2023): IM77-IM86. <a href="https://library.seg.org/doi/am-pdf/10.1190/geo2022-0353.1"> [Link] </a> <a href="https://eartharxiv.org/repository/view/5308/"> [PDF] </a> 
</div>

<!-- Next research item. -->

<h3 style="margin: 10px 10px 10px 0px;">Learning under Sparse, Missing Labels for Structure Interpretation via Visual Attention Modeling</h3>
<img src="./assets/img/attention_mechanisms.PNG" class="teaser img-fluid z-depth-1" style="width=100%;height=100%">
Accurate interpretation of visual data for relevant information forms an important component of many real-world applications such as medical disease diagnosis, geological hazard assessment, hydrocarbon exploration, etc. Producing fine-grained annotations on images is an expensive, laborious, and time-consuming process. The human brain is wired to selectively focus its attention on certain aspects of the visual scene. This perception mechanism is driven both by low-level signal cues, such as changes in color, contrast, intensity, shapes etc., as well as high-level cognitive factors such as one’s prior knowledge, goals, expectations, and constraints with respect to the task at hand. 

<p id="show-more-link" onclick="toggleContent()">Show more</p>
<div id="more-content">
These attentional factors, referred to as bottom-up and top-down attention respectively, play an important role in determining the final annotations that get produced for a given visual scene, often at the cost of leaving out a lot of visual information the brain deems to be unimportant with regard to the task of interest. Mapping geological faults on 3D seismic volumes is one such application where human attention selectivity results in highly incomplete fault annotations. Conventional supervised learning methods treat regions of missed fault labels as negatives, resulting in non-optimal learning for the machine learning model. We propose a method to model visual attention and incorporate it into data sampling and model training procedures. We demonstrate the utility of this approach for mapping faults on seismic volumes using pretrained 3D convolutional neural networks (CNNs). Using an annotated seismic dataset from NW Australia, we show quantitatively and qualitatively that modeling visual attention leads to significant performance gains even with limited, incompletely labeled seismic training data.

<h4 style="margin: 10px 10px 10px 0px;">Results</h4>
Fault interpretation is carried out using a model trained in the proposed manner (i.e., attention modeling) and also using models trained without modeling visual attention. The proposed approach can be seen to outperform baseline strategies even when trained on data with highly incomplete labels.

<figure>
    <img src="./assets/img/attention_comparison_1.png" alt="Alt Text for Image 1">
    <figcaption>Performance curves for the proposed and baseline training startegies on a seismic section from the test set.</figcaption>
</figure>

<figure>
    <img src="./assets/img/attention_comparison_3.png" alt="Alt Text for Image 1">
    <figcaption>Performance curves for the proposed and baseline training startegies on a seismic section from the test set.</figcaption>
</figure>

<h4 style="margin: 10px 10px 10px 0px;">Codes</h4>
Codes related to this project can be found at <a href="https://github.com/amustafa9/attention-fault-interpretation">this GitHub repository</a>. Detailed instructions regarding the running of the codes and installing related dependencies are provided.
<h4 style="margin: 10px 10px 10px 0px;">Related Publications</h4>
More information regarding the work can be accessed at the publications below:
<br>
1. A. Mustafa, R. Rastegar, T. Brown, G. Nunes, D. De Lilla, and G. AlRegib, "Adaptive Finetuning of 3D CNNs With Interpretation Uncertainty for Seismic Fault Prediction," in IEEE Transactions of Geoscience and Remote Sensing. <a href="https://eartharxiv.org/repository/view/5558/">[Preprint]</a>
</div>

<script>
    // JavaScript function to toggle the visibility of additional content
    function toggleContent() {
        var moreContent = document.getElementById("more-content");
        var showMoreLink = document.getElementById("show-more-link");

        // Toggle the display property of the additional content
        if (moreContent.style.display === "none") {
            moreContent.style.display = "block";
            showMoreLink.textContent = "Show less";
        } else {
            moreContent.style.display = "none";
            showMoreLink.textContent = "Show more";
        }
    }
</script>
