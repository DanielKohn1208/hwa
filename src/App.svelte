<script>
	import Timer from './Timer.svelte';
	import HowTo from './HowTo.svelte';
	let audio;
	function timerEnds(){
		audio.play();
		 
	}
</script>
<style>
	h1,h3{
		text-align: center;
	}
</style>
<h1>Handwashing App</h1>

<Timer on:end={timerEnds}/>

<HowTo />
<h3>
	<a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control">Picture source</a>
	<a href="https://freesound.org/people/metrostock99/sounds/345086/">Sound Effect</a>
</h3>

<audio bind:this={audio}>
	<source src="public_sound.wav" />
</audio>
