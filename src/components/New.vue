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
        },
        destroyed() {
            console.log('New comp destroyed');
        },
        deactivated() {
            console.log('new comp deactivated');
        },
        activated() {
            console.log('new comp activated');
        }
	}
</script>

<style>
    
</style>