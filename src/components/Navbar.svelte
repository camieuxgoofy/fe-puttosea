<script>
	function handleAnchorClick(event) {
		event.preventDefault();
		const link = event.currentTarget;
		const anchorId = new URL(link.href).hash.replace('#', '');
		const anchor = document.getElementById(anchorId);
		window.scrollTo({
			top: anchor.offsetTop,
			behavior: 'smooth'
		});
	}
</script>

<nav class="sticky top-0 w-full py-6 text-white flex">
	<div class="flex justify-between max-w-screen-xl mx-auto">
		<div class="flex space-x-8">
			<img src="/images/logo.png" alt="Puttosea Logo" width={99} height={13} />
			<div class="flex items-center pl-28 space-x-8">
				<a href="/">Home</a>
				<a href="/#destination" on:click={handleAnchorClick}>Destination</a>
				<a href="/#service" on:click={handleAnchorClick}>Service</a>
				<a href="/">Gallery</a>
				<a href="/">About</a>
			</div>
			<div class="flex items-center space-x-8">
				<a class="border py-3 px-4 rounded-2xl" href="/">Sign In</a>
				<a class="bg-white py-3 px-4 text-black rounded-2xl" href="/">Sign Up</a>
			</div>
		</div>
	</div>
</nav>
