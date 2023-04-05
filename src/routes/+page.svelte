<script lang="ts">
	import { onMount } from 'svelte';

	function shuffle(array) {
		let currentIndex = array.length,
			randomIndex;
		// While there remain elements to shuffle.
		while (currentIndex != 0) {
			// Pick a remaining element.
			randomIndex = Math.floor(Math.random() * currentIndex);
			currentIndex--;
			// And swap it with the current element.
			array[currentIndex], array[randomIndex] = array[randomIndex], array[currentIndex]
		}

		return array;
	}
	let separator =
		'&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;';
	let texts = `
Apeeling Bananas Inc. - peel away your problems one layer at a time!                     
Emotional Skies Umbrellas Ltd. - because even the sky needs a good cry.                     
NinjaStride Sneakers Co. - silent but speedy, just like your ninja dreams.  
BubbleWonders Gum Factory - turning your mouth into a tiny bubble factory!
Eclipse Eyewear Emporium - solar eclipses for your eyes, all day, every day.
DragonSlayer Toothpaste Corp. - the minty fresh secret to conquering dragon breath.
Napuccino Coffee Roasters - it's like a power nap in a cup!
FootMittens Sock Boutique - feet mittens for every season.
CloudCradle Pillows & More - bedtime clouds for your sleepy head.
CrunchyDelight Taco House - portable happiness with a crunch.
RelentlessBuddies Alarm Clocks - the annoying friends you never knew you needed.
Sticktastic Duct Tape Ventures - the ultimate solution to life's sticky situations.
GrassyLocks Lawn Mower Services - giving grass a much-needed haircut since 1830.
GnomeGuardian Garden Decor - magical creatures that protect your tulips from evil.
WallWhisperer Paint Co. - make your walls look fabulous, one color at a time.
Hairvengers Shampoo Solutions - because dirt has no business being in your hair.
BreezyBliss Air Fresheners - no more awkward smells, just breezy bliss.
PaperJungle Tamers Inc. - taming the wild paper jungles of your desk.
OdorWarrior Deodorant Factory - conquering the battle against body odor since forever.
ChillSpot Refrigeration Ltd. - where leftovers go to chill.
RollAway Life Luggage Store - pack your life into a box and roll away.
StickyRice Glue Co. - sticking to you like white on rice.
HearthFire Candles Boutique - portable mini campfires for your home.
InkyEmpire Pen Warehouse - unleashing the power of ink onto an unsuspecting world.
StretchSquad Rubber Bands Corp. - the ultimate stretchy solution to holding stuff together.
WorldTuner Headphone Shop - drowning out the world, one song at a time.
ElectricOutreach Extension Cords - bringing electricity to places it was never meant to be.
GroundFlyer Bicycles - the closest thing to flying without leaving the ground.
PortableWaterfall Bottle Co. - your personal waterfall on the go.
Keycessorize Emporium - because keys deserve to accessorize, too!
		`.split('\n');
</script>

<div class="scrolling-text">
	<span
		on:animationiteration={() => {
			texts = shuffle(texts);
		}}><h4>{@html texts.join(separator)}</h4></span
	>
</div>
<main class="container">
	<h1>WARC</h1>
	<div class="grid">
		<div>
			<!-- <article> -->
				<h2>Current circle</h2>
				<table>
					<thead>
						<tr>
							<th scope="col">Team</th>
							<th scope="col">Time</th>
							<th scope="col">Delta</th>
						</tr>
					</thead>
					<tbody>
						<tr>
							<th scope="row">Red racer</th>
							<td>4.1</td>
							<td>+0.3</td>
						</tr>
					</tbody>
					<!-- <tfoot>
                  <tr>
                    <th scope="col">#</th>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                  </tr>
                </tfoot> -->
				</table>
			<!-- </article> -->
			<h2>Teams rating</h2>
			<table>
				<thead>
					<tr>
						<th scope="col">#</th>
						<th scope="col">Team</th>
						<th scope="col">Time</th>
						<th scope="col">Delta</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<th scope="row">1</th>
						<td>Red racer</td>
						<td>4.1</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">2</th>
						<td>IDK</td>
						<td>5.2</td>
						<td>+0.2</td>
					</tr>
					<tr>
						<th scope="row">3</th>
						<td>DM</td>
						<td>6.7</td>
						<td>+0.4</td>
					</tr>
					<tr>
						<th scope="row">4</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
				</tbody>
				<!-- <tfoot>
                  <tr>
                    <th scope="col">#</th>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                    <td scope="col">Total</td>
                  </tr>
                </tfoot> -->
			</table>
		</div>
		<div>
			<h2>Last circle</h2>
			<table>
				<thead>
					<tr>
						<th scope="col">#</th>
						<th scope="col">Team</th>
						<th scope="col">Time</th>
						<th scope="col">Delta</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<th scope="row">1</th>
						<td>Red racer</td>
						<td>4.1</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">2</th>
						<td>IDK</td>
						<td>5.2</td>
						<td>+0.2</td>
					</tr>
					<tr>
						<th scope="row">3</th>
						<td>DM</td>
						<td>6.7</td>
						<td>+0.4</td>
					</tr>
					<tr>
						<th scope="row">4</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">5</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">6</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">7</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">8</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
					<tr>
						<th scope="row">9</th>
						<td>Mhuahaha</td>
						<td>11</td>
						<td>+0.3</td>
					</tr>
				</tbody>
			</table>
		</div>
	</div>
</main>

<style>
	.scrolling-text {
		white-space: nowrap;
		overflow: hidden;
		position: relative;
	}

	.scrolling-text span {
		display: inline-block;
		padding-left: 100%;
		animation: scrolling 300s linear infinite;
	}

	@keyframes scrolling {
		0% {
			transform: translateX(0);
		}
		100% {
			transform: translateX(calc(-100%));
		}
	}
</style>
