---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some places I have lived.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
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

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // Clear the output
outputElement.innerHTML = '';

// Data array
const living_in_the_world = [
  {flag: "https://upload.wikimedia.org/wikipedia/commons/0/01/Flag_of_California.svg", greeting: "Hey", description: "California - forever"},
  {flag: "https://upload.wikimedia.org/wikipedia/commons/b/b9/Flag_of_Oregon.svg", greeting: "Hi", description: "Oregon - 9 years"},
  {flag: "https://upload.wikimedia.org/wikipedia/commons/b/be/Flag_of_England.svg", greeting: "Alright mate", description: "England - 2 years"},
  {flag: "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Flag_of_the_United_States_%281912-1959%29.svg/960px-Flag_of_the_United_States_%281912-1959%29.svg.png?20251108224147", greeting: "Aloha", description: "Hawaii - 2 years"}
];

// Create a div container with id
const container = document.createElement('div');
container.id = 'grid_container';

// Style the container 
container.style.border = '2px solid';
container.style.padding = '10px';

// Grid specific styles
container.style.display = 'grid';
container.style.gridTemplateColumns = 'repeat(auto-fill, minmax(150px, 1fr))';
container.style.gap = '10px';

// Loop through data and create grid items
for (const location of living_in_the_world) {
  // Create grid item
  const gridItem = document.createElement('div');
  gridItem.style.textAlign = 'center';
  
  // Create a flag image
  const img = document.createElement('img');
  img.src = location.flag;
  img.alt = location.description + ' Flag';
  img.style.width = '100%';
  img.style.height = '100px';
  img.style.objectFit = 'contain';
  
  // Create a description
  const description = document.createElement('p');
  description.textContent = location.description;
  description.style.margin = '5px 0';
  description.style.fontWeight = 'bold';
  
  // Create a greeting
  const greeting = document.createElement('p');
  greeting.textContent = location.greeting;
  greeting.style.margin = '5px 0';
  greeting.style.fontStyle = 'italic';
  greeting.style.opacity = '0.7';
  
  // Add all elements to grid item
  gridItem.appendChild(img);
  gridItem.appendChild(description);
  gridItem.appendChild(greeting);
  
  // Add grid item to container
  container.appendChild(gridItem);
}

// Add containter to output 
outputElement.appendChild(container);
</script>

### Journey through Life
moved from Portland, Oregon in 2021
joined Boyscouts in 2022 to present
