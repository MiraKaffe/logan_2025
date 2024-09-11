---
layout: page
title: Interest
permalink: /interest/
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

### My interest: Storytelling in videogames
I love storytelling throughout any medium, but using videogames to tell a compelling story is one of my favorites. The examples I shall gush about on this page are: Hades, Celeste, Breath of the Wild / Tears of the Kingdom, and Bloodborne.

## Hades

Hades is a rogue-like hack and slash game where you play as Zagreus, son of Hades. Your goals is to go through 4 different zones with bosses at the end to escape your father's domain and go to olympus. The game is thrilling and has an amazing gameplay loop, but the best part about it is arguably the story.

The story of Hades is given to you in small portions throughout a given run, when you encounter npcs who give you perks, and a piece of their story. When you inevitably die before escaping the underworld, you go to Hades' abode, where other characters dwell as well, coming and going as you progress the game. The story is perfectly combined with the main gameplay to give an amazing experience overall. This gives the game's story balance.

## Celeste

Celeste is a grueling 2d platformer with an emphasis on precision and endurance. In  Celeste, you climb Mount Celeste, a mountain where strange things happen the farther up you go. It is a game about conquering hardships and accepting yourself.

Celeste's story is beautiful, and tackles serious topics from the developers' lives. The story has heart.

## Breath of the Wild / Tears of the Kingdom

Breath of the Wild and Tears of the Kingdom (from now on shortened to botw and totk) are the latest installments to the Legend of Zelda franchise. They are open world rpgs where you fight enemies and solve puzzles in a massive world, and the story is weaved into this world. 

Between botw and totk, there is a time skip of about 5-10 years. When you return to hyrule in totk, you get to see how the world has changed. This gives the world a level of realism.

## Bloodborne


<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/babel.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/Bloodborne.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/Truman.jpg" alt="Image 3">
 <img src="{{site.baseurl}}/images/about/run.jpg" alt="Image 4">
     <img src="{{site.baseurl}}/images/about/Stardew.jpg" alt="Image 5">
</div>
