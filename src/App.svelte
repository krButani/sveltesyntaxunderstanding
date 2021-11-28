<script>
import { end_hydrating } from 'svelte/internal';

	import Feedback from './components/Feedback.svelte';

	let name = 'kartik';

	const handelname = (e) => {
		console.log(e.detail);

		name = e.detail;
	}

</script>

<main>
	<Feedback username={name} on:changename={handelname} />
</main>

