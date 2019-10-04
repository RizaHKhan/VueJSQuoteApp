<template>
    <div>
        <h1 
        v-for="quote in quoteArray"
        @click="removeQuote($event)"
        >{{quote}}</h1>
    </div>
</template>

<script>
export default {
    props: ['quoteArray'],
    methods: {
    removeQuote(e) {
       
        this.quoteArray.splice(this.quoteArray.indexOf(e.target.innerHTML, 0), 1)
        
    }
  }
}
</script>

<style scoped>
    
</style>