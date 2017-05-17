
<template src="./template.html"></template>

<script>

export default {
  name: 'slideshow',
  data () {
    return {
      images: ['http://i.imgur.com/vYdoAKu.jpg', 'http://i.imgur.com/PUD9HQL.jpg', 'http://i.imgur.com/Lfv18Sb.jpg', 'http://i.imgur.com/tmVJtna.jpg', 'http://i.imgur.com/ZfFAkWZ.jpg'],
      currentNumber: 0
    }
  },

  mounted: function () {
    this.startRotation()
  },

  methods: {
    startRotation: function () {
      this.timer = setInterval(this.next, 3000)
    },

    stopRotation: function () {
      clearTimeout(this.timer)
      this.timer = null
    },

    next: function () {
      this.currentNumber += 1
    }
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

