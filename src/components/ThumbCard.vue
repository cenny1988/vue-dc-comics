<template>
  <div class="thumb">
    <img :src="details.thumb" alt="details.series">
    <h4>{{details.series}}</h4>
  </div>
</template>

<script>
export default {
  name: 'ThumbCard',
  props: {
      details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.thumb{
    width: calc(100% / 6);
    padding: 5px;
    img{
        max-width: 100%;
    }
    h4{
        padding: .8rem 0;
    }
}
</style>
