<script setup>
import Card from './Card.vue'
</script>

<template>
    <Card>
        <template #icon>
            <i class="fa-regular fa-file-lines" style="color: #2b69d4;"></i>
        </template>

        <template #title>
            <span>Description</span>
        </template>

        <template #content>
            <div id="content">
                <h1 id="title">3. Longest Substring Without Repeating Characters</h1>

                <div id="tag-container">
                    <span class="tag" style="color: rgb(31, 211, 31);">
                        Easy
                    </span>
                    <span class="tag">
                        <i class="fa-solid fa-tag" style="color: #fafafa;"></i>
                        Topics
                    </span>
                </div>

                <p id="description">
                    Given a string s, find the length of the longest substring without repeating characters.
                </p>

                <br>

                <div class="example-container">
                    <h3>Example 1:</h3>
                    <div class="example-content">
                        <p><b>Input:</b> s = 2</p>
                        <p><b>Output:</b> 4</p>
                        <p><b>Explanation:</b> Fordi s er 2 og noe sånt er svaret 4</p>
                    </div>
                </div>
            </div>
        </template>
    </Card>
</template>

<style scoped>
#content {
    padding: 20px 16px;

    display: flex;
    flex-direction: column;
    gap: 1rem;
}

#title {
    font-size: 24px;
    font-weight: 600;
}

#tag-container {
    height: 24px;

    display: flex;
    gap: 0.25rem;
}

.tag {
    padding: 4px 8px;
    height: 100%;

    border-radius: 12px;

    background-color: #3C3C3C;

    font-size: 12px;
}

#description {
    font-size: 14px;
}


.example-container h3 {
    margin: 16px 0;

    font-size: 14px;
    font-weight: 700;
}

.example-content {
    padding-left: 16px;

    border-left: #454545 2px solid;

    font-family: sans-serif;
    line-height: 1.25rem;
}

</style>