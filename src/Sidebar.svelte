<script>
	import Pages from "./Pages.svelte";
	import Dictionary from "./helpers/dictionary.helper.ts";

	export let open = false;
</script>

<style>
	aside {
		margin-top: 48px;
		width: 295px;
		height: 700px;
		max-height: 1050px;
		background: rgb(255, 255, 255);
		top: -300%;
		transition: top 0.5s ease-in-out;
		overflow-y: scroll;
	}

	nav {
		padding: 5% 0% 5% 10%;
	}

	.content {
		border-top: 1px solid #dddddd;
	}

	.open {
		top: 0;
	}
</style>

<aside
	class="absolute w-full h-full bg-gray-200 border-r-2 shadow-lg"
	class:open>
	<nav class="content-main">
		<Pages pages={Dictionary.pages.about} icon={"icon-chat"}/>
	</nav>
	<nav class="content">
		<Pages pages={Dictionary.pages.contact} icon={"icon-phone"}/>
	</nav>
</aside>
