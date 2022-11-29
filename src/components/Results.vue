<template>
<p>Reaction timer: {{scr}} ms </p>
<p class="rank"> {{ rank }}</p>
</template>

<script>
  export default {
    props: ['scr'],
    data(){
      return { 
        rank: null
      }
    },
    mounted(){
      if (this.scr < 250 ) {
        this.rank = 'Ninja Fingers'
      } else if (this.scr < 400){
        this.rank = 'Rapid Reflexes' 
      } else {
        this.rank = 'Snail pace...'
      }
    }
  }
</script>
  <style>
    .rank {
      font-size: 1.4em;
      color: green;
      font-weight:bold;
    }
  </style>
