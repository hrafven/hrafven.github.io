<script>
	import Icon from '@iconify/svelte';

	function scrollBottom() {
		window.scroll({ top: 9999, left: 0, behavior: 'smooth' });
		document.getElementById('email')?.focus({ preventScroll: true });
	}
</script>

<div class="overflow-visible">
	<header class="h-screen md:container md:mx-auto">
		<section class="flex flex-col justify-center items-center h-full">
			<div class="flex flex-col gap-5 justify-center items-center w-3/4 max-w-sm h-1/2 sm:w-11/12 sm:max-w-md">
				<a class="flex flex-col items-center" href="/">
					<img src="https://avatars.githubusercontent.com/u/15106129" alt="" />
					<h1 class="text-3xl font-bold underline text-center">
						Hugo <span class="font-thin">"hrafven"</span> Bidois
					</h1>
				</a>
				<section>
					<p class="text-center">Salesforce CRM Technical Consultant at iCom by KPMG</p>
				</section>
				<section class="flex justify-center gap-5 items-center w-5/6 text-2xl">
					<a href="https://www.linkedin.com/in/hugo-bidois-hrafven/">
						<Icon icon="line-md:linkedin" />
					</a>
					<button
						class="px-3 align-middle rounded-full bg-sky-500 hover:bg-sky-700"
						on:click={scrollBottom}
					>
						Contact Me
					</button>
					<a href="https://github.com/hrafven">
						<Icon icon="line-md:github" />
					</a>
				</section>
			</div>
		</section>
	</header>

	<main class="h-screen md:container md:mx-auto">
		<section class="flex flex-col justify-center items-center h-full">
			<form
				enctype="application/x-www-form-urlencoded"
				action="https://hrafven-contact.deno.dev/"
				method="post"
				class="w-3/4 max-w-sm text-2xl"
				target="formresponse"
			>
				<fieldset class="flex flex-col gap-5 justify-around py-5">
					<legend><h2>Contact Me</h2></legend>
					<label class="block" for="email">
						<span class="block text-sm font-medium">Email Address</span>
						<input
							type="text"
							id="email"
							name="email"
							required
							autocomplete="email"
							class="block py-2 px-3 mt-1 w-full text-sm bg-white rounded-md border shadow-sm focus:ring-1 focus:outline-none disabled:shadow-none border-slate-300 placeholder-slate-400 invalid:border-pink-500 invalid:text-pink-600 focus:border-sky-500 focus:ring-sky-500 focus:invalid:border-pink-500 focus:invalid:ring-pink-500 disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200"
						/>
					</label>
					<label class="block" for="message">
						<span class="block text-sm font-medium">Message</span>
						<textarea
							id="message"
							name="message"
							required
							class="block py-2 px-3 mt-1 w-full text-sm bg-white rounded-md border shadow-sm focus:ring-1 focus:outline-none disabled:shadow-none border-slate-300 placeholder-slate-400 invalid:border-pink-500 invalid:text-pink-600 focus:border-sky-500 focus:ring-sky-500 focus:invalid:border-pink-500 focus:invalid:ring-pink-500 disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200"
						></textarea>
					</label>
					<button class="px-3 align-middle rounded-full bg-sky-500 hover:bg-sky-700"> Send </button>
				</fieldset>
			</form>
			<iframe title="formresponse" name="formresponse" style="color:white;text-align:center" ></iframe>
		</section>
	</main>
</div>

<style lang="postcss">
	:global(html) {
		background-color: #242425;
		color: white;
	}
	input,
	textarea {
		color: black;
	}
</style>
