---
title: Customizing Your Snake
permalink: /snake-customization
layout: card
---

Make your snake unique by assigning it a color, head, and tail in your response to the Battlesnake API's `start` request.

### A response to start with these specifications:

```
{
	"color": "#736CCB",
	"headType": "beluga",
	"tailType": "curled"
}
```
#### Will customize your snake like this!

<div class="row p-10">
	<svg class="align-self-center ml-3 mr-0 w-40" fill="#736CCB" style="transform:rotateY(180deg);" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
	    <path d="M23 48c2 12 2 26 4 26 0 0-2 0 0 0s1-19-1-28c-1-10-2-19-1-28S31 1 42 0c10-1 19 5 25 12 5 7 7 11 8 21l1 12c0 3-2 17-1 21 1 5 8 7 8 7 8 3 16-1 17 1 0 2-3 5-8 6-11 3-24 6-30-4-4-8-2-18-2-26-1-9-1-20-6-28-2-3-6-5-9-4s-2 4-2 6c0 20 9 42 2 61-4 8-11 16-21 15l-4-1-2-1c-3-2-6-2-9-2-4 1-5 4-9 4V0c17 2 22 38 23 48z"/>
	</svg>
	<svg class="align-self-center mr-0 w-40" fill="#736CCB" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
	    <path d="M0 0h100v100H0z"/>
	</svg>
	<svg class="align-self-center w-40" fill="#736CCB" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
	  <path d="M0 100h56L32 88l-5-14 73 2-10-48L50 0H0zm23-61a9 9 0 1 1-10 10 9 9 0 0 1 10-10z"/>
	</svg>
</div>


---

## Assign a Color

Specify the `color` for your snake using a HEX code (like this: `#736CCB`). A random color will be selected for you if you do not specify a color.

---

## Choose a head and tail

Find your favorite snake head and tail from the options below and use the name in the parameters `headType` and `tailType`. If you do not specify a head or tail type the "regular" version will be used.

<div class="row">
	<div class="col-12 col-sm-5 p-25 card-body">
		<h4 class="card-header"><strong>Snake Heads</strong></h4>
		<ul class="list-group">
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/regular.svg" fill="#736CCB" alt="regular snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">regular (default)</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/beluga.svg" alt="beluga snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">beluga</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bendr.svg" alt="bendr snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bendr</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/dead.svg" alt="dead snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">dead</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/evil.svg" alt="evil snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">evil</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/fang.svg" alt="fang snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">fang</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/pixel.svg" alt="pixel snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">pixel</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/safe.svg" alt="safe snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">safe</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/sand-worm.svg" alt="sand-worm snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">sand-worm</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/shades.svg" alt="shades snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">shades</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/silly.svg" alt="silly snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">silly</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/smile.svg" alt="smile snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">smile</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/tongue.svg" alt="tongue snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">tongue</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-bonhomme.svg" alt="bwc-bonhomme snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-bonhomme</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-earmuffs.svg" alt="bwc-earmuffs snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-earmuffs</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-rudolph.svg" alt="bwc-rudolph snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-rudolph</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-scarf.svg" alt="bwc-scarf snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-scarf</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-ski.svg" alt="bwc-ski snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-ski</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-snow-worm.svg" alt="bwc-snow-worm snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-snow-worm</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/head/bwc-snowman.svg" alt="bwc-snowman snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-snowman</p>
			</li>
		</ul>
	</div>
	<div class="col-12 col-sm-5  p-25 card-body">
		<h4 class="card-header"><strong>Snake Tails</strong></h4>
		<ul class="list-group">
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/regular.svg" alt="regular snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">regular (default)</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/block-bum.svg" alt="block-bum snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">block-bum</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/bolt.svg" alt="bolt snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bolt</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/curled.svg" alt="curled snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">curled</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/fat-rattle.svg" alt="fat-rattle snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">fat-rattle</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/freckled.svg" alt="freckled snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">freckled</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/hook.svg" alt="hook snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">hook</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/pixel.svg" alt="pixel snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">pixel</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/round-bum.svg" alt="round-bum snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">round-bum</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/sharp.svg" alt="sharp snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">sharp</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/skinny.svg" alt="skinny snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">skinny</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/small-rattle.svg" alt="small-rattle snake head"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">small-rattle</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/bwc-bonhomme.svg" alt="bwc-bonhomme snake tail"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-bonhomme</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/bwc-flake.svg" alt="bwc-flake snake tail"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-flake</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/bwc-ice-skate.svg" alt="bwc-ice-skate snake tail"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-ice-skate</p>
			</li>
			<li class="list-group-item d-flex align-items-center">
				<img class="justify-self-start mr-2 w-40" src="/assets/images/snake/tail/bwc-present.svg" alt="bwc-present snake tail"/>
				<p class=" font-size-16 m-0 pl-4 pl-sm-2 pl-md-4">bwc-present</p>
			</li>
		</ul>
	</div>
</div>

### Futher Reading

Check out the [Battlesnake API Docs](/snake-api.html) for more on information and examples on interacting with the Battlesnake API.
