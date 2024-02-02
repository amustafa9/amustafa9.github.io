<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .toggleable-content {
            display: none;
            border: none;
            padding: 0px;
            margin: 0px;
        }

        .toggle-text {
            color: darkblue;
            cursor: pointer;
        }
    </style>
    <title>Show More Text</title>
</head>

<h1 id="software"></h1>
<h2 style="margin: 60px 0px 10px;">Software and Codes</h2>

<h3 style="margin: 0px 10px 10px 0px;">1. <a href="https://github.com/amustafa9/SeisWiz">amustafa9/SeisWiz</a></h3>
<img src="./assets/teaser/basic_mode_grayscale.gif" class="teaser img-fluid z-depth-1" style="width=100%;height=100%">
The ultimate lightweight Matplotlib-based seismic volume viewer with multi-view support and horizon visualization capabilities. 

<script>
    // JavaScript function to toggle the visibility of a specific element by ID
    function toggleContent(elementId) {
        var element = document.getElementById(elementId);

        if (element.style.display === "none") {
            element.style.display = "block";
            document.querySelector('.toggle-text').textContent = "Show less";
        } else {
            element.style.display = "none";
            document.querySelector('.toggle-text').textContent = "Show more";
        }
    }
</script>
