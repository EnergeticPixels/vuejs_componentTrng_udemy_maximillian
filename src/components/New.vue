<template>
    <div>
        <h3>The new component</h3>
        <button @click='counter++'>Increase</button>
        <p>{{ counter }}</p>
    </div>
</template>

<script>
    console.log('from inside quote');
	export default {
        data: function() {
            return {
                counter: 0
            };
        }
	}
</script>

<style>
    
</style>