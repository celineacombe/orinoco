<template>
  <b-card
    :title="teddy.name"
    :img-src="teddy.imageUrl"
    img-alt="Image"
    img-top
    img-height="206px"
    img-width="316px"
    tag="article"
    style="max-width: 20rem;"
    class="mb-2 teddyImage text-center"
  >
    <b-card-text>
      {{teddy.description}}
      <br />
      {{formatedPrice}}
    </b-card-text>

    <b-button :to="'/detail/'+teddy._id" variant="primary">Voir cet article</b-button>
  </b-card>
</template>

<script>
// import axios from 'axios'
import {formatPrice} from '@/functions'
export default {
name: 'Product',
props:{teddy:{
  type: Object
}},
data () {
      return {
    
      }},
computed: {
formatedPrice () {
  return formatPrice(this.teddy.price)
}
},
    
  methods: {
      //goToDetail(): 
  }
}
</script>

<style>
</style>