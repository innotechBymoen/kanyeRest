<template>
    <div id="kanye-quote">
        <h2>{{quote}}</h2>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quote: "Click the button for more Kanye!"
            }
        },
        mounted: function() {
            this.$root.$on('newQuote', this.getNewQuote)
        },
        methods: {
            getNewQuote: function(){
                axios.get('/kanye-quote')
                .then(response => {
                    console.log(response);
                    this.quote = response.data.quote;
                })
                .catch(error => {
                    console.log(error);
                    this.quote = 'Error getting that sweet sweet Kanye Quote';
                });
            }
        }
    }
</script>

<style>
    #kanye-quote {
        max-width: 75vw;
    }
</style>
