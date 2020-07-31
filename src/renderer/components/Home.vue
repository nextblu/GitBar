<template>
    <div class="app">
        <Topbar></Topbar>

        <div v-if="loading">
            <div class="container is-fluid">

                <section class="loadeing-animation">
                    <article class="media" v-for="i in media" :key="i">
                        <figure class="media-left">
                            <p class="image is-64x64">
                                <b-skeleton circle width="64px" height="64px"></b-skeleton>
                            </p>
                        </figure>
                        <div class="media-content">
                            <div class="content">
                                <p>
                                    <b-skeleton active></b-skeleton>
                                    <b-skeleton  height="80px"></b-skeleton>
                                </p>
                            </div>
                            <nav class="level is-mobile">
                                <div class="level-left">
                                    <a class="level-item">
                                <span class="icon is-small">
                                    <b-skeleton></b-skeleton>
                                </span>
                                    </a>
                                    <a class="level-item">
                                <span class="icon is-small">
                                    <b-skeleton></b-skeleton>
                                </span>
                                    </a>
                                </div>
                            </nav>
                        </div>
                    </article>
                </section>
            </div>
        </div>
        <div v-else>
            <section>
                <article class="media">
                    <figure class="media-left">
                        <p class="image is-64x64">
                            <img class="is-rounded" src="logo.png">
                        </p>
                    </figure>
                    <div class="media-content">
                        <div class="content">
                            <p>
                                Corpo del testo della notifica
                            </p>
                        </div>
                        <nav class="level is-mobile">
                            <div class="level-left">
                                <a class="level-item">
                                <span class="icon is-small">
                                    <b-icon
                                            icon="account"
                                            size="is-small">
                                    </b-icon>
                                </span>
                                </a>
                                <a class="level-item">
                                <span class="icon is-small">
                                    <b-icon
                                            icon="account"
                                            size="is-small">
                                    </b-icon>
                                </span>
                                </a>
                            </div>
                        </nav>
                    </div>
                </article>
            </section>

        </div>


        <Navbar></Navbar>
    </div>
</template>

<script>
    import Navbar from './Home/Bottombar'
    import Topbar from './Home/Topbar'
export default {
      name: 'home-page',
      components: {
        Navbar,
        Topbar
      },
      data () {
        return {
          loading: true,
          media: 7
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
    .media {
        padding: 40px;
    }
    .loadeing-animation {
        margin-top: 40px;
    }

</style>