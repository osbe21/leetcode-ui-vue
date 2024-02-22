<script setup>

</script>

<template>
<div id="container">
    <div id="tab">
        <slot name="icon">Icon</slot>
        <slot name="title">Title</slot>
    </div>
    <div id="content">
        <slot name="content"></slot>
    </div>
</div>
</template>

<style scoped>
#container {
    display: flex;
    flex-direction: column;

    width: 100%;
    height: 100%;

    border-radius: 8px;

    overflow: hidden;

    background-color: #262626;
}

#tab {
    flex: 0 0 auto;

    display: flex;
    align-items: center;
    gap: 6px;

    padding: 4px;
    padding-left: 12px;
    height: 36px;

    background-color: #333333;
    
    font-size: 0.875rem;
    font-weight: 500;
}

#content {
    flex: 1 1 0;
    
    width: 100%;
    height: 100%;
}
</style>