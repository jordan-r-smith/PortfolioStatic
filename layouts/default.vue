<template>
    <div>
        <nuxt />
        <div id="backToTop" class="button is-large" v-on:click="moveTo()">
            <span class="icon">
                <fa :icon="['fas', 'chevron-up']" />
            </span>
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
    background: #7091b9;
    border-radius: 6px;
    opacity: 0.5;
    transition: opacity 200ms ease-in;
}

#backToTop:hover {
    background: #7091b9;
    opacity: 1;
}
</style>
