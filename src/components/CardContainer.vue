<script setup>
import { ref } from 'vue';

const props = defineProps(["direction"]);

const container = ref(null);
const slot1 = ref(null);
const slot2 = ref(null);

let isResizing = false;

document.addEventListener('mousemove', ev => {
    if (isResizing) {
        const rect = container.value.getBoundingClientRect();

        const v = props.direction == 'column' ? ev.clientY : ev.clientX;
        const a = props.direction == 'column' ? rect.top : rect.left;
        const b = props.direction == 'column' ? rect.bottom : rect.right;
        
        const percent = Math.max(Math.min((v - a) / (b - a), 1), 0);

        slot1.value.style['flex-grow'] = percent;
        slot2.value.style['flex-grow'] = 1 - percent;
    }
})

document.addEventListener('mouseup', _ => isResizing = false)

</script>

<template>
    <div ref="container" id="container">
        <div ref="slot1" class="card">
            <slot name="1"></slot>
        </div>

        <div @mousedown="isResizing=true" id="separator"></div>

        <div ref="slot2" class="card">
            <slot name="2"></slot>
        </div>
    </div>
</template>

<style scoped>
#container {
    width: 100%;
    height: 100%;

    display: flex;
    flex-direction: v-bind('props.direction || "row"');
    align-items: stretch;

    flex: 1 1 auto;
}

#separator {
    flex: 0 0 8px;

    display: flex;
    flex-direction: v-bind('props.direction == "column" ? "row" : "column"');
    justify-content: center;
    align-items: center;

    cursor: v-bind('(props.direction == "column" ? "ns" : "ew") + "-resize"');
}

#separator::after {
    content: '';
    display: inline-block;

    width: 2px;
    height: 2px;
    flex-basis: 20px;

    border-radius: 1px;
    background-color: #313131;
}

#separator:hover::after {
    flex-basis: 100%;

    background-color: #1A90FF;
}

.card {
    width: 100%;
    height: 100%;

    flex: 1 1 0;
}
</style>