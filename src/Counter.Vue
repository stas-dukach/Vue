<template>
    <div>
    <h1>Counter: {{count}} </h1>
    <button @click="add"> Add </button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            count: 0
        }
    },
    methods: {
            add () {
            this.count = this.count + 1
        }
        }
}
</script>