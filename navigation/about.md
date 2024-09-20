---
layout: post
title: About
permalink: /about/
---

<style>
    /* Style looks pretty compact, trace grid-container and grid-item in the code */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

      .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is for the CSS styling, the id is for JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - for now"},
        {"flag": "b/b9/Flag_of_Oregon.svg", "greeting": "Hi", "description": "Oregon - never"},
        {"flag": "b/be/Flag_of_England.svg", "greeting": "Alright mate", "description": "England - many trips"},
        {"flag": "e/ef/Flag_of_Hawaii.svg", "greeting": "Aloha", "description": "Hawaii - never"},
    ]; 
   
    
    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

## Interests and Disenterests 
I enjoy playing games and reading books. My favorite books are the Mistborn trilogy, Babel, Priory of the Orange Tree, and The Invisible Life of Addie La Rue. I enjoy fantasies and science fictions. I also enjoy playing video games, and my favorite is Bloodborne. Some of my other favorite games include Celeste, Neon White(top 2k on global leaderboard), Stardew Valley, and Breath of the Wild. My favorite movie is The Truman Show(excluding lord of the rings). My favorite food is Lumpia, and I've run a 25k before (and hopefully a marathon by the end of the year).

My favorite subject is English, and I have a terrible memory most of the time.

I went to Monterey Ridge for elementary school, Oak Valley for middle, and am in Del Norte. I played soccer for about ~5 years before giving up and trail running instead.


I do not enjoy sports outside of running, I find coding painful, and I dislike noise.


<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/babel.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/Bloodborne.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/Truman.jpg" alt="Image 3">
 <img src="{{site.baseurl}}/images/about/run.jpg" alt="Image 4">
     <img src="{{site.baseurl}}/images/about/Stardew.jpg" alt="Image 5">
</div>


<script src="https://utteranc.es/client.js"
        repo="nighthawkcoders/portfolio_2025"
        issue-term="title"
        label="blogpost-comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>

