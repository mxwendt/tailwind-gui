<script>
	import { gapX, gapY } from '../stores/grid-store';
	export let valueX;
	export let valueY;

	const handleXChange = () => gapX.set(valueX);
	const handleYChange = () => gapY.set(valueY);
</script>

<div class="flex flex-grow flex-col items-center">
	<span>{valueX.replace('gap-x-', '')}</span>
	<input
		class="my-1"
		type="radio"
		name="gap-x"
		id={valueX}
		on:change={handleXChange}
		checked={$gapX === valueX}
	/>
	<input
		class="my-1"
		type="radio"
		name="gap-y"
		id={valueY}
		on:change={handleYChange}
		checked={$gapY === valueY}
	/>
</div>
