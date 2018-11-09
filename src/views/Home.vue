<template>
  <div class="home">
    <app-homelayout msg="This is home layout"/>
    <app-footer></app-footer>
  </div>
</template>

<script>
// @ is an alias to /src
import homelayout from '@/components/homelayout.vue'
import footer from '@/components/footer.vue'


export default {
  name: 'home',
  components: {
    'app-homelayout': homelayout,
    'app-footer': footer
  }
}
</script>
