<template>
    <div class="SimpleCard">

        <div class="caption">
            <h2>{{caption || 'Unnamed Card'}}</h2>
        </div>

        <div class="description">
            <p>{{description}}</p>
        </div>

        <div class="illustration">
            <figure>
                <img src="../assets/illustrations/austria.svg" alt="Austria">
            </figure>
        </div>

    </div>
</template>

<script>

    // Define attributes for the component

    let props = [ 'caption', 'description' ]

    // Export

    export default {
        name: 'SimpleCard',
        props,
    }

</script>

<style>
    .SimpleCard {
        background-color: hsl(204, 22%, 55%);
        color:     black;

        display: grid;
        grid-template-areas:
            "Cap Ico"
            "Des Ico";
        grid-template-columns: auto max-content;
        grid-template-rows:    max-content auto;
    }
    .SimpleCard>.caption      { grid-area: Cap; }
    .SimpleCard>.description  { grid-area: Des; }
    .SimpleCard>.illustration { grid-area: Ico; }

    .SimpleCard .caption      { padding: 1em; padding-bottom: 0; }
    .SimpleCard .description  { padding: 1em; }
    .SimpleCard .illustration { padding: 1em; }
    .SimpleCard .illustration img {
        width:  10em;
        height: auto;
    }
    .SimpleCard h2,
    .SimpleCard p,
    .SimpleCard figure {
        margin:  0;
        padding: 0;
    }
</style>
