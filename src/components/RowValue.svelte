<script>
	import { cols, rows } from '../stores/grid-store';
	export let valueX;
	export let valueY;

	const handleXChange = () => cols.set(valueX);
	const handleYChange = () => rows.set(valueY);
</script>

<div class="flex flex-grow flex-col items-center">
	<span>{valueX.replace('grid-cols-', '')}</span>
	<input
		class="my-1"
		type="radio"
		name="grid-cols"
		id={valueX}
		on:change={handleXChange}
		checked={$cols === valueX}
	/>
	<input
		class="my-1"
		type="radio"
		name="grid-rows"
		id={valueY}
		on:change={handleYChange}
		checked={$rows === valueY}
	/>
</div>
