---
layout: page
title: Interest
permalink: /interest/
---

{% include nav/mourn.html %}


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



### My interest: Storytelling in videogames
I love storytelling throughout any medium, but using videogames to tell a compelling story is one of my favorites. The examples I shall gush about on this page are: Hades, Celeste, Breath of the Wild / Tears of the Kingdom, and Bloodborne.

## Hades

Hades is a rogue-like hack and slash game where you play as Zagreus, son of Hades. Your goals is to go through 4 different zones with bosses at the end to escape your father's domain and go to olympus. The game is thrilling and has an amazing gameplay loop, but the best part about it is arguably the story.

The story of Hades is given to you in small portions throughout a given run, when you encounter npcs who give you perks, and a piece of their story. When you inevitably die before escaping the underworld, you go to Hades' abode, where other characters dwell as well, coming and going as you progress the game. The story is perfectly combined with the main gameplay to give an amazing experience overall. This gives the game's story *Balance*.

## Celeste

Celeste is a grueling 2d platformer with an emphasis on precision and endurance. In  Celeste, you climb Mount Celeste, a mountain where strange things happen the farther up you go. It is a game about conquering hardships and accepting yourself.

Celeste's story is beautiful, and tackles serious topics from the developers' lives. The story has *Heart*.

## Breath of the Wild / Tears of the Kingdom

Breath of the Wild and Tears of the Kingdom (from now on shortened to botw and totk) are the latest installments to the Legend of Zelda franchise. They are open world rpgs where you fight enemies and solve puzzles in a massive world, and the story is weaved into this world. 

Between botw and totk, there is a time skip of about 5-10 years. When you return to hyrule in totk, you get to see how the world has changed. This gives the world a level of *Realism*.

## Bloodborne

Bloodborne is a gruesome game. It is a punishing, violent, gruesome game. It also happens to be one of the greatest cosmic horrors ever made. The initial asthetic is that of misformed monsters that were once human, going on a wild witch hunt of sorts, with you as their target. 

The game leads you to believe that this game is simply about human conflicts. But this game's story has depth to it. The source of this corruption of humanity is an eldritch race of gods called *Great Ones*. Throughout the game, you never see more than a handful of them within the game, but their prescence is notable from the very begginning. This game has *Depth*.

<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/Bloodborne.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/botw.jpg" alt="Image 2">
 <img src="{{site.baseurl}}/images/about/totk.jpeg" alt="Image 3">
 <img src="{{site.baseurl}}/images/about/Stardew.jpg" alt="Image 4">
 <img src="{{site.baseurl}}/images/about/hades.jpeg" alt="Image 5">
 <img src="{{site.baseurl}}/images/about/celeste.png" alt="Image 6">
</div>
