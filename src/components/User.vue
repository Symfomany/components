<template>
	<div>
		<p>Je suis Julien, développeur {{ langage }}</p>
	</div>
</template>


<script>

// exporte le composant pour Webpack
export default {
		name: 'user',
		props: {
			langage: {
				type: String
			}
		}
}
</script>

<style scoped>
	p {
		color: blue;
	}
</style>