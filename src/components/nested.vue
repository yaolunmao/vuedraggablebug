<template>
    <draggable class="dragArea" :tag="tag" :list="tasks" :group="{ name: 'g1' }" item-key="name" v-if="tasks.length>0">
    
        <template #item="{ element }">
            <nested-draggable :tasks="element.tasks" :tag="element.name"></nested-draggable>
        </template>
    </draggable>
    <component v-else :is="tag">Button</component>
</template>
<script>
import draggable from "vuedraggable/src/vuedraggable";
export default {
    props: {
        tasks: {
            required: true,
            type: Array
        },
        tag: {
            required: false,
            type: String,
            default: "div"
        }
    },
    components: {
        draggable
    },
    name: "nested-draggable"
};
</script>
<style scoped>
.dragArea {
}
</style>