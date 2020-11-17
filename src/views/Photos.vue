<template>
  <div>
    <h2>Photos view</h2>
    <h5>Photos Gallery</h5>
    <router-link v-for="(item,index) of photos" :to="{name: 'Photos' , params: { id: item}}" :key="index"><button class="btn btn-danger mx-2 my-3">{{item}}</button></router-link>
    <photo class="mb-5"></photo>
    <button @click="goBefore" class="btn btn-primary">Go Before</button>
    <button @click="home" class="btn btn-success mx-5">Go to Home</button>
    <button @click="goNext" class="btn btn-warning">Go Next</button>
  </div>
</template>
<script>
import Photo from "@/components/Photo";

export default {
  name: 'Photos',
  components: {
    Photo
  },
  data(){
    return {
      photos: [1,2,3,4,5,6]
    }
  },
  methods: {
    home(){
      this.$router.push('/')
    },
    goBefore(){
      this.$router.go(-1)
    },
    goNext(){
      this.$router.go(1)
    }
  }
}
</script>