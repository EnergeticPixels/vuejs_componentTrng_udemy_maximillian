<template>
    <div class='container'>
      <div class='row'>
        <div class='col-xs-12'>
					<button @click="selectedComponent = 'appQuote'">Quote</button>
					<button @click="selectedComponent = 'appAuthor'">Author</button>
					<button @click="selectedComponent = 'appNew'">New</button>
					<hr>
					<p>{{ selectedComponent }}</p>
					<keep-alive>
						<component :is="selectedComponent">
							<p>Default Content</p>
						</component>
						<!--<app-quote>
							<h2 slot='title'>{{ quoteTitle }}</h2>
							<p>A damn wonderful quote</p>
						</app-quote>-->
					</keep-alive>
        </div>
      </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
		import Author from './components/Author.vue';
		import New from './components/New.vue';
    export default {
			data: function() {
				return {
					quoteTitle: 'The Great Quote',
					selectedComponent: 'appQuote'
				}
			},
			components: {
				appQuote: Quote,
				appAuthor: Author,
				appNew: New
			}
    }
</script>

<style>

</style>
