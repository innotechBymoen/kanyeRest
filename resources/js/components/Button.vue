<template>
    <div id="kanye-button" @click="requestQuote">
        <p><strong>Click For Kanye</strong></p>
    </div>
</template>

<script>
    export default {
        methods: {
             requestQuote: function() {
                this.$root.$emit('newQuote');
            }
        },
    }
</script>

<style>
    #kanye-button{
        box-shadow: 5px 5px 10px grey;
        transition: box-shadow 0.2s;
        padding: 2vh 4vw;
    }
    #kanye-button:hover {
        cursor: pointer;
    }
    #kanye-button:focus {
        box-shadow: 2px 2px 5px lightgray;
    }
    #kanye-button:active {
        box-shadow: 2px 2px 5px lightgray;
    }
</style>
