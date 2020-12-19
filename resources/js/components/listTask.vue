<template>
    <div>
        <!-- <list-item
                    :item="item"
                    class="item"
                    v-on:itemchanged="$emit('reloadList')"
                    /> -->
        <div v-for="(item, index) in items" :key="index">
                <list-thing
                    :item="item"
                    class="item"
                    v-on:itemchanged="$emit('reloadList')"
                    />
        </div>
    </div>
</template>

<script>
import listThing from "./listThing"
import ListThing from './listThing.vue'

export default {
    props: ['items'],
    components: {
        listThing
    }
}
</script>

<style scoped>
.item{
    background: #e6e6e6;
    padding: 5px;
    margin-top: 5px;
}
</style>