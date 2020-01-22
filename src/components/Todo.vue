<template>
<div>
    <div>counter</div>
   {{ getCount}} <br />
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
</div>
</template>

<script>
    import { mapGetters } from 'vuex'
export default {
  name: 'counter',
/*
  data(){
      return{
          counter: getCount()


      }
  },*/
    methods:{
      increment(){
          this.$store.dispatch('increment')


      },
        decrement(){
            this.$store.dispatch('decrement')

            alert('-')
        }
    },
    computed: {
        ...mapGetters([
            'getCount'
        ]),
    }

};
</script>
