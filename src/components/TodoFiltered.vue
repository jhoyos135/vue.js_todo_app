<template>
    <div class="btn-group">
    <button class="btn btn-secondary" :class="{ active: filter == 'all' }" @click="changeFilter('all')">All</button>
    <button class="btn btn-secondary" :class="{ active: filter == 'active' }" @click="changeFilter('active')">Active</button>
    <button class="btn btn-secondary" :class="{ active: filter == 'completed' }" @click="changeFilter('completed')">Completed</button>
    </div>
</template>

<script>
export default {
    name: 'todo-filtered',
    data() {
        return {
            'filter': 'all',
        }
    },
    methods: {
        changeFilter(filter) {
            this.filter = filter
            eventBus.$emit('filterChanged', filter)
        }
    }
    
}
</script>
