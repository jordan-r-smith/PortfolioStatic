<template>
    <div>
        <section class="hero">
            <div class="hero-body container">
                <h1 class="title is-1">
                    <span class="title-accent">Jordan</span> Smith
                </h1>

                <!-- About -->
                <p class="content">
                    I am a web developer located in Roswell, Georgia and am interested in developing functional and elegant code. I have
                    experience developing applications in Angular, DotNet, Rails, TypeScript, HTML, CSS and Java. You can contact me
                    using any of the links below.
                </p>
                <!-- /About -->

                <!-- Social -->
                <div class="columns social-media is-mobile">
                    <div class="column">
                        <a href="https://github.com/jordan-r-smith">
                            <fa :icon="['fab', 'github']" class="fa-4x" />
                        </a>
                    </div>
                    <div class="column">
                        <a href="https://www.linkedin.com/in/jordanrsmith">
                            <fa :icon="['fab', 'linkedin']" class="fa-4x" />
                        </a>
                    </div>
                    <div class="column">
                        <a href="mailto:jordan.r.smith@gmail.com">
                            <fa :icon="['fas', 'envelope']" class="fa-4x" />
                        </a>
                    </div>
                </div>
                <!-- /Social -->
            </div>
        </section>

        <div v-for="(project, index) in projects" :key="index">
            <showcase :project="project" />
        </div>

        
    </div>
</template>

<script>
import showcase from "~/components/showcase";
import projects from "~/data/projects.json";

export default {
    components: {
        showcase
    },
    asyncData({ params }) {
        return { projects };
    }
};
</script>

<style>
.hero {
    background-color: #7091b9;
    color: #fff;
}

.title.is-1 {
    color: #fff;
}

.hero-body p {
    font-size: 20px;
    font-weight: 400;
}

.title-accent {
    color: #283c54;
}

.social-media {
    margin: 10px 0 5px 0;
    text-align: center;
}

.social-media a {
    color: #fff;
    transition: color 300ms ease-out;
}

.social-media a:hover {
    color: #283c54;
}
</style>
