<script setup>

</script>

<template>
<div id="container">
    <div id="buttons">
        <button>
            <i class="fa-solid fa-bug" style="color: #FFD43B;"></i>
        </button>
        <button>
            <i class="fa-solid fa-play" style="color: #A7A7A7;"></i>
            Run
        </button>
        <button>
            <i class="fa-solid fa-cloud-arrow-up" style="color: #44b52d;"></i>
            <span style="color: #44b52d;">Submit</span>
        </button>
    </div>
</div>
</template>

<style scoped>
#container {
    flex: 0 0 auto;

    padding: 4px 0;
    height: 40px;

    display: flex;
    justify-content: center;
    align-items: stretch;
}

#buttons {
    display: flex;
    gap: 2px;

    width: min-content;

    overflow: hidden;

    border-radius: 5px;
}

#buttons button {
    display: flex;
    align-items: center;
    gap: 10px;

    padding: 6px 12px;

    outline: none;
    border: none;
    border-radius: 0;

    background-color: #222222;

    cursor: pointer;

    color: #f5f5f5;
    font-family: "-apple-system","BlinkMacSystemFont","Segoe UI","Helvetica","Arial","sans-serif","Apple Color Emoji","Segoe UI Emoji";
    font-size: 14px;
    font-weight: 500;
}

#buttons button:hover {
    background-color: #2F2F2F;
}
</style>