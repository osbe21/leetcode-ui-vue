<script setup>

import { ref } from 'vue';
import Card from './Card.vue';

import { PrismEditor } from 'vue-prism-editor';
import 'vue-prism-editor/dist/prismeditor.min.css';

import { highlight, languages } from 'prismjs/components/prism-core';
import 'prismjs/components/prism-clike';
import 'prismjs/components/prism-javascript';
import 'prismjs/themes/prism-vsc-dark-plus.css';

const code = ref('\n//console.log the result\nfunction twoSum(nums, k) {\n\tconsole.log("Hello world");\n}\n');

const highlighter = (code) => highlight(code, languages.js);


</script>

<template>
<Card>
    <template #icon>
        <i class="fa-solid fa-code" style="color: #20b138;"></i>
    </template>

    <template #title>
        <span>Code</span>
    </template>

    <template #content>
        <prism-editor id="editor" v-model="code" :highlight="highlighter" line-numbers></prism-editor>
    </template>
</Card>
</template>

<style scoped>
#editor {
    /* we dont use `language-` classes anymore so thats why we need to add background and text color manually */
    background: #262626;
    color: #ccc;

    /* you must provide font-family font-size line-height. Example: */
    font-family: "Fira code", "Fira Mono", Consolas, Menlo, Courier, monospace;
    font-size: 14px;
    line-height: 1.5;
    padding: 5px;
}
  
/* optional class for removing the outline */
#editor:deep() .prism-editor__textarea:focus {
    outline: none;
}

#editor:deep() .prism-editor__line-numbers {
    color: #858585;
}
</style>