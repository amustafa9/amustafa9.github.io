<h1 id="research"></h1>
<h2 style="margin: 60px 0px 10px;">Research</h2>



<h3 style="margin: 0px 10px 10px;">Efficient Training Sample Selection for Seismic Interpretation using Active Learning</h3>
<img src="./assets/teaser/geo-al.png" class="teaser img-fluid z-depth-1" style="width=100%;height=100%">
Machine learning-assisted seismic interpretation tasks require large quantities of labeled data annotated by expert interpreters, which is a costly and time-consuming process. Where existing works to minimize dependence on labeled data assume the data annotation process to already be completed, active learning---a field of machine learning---works by selecting the most important training samples for the interpreter to annotate in real time simultaneously with the training of the interpretation model itself, thereby reducing cost and effort to produce annotated training samples while minimizing the negative impact on performance. We develop a unique and first-of-a-kind active learning framework for seismic facies interpretation using the manifold learning properties of deep autoencoders. <button onclick="toggleContent()">Show More</button>  <div id="more-content"> By jointly learning representations for supervised and unsupervised tasks and then ranking unlabeled samples by their nearness to the data manifold, we are able to identify the most relevant training samples to be labeled by the interpreter in each training round. This is shown in the figure below. On the popular F3 dataset, we obtain close to 10 percentage point difference in terms of interpretation accuracy between the proposed method and the baseline with only three fully annotated seismic sections.</div>
<h4 style="margin: 0px 10px 10px;">Results</h4>
<h4 style="margin: 0px 10px 10px;">Codes</h4>
<h4 style="margin: 0px 10px 10px;">Related Publications</h4>


<h3 style="margin: 10px 10px 10px;">Active Learning</h3>
<img src="./assets/teaser/geo-weight-share.png" class="teaser img-fluid z-depth-1" style="width=100%;height=100%">
I talk about this project here



<script>
    // JavaScript function to toggle the visibility of additional content
    function toggleContent() {
        var moreContent = document.getElementById("more-content");
        var button = document.querySelector("button");

        // Toggle the display property of the additional content
        if (moreContent.style.display === "none") {
            moreContent.style.display = "block";
            button.textContent = "Show Less";
        } else {
            moreContent.style.display = "none";
            button.textContent = "Show More";
        }
    }
</script>



