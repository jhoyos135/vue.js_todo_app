<template>
            <div> <label> <input class="mr-2" type="checkbox" :checked="!anyRemaining" @change="allChecked">Check All</label></div>
</template>

<script>
export default {
    name: 'todo-check-all',
    props: {
        anyRemaining: {
            type: Boolean,
            required: true
        }
    },
    methods: {
        allChecked() {
            eventBus.$emit('checkAllChanged', this.anyRemaining)
        }
    }
    
}
</script>
