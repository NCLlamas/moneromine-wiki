# moneromine-wiki
A Wiki covering all things Monero, Pools, &amp; Mining

## Project Overview
This project is scaffolded using a combination of Bootstrap, JQuery, and Alpine.js.

- Bootstrap provides the base styling and access to utility functions
- JQuery is currently supporting some of the base functions with the prebuilt Bootstrap sidebar
- Alpine.js handles the state management and reactive visibility of sections (AKA pages)

## Adding pages to the Wiki
Each page needs two things to be fully supported:
###1. A menu entry on the sidebar, following the model:
   
    <li :class="{ 'active': nav === 'section-id' }">
    <a class="scroll-link"  @click="nav = 'section-id'">New Page</a>
    </li>

where section-id is a unique identifier used by alpine.js to determine visibility with navigation.

###2. A section (aka page) following the model:

    <section x-show="nav === 'section-id'" class="section-1-container section-container" id="section-1">
        <div class="container">
            /* Enter whatever HTML your heart desires */
        </div>
    </section>

where the x-show value matches your unique identifier.

##Roadmap for future Improvements
There are a number of improvements that could happen once the content is solidified.
 - Eliminate unused JS remaining from the project this was sourced from
 - Add header links to the Discord, Twitter, Email, and Status
 - Do further work to match styles from main site to wiki site

This is just a starter! Hack away.
