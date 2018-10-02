<template>
     <div>{{ remaining }} items left</div>
</template>

<script>
export default {
    name: 'todo-remaining',
    props: {
        remaining: {
            type: Number,
            require: true
        }
    }
}
</script>

