<template>
    <DefaultLayout>
        <NuxtPage />
    </DefaultLayout>
</template>

<script setup lang="ts">
    import DefaultLayout from "~/layouts/default.vue";
    import "@kestra-io/ui-libs/style.css";

    String.prototype.capitalize = function () {
        return this.charAt(0).toUpperCase() + this.slice(1)
    }

    useHead({
        htmlAttrs: {
            lang: "en",
            class: "dark",
        },
        link: [
            {
                rel: "icon",
                type: "image/png",
                href: "/favicon-192x192.png",
            },
        ],
        titleTemplate: (titleChunk) => {
            return titleChunk &&
                titleChunk != "Kestra, Open Source Declarative Data Orchestration"
                ? `${titleChunk}`
                : "Kestra, Open Source Declarative Data Orchestration";
        },
    });
</script>

<style lang="scss">
.text-gradient {
    background: var(
        --Text_gradient,
        linear-gradient(90deg, #e151f7 2%, #5c47f5 65%)
    );
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
</style>
