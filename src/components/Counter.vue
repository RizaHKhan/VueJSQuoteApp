<template>
   <div>
       <div class="container"><p class="percentage">{{quoteArray.length * 10 }}%</p>
           <div class="percent" v-bind:style="{width: quoteArray.length*10 + '%'}"></div>
       </div>
   </div>
</template>

<script>
export default {

    // here we receive the value
    props: ['quoteArray'],
    data() {
        return {
        }
    }
}
</script>

<style scoped>
    
    .container {
        margin: 0;
        padding: 0;
        border: solid 1px red;
        height: 30px;
        width: 50%;
        margin: 4em auto;
        font-size: 2rem;
        text-align: center;
        position: relative;
    }

    .percentage {
        position: absolute;
        margin: 0 auto;
    }

    .percent {
        height: 100%;
        transition: all .3s ease-in-out;
        background: red;
    }  
</style>