<style>
	#laboite {
		display: flex;
		flex-direction: column;
		margin-top: 10rem;
	}

	button {
		margin-bottom: 1rem;
		border: none;
		font-size: 1.2rem;
		background: #55ACEE;
		color: #fff;
		cursor: pointer;
		padding: 15px 30px;
		transition: all 0.2s;
	}
</style>

<svelte:head>
	<title>La boite à teucha</title>
</svelte:head>

<h1>La boite à teucha</h1>

<div id="laboite">
	<button on:click="{ () => { play('lachatte') } }">La chatte</button>
	<button on:click="{ () => { play('lachatquila') } }">La chatte qu'il a</button>
	<button on:click="{ () => { play('lachaaate') } }">La chaaaatte !!!</button>
</div>

<script>
	function play(sampleName) {
		var sample = new Audio(`${sampleName}.mp3`);
		sample.play();
	}
</script>