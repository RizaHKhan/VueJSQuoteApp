<template>
  <div>
    <div class="counter-container">
        <Counter
        :quoteArray='quoteArray' 
        v-if="quoteArray"        
                />
      </div>
      <textarea 
      v-model="newQuote"
      />

    <button
      @click="addQuote(newQuote)"
    >Add Quote</button>

    <Display :quoteArray="quoteArray"/>
  </div>
</template>

<script>
import Counter from './Counter.vue'
import Display from './Display.vue'

export default {
  name: 'Main',
  data() {
    return{
      newQuote: '',
      quoteArray: [],
      
    }
  },
  computed: {
    
  },
    components: {
      Counter,
      Display,
  },
  methods: {
    addQuote(data) {
      if(data == '') {
        alert('Please enter a quote')
      } else {
        if(this.quoteArray.length == 10) {
          alert('Delete a quote to add another')
        } else {
            this.quoteArray.push(data)
     this.counter = this.quoteArray.length
     this.newQuote = '' 
     this.newQuote.focus()
        }

     }
      
    },
  }}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.counter-container {
  border: solid 1px red;
  height: 200px;
}

</style>
