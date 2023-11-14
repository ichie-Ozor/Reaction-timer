<template>
   <div @end="endPlay">
       <p>Reaction time - {{ show }} ms</p>
       <p class="rank">{{ rank }}</p>
   </div>
</template>

<script>
export default {
    name: "Result",
    props: ['show'],
    data(){
        return {
            rank: null
        }
    },
    mounted(){
        if(this.show < 250) {
            this.rank = 'Ninja finger'
        } else if (this.show < 400) {
            this.rank = 'Rapid Reflexes'
        } else  {
            this.rank = 'Snail pace...'
        }
    }
}
</script>
<style>
.rank{ 
    font-size: 1.4rem;
    color: #0faf87;
    font-weight: bold;
    }
</style>