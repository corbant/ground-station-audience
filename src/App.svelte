<script>




	const source = new EventSource('/events');

	source.addEventListener('position', function(e) {
		console.log(e.data);
	});

	source.addEventListener('altitude', function(e) {
		console.log(e.data);
	});

	source.addEventListener('status', function(e) {
		console.log(e.data);
	});
</script>

<main>
	<h1>Ground Control to Major Tom!</h1>
	<p>This was served from the ground station right to your phone.</p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>