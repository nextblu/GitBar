<template>
    <div>
        <nav class="top-bar">
            <div class="level">
                <div class="buttons">
                    <b-taglist attached>
                        <b-tag>Connected</b-tag>
                    </b-taglist>
                </div>
                <div class="icon">
                    <img src="logo-white.png" alt="logo">
                </div>
                <div class="gh-project-logo">
                    <b-taglist attached>
                        <b-tag type="is-dark">GitBar</b-tag>
                        <b-tag type="is-info">0.0.1</b-tag>
                    </b-taglist>
                </div>
            </div>

        </nav>
    </div>
</template>

<script>
    export default {
      name: 'Topbar.vue'
    }
</script>

<style scoped>
    .top-bar {
        position: fixed;
        top: 0;
        width: 100%;
        height: 50px;
        background-color: #24292e;
        justify-content: center;
        flex-shrink: 0;
        z-index: 2;
        display: table-cell;
        vertical-align: middle;

    }

    .icon {
        display: block;
        margin-left: auto;
        margin-right: auto;
    }

    .buttons {
        position: relative;
        top: 50%;
        transform: perspective(1px) translateY(+50%);
    }

    .level {
        margin-right: 20px;
        margin-left: 20px;
    }

</style>