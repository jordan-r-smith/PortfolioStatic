<template>
    <div>
        <nuxt />
        <div id="backToTop" class="button" v-on:click="moveTo()">
            <span class="">Back to Top</span>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        moveTo() {
            window.scroll({
                top: 0,
                left: 0,
                behavior: "smooth"
            });
        }
    }
};
</script>

<style>
body {
    font-size: 18px;
}

#backToTop {
    position: fixed;
    bottom: 2rem;
    right: 2rem;
    cursor: pointer;
    color: #ffffff;
    background: #c1d2e6;
    border-radius: 6px;
}

#backToTop:hover {
    background: #7091b9;
}
</style>
