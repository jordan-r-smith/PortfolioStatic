<template>
    <section class="section container">
        <div class="columns is-vcentered">
            <div class="column is-half">
                <h2 class="title title-accent">
                    {{project.name}}
                    <small class="subtitle">{{project.date}}</small>
                </h2>
            </div>
            <div class="column is-half">
                <div class="tags float-right">
                    <template v-for="(tag, index) in project.tags">
                        <span :class="['tag', tag.class]" :key="index">{{tag.name}}</span>
                    </template>
                </div>
            </div>
        </div>
        <div class="columns">
            <div class="column content">
                <p>{{project.description}}</p>
                <div class="buttons">
                    <template v-for="(link, index) in project.links">
                        <a class="button is-dark" :href="link.url" :key="index">{{link.text}}</a>
                    </template>
                </div>
            </div>
            <div class="column is-narrow">
                <a :href="project.imageLink">
                    <img :src="project.imageSrc" :alt="project.name" loading="lazy" />
                </a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: ["project"]
};
</script>

<style>
img {
    border: 2px solid #ddd;
    border-radius: 6px;
    transition: opacity 300ms ease-out, border 300ms ease-out;
    width: 100%;
}

img:hover {
    opacity: 0.8;
    border: 2px solid #aaa;
}

@media only screen and (min-width: 992px) {
    .float-right {
        float: right !important;
    }
}
</style>
