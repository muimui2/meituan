<template>
  <div class="invitebar">
        <div class="invite">
          <img :src=inviteImg alt="">
      </div>
  </div>
</template>

<script>
export default {
  props: {
  },
  data () {
    return {
        inviteImg:'https://picsum.photos/500/500.jpg',
    }
  },
  created () {},
  mounted () {},
  watch: {},
  computed: {},
  methods: {},
  components: {},
}
</script>
<style>

.invite{
    height: 100px;
    margin: 12px 0;
    overflow: hidden;
    border-radius: 10px;
}

</style>