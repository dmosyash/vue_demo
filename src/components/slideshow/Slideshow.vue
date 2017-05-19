
<template src="./template.html"></template>

<script>
  import { Carousel, CarouselItem } from 'vue-l-carousel'

  var list1 = [
    {
      url: 'url1'
    },
    {
      url: 'url2'
    },
    {
      url: 'url3'
    }
  ]

export default {
    name: 'slideshow',
    data () {
      return {
        images: ['http://i.imgur.com/vYdoAKu.jpg', 'http://i.imgur.com/PUD9HQL.jpg', 'http://i.imgur.com/Lfv18Sb.jpg', 'http://i.imgur.com/tmVJtna.jpg', 'http://i.imgur.com/ZfFAkWZ.jpg'],
        list: list1
      }
    },
    components: {
      'carousel': Carousel,
      'carousel-item': CarouselItem
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

