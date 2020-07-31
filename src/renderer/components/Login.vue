<template>
    <div class="page">

        <section class="loading" v-if="isLoading">
            <b-skeleton width="20%" ></b-skeleton>

            <b-skeleton width="40%" ></b-skeleton>

            <b-skeleton width="80%" ></b-skeleton>

            <b-skeleton></b-skeleton>
            <b-skeleton width="32%" ></b-skeleton>

            <b-skeleton width="44%" ></b-skeleton>

            <b-skeleton width="98%" ></b-skeleton>

            <b-skeleton></b-skeleton>
            <b-skeleton width="14%" ></b-skeleton>

            <b-skeleton width="77%" ></b-skeleton>

            <b-skeleton width="7%" ></b-skeleton>

            <b-skeleton></b-skeleton>
            <b-skeleton width="20%" ></b-skeleton>

            <b-skeleton width="40%" ></b-skeleton>

            <b-skeleton width="70%" ></b-skeleton>

            <b-skeleton></b-skeleton>
            <b-skeleton width="20%" ></b-skeleton>

            <b-skeleton width="25%" ></b-skeleton>

            <b-skeleton width="80%" ></b-skeleton>

            <b-skeleton></b-skeleton>

        </section>
        <div class="modal-card" style="width: auto" v-else>
            <header class="modal-card-head">
                <p class="modal-card-title">Login</p>
            </header>
            <section class="modal-card-body">
                <b-field label="Email">
                    <b-input
                            type="email"
                            :value="email"
                            placeholder="Your email"
                            required>
                    </b-input>
                </b-field>

                <b-field label="Password">
                    <b-input
                            type="password"
                            :value="password"
                            password-reveal
                            placeholder="Your password"
                            required>
                    </b-input>
                </b-field>

            </section>
            <footer class="modal-card-foot">
                <button class="button is-primary" @click="$router.push({name:'home-page'})">Login</button>
            </footer>
        </div>
    </div>
</template>

<script>
    export default {
      name: 'Login',
      data () {
        return {
          isLoading: false,
          email: '',
          password: ''
        }
      }
    }
</script>

<style scoped>
    .loading {
        padding: 20px;
    }
    .login-page {
        padding: 20px;
        min-height: 100vh;
        min-width: 100%;
        display: block;
        position: relative;

    }

</style>