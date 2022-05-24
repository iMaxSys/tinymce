<script setup>
import { ref, onMounted } from "vue";
import "./tinymce.min.js";
import "./themes/silver/theme.min.js";
import "./icons/default/icons.min.js";
import "./models/dom/model.min.js";
import "./plugins/preview/plugin.min.js";
import "./plugins/table/plugin.min.js";
import "./langs/zh-Hans.js";
onMounted(() => {
  tinymce.init({
    selector: "#tinymce-editor",
    language: "zh-Hans",
    base_url: "/tinymce",
    plugins: "preview table",
  });
});
</script>

<template>
  <section id="tinymce-editor">it's me.</section>
</template>

<style lang="scss" scoped>
@import url("./skins/ui/oxide/skin.min.css");
</style>
