<script>
	import { v4 as uuidv4 } from 'uuid';
	import Exercise from './Exercise.svelte';

	export let exercises : []
	export let workoutName : String
</script>

<h2>{workoutName}</h2>

<Exercise
	name='wide-front pull-ups'
	id=uuidv4()
	/>

<Exercise
	name='arnold presses'
	weight=true
	id=uuidv4()
	/>
