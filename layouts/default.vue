<template>
  <v-app>
    <v-main>
  	<SideBar  />
    <nuxt/>
  </v-main>
  </v-app> 
</template>

<script>
	
	import SideBar from "~/components/basics/sidebar"
  export default {
    data() {
      return{

      }
    },
    components:{
    	SideBar
    }
  }
</script>
