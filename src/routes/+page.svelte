<script>
	import Icon from '@iconify/svelte';
</script>

<header class="h-screen md:container md:mx-auto">
	<section class="flex flex-col justify-center items-center h-full">
		<div class="flex flex-col justify-around items-center h-1/3">
			<a class="flex flex-col items-center my-5" href="/">
				<img src="https://avatars.githubusercontent.com/u/15106129" alt="" />
				<h1 class="text-3xl font-bold underline">
					Hugo <span class="font-thin">"hrafven"</span> Bidois
				</h1>
			</a>
			<section class="flex justify-between w-1/2 text-2xl">
				<a href="https://www.linkedin.com/in/hugo-bidois-hrafven/">
					<Icon icon="line-md:linkedin" />
				</a>
				<a href="https://github.com/hrafven">
					<Icon icon="line-md:github" />
				</a>
			</section>
		</div>
	</section>
</header>

<style lang="postcss">
	:global(html) {
		background-color: #242425;
		color: white;
	}
</style>
