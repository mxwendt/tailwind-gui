<script>
	import { cols, gapX, gapY, rows } from '../stores/grid-store';
	import Breakpoints from '../components/Breakpoints.svelte';
	import Gaps from '../components/Gaps.svelte';
	import Rows from '../components/Rows.svelte';

	const maybeJoinXY = (gapX, gapY) =>
		gapX.replace('gap-x-', '') !== gapY.replace('gap-y-', '')
			? `${gapX} ${gapY}`
			: gapX.replace('-x', '');
</script>

<h1 class="text-3xl font-bold text-center">Tailwind Grid Editor</h1>

<div class="my-8">
	<h3 class="text-xl my-4">Breakpoints in <code class="font-bold">px</code></h3>
	<Breakpoints />
</div>

<div class="my-8">
	<h4 class="text-lg my-4">Grid Template Columns and Rows</h4>
	<Rows />
</div>

<div class="my-8">
	<h4 class="text-lg my-4">Gap</h4>
	<Gaps />
</div>

<div class="my-8 grid gap-0">
	<h3 class="text-xl my-4">Preview</h3>
	<div class="grid {maybeJoinXY($gapX, $gapY)} {$cols} {$rows}">
		<div class="rounded-lg border-2 border-blue-200 p-4">1</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">2</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">3</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">4</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">5</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">6</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">7</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">8</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">9</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">10</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">11</div>
		<div class="rounded-lg border-2 border-blue-200 p-4">12</div>
	</div>
</div>

<div class="my-8 grid gap-0">
	<h3 class="text-xl my-4">Markup</h3>
	<pre><code>
{`<div class="grid ${maybeJoinXY($gapX, $gapY)} ${$cols} ${$rows}">
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>
    <div>5</div>
    <div>6</div>
    <div>7</div>
    <div>8</div>
    <div>9</div>
    <div>10</div>
    <div>11</div>
    <div>12</div>
</div>`}
    </code></pre>
</div>
