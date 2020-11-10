<template>
    <div class="CardGrid">

        <!-- Case A: Just display the component -->
        <simple-card/>


        <!-- Case B: Set attributes for component -->
        <simple-card
            caption="Caption from attribute"
            description="Description from attribute"
            />


       <!-- Case C: Use js variables as attributes -->
        <simple-card
            v-bind:caption="CustomCaption"
            v-bind:description="CustomDescription"
            />


        <!-- Case D: Repeat with array -->
        <simple-card
            v-for="card in ArrayWithCards"
            v-bind:caption="card.caption"
            v-bind:description="card.description"
            />

    </div>
</template>

<script>
// ---------------------------- define export

    let props       = []
    let components  = {}
    let methods     = {}
    let computed    = {}
    let watch       = {}
    let data        = {}

// ---------------------------- main logic


    // load component

    import SimpleCard from '@/components/SimpleCard.vue'
    components = { SimpleCard, ...components }


    // Case C: define some data for component

    const CustomCaption     = 'Caption from data'
    const CustomDescription = 'Description from data'
    data = {
        CustomCaption,
        CustomDescription,
    ...data }


    // Case D: create an array with cards

    const ArrayWithCards = [
        {
            caption:     'First card in Array',
            description: 'Some description',
        },
        {
            caption:     'Second card in Array',
            description: 'Some description',
        },
        {
            caption:     'Third card in Array',
            description: 'Some description',
        },
    ]
    data = {
        ArrayWithCards,
    ...data }


// ---------------------------- export ready

    export default {
        name: 'ExampleView-GridForSimpleCards',
        props,
        components,
        methods,
        computed,
        watch,
        data () { return data },
    }
// ---------------------------- end script
</script>

<style>
    .CardGrid {
        display: grid;
        grid-gap: 1em;
        padding:  1em;
        grid-template-columns: repeat( auto-fit, minmax(24em,1fr) );
    }
</style>
