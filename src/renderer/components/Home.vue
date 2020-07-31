<template>
    <div class="app">

        <div class="container is-fullhd">


            <b-message title="Default" aria-close-label="Close message">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
            </b-message>


        </div>
        <Navbar></Navbar>
    </div>
</template>

<script>
    import Navbar from './Home/Bottombar'
export default {
      name: 'home-page',
      components: {
        Navbar
      },
      data () {
        return {

        }
      },
      mounted () {
        this.$buefy.snackbar.open({
          message: 'Welcome back!',
          type: 'is-warning',
          position: 'is-bottom',
          indefinite: false
        })
      }
    }
</script>

<style scoped>

</style>