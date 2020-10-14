<script>
	import Pages from "./Pages.svelte";
	import Dictionary from "./helpers/dictionary.helper.ts";

	export let open = false;
</script>

<style>
	aside {
		position: absolute;
		margin-top: 48px;
		width: 295px;
		height: 700px;
		max-height: 1050px;
		background: rgb(255, 255, 255);
		top: -300%;
		transition: top 0.5s ease-in-out;
		box-shadow: 0 10px 15px -3px rgba(0,0,0,.1), 0 4px 6px -2px rgba(0,0,0,.05);
		--bg-opacity: 1;
		border-right-width: 2px;
	}

	nav {
		padding: 2% 0% 2% 10%;
	}

	.content {
		border-top: 1px solid #dddddd;
	}

	.open {
		top: 0;
	}

	@media screen and (max-width: 976px) {
		aside {
			overflow-y: scroll;
		}
	}
</style>

<aside class:open>
		<nav class="content-main">
			<Pages pages={Dictionary.pages.about} icon={"icon-chat"} />
		</nav>
		<nav class="content">
			<Pages pages={Dictionary.pages.contact} icon={"icon-phone"} />
		</nav>
		<nav class="content">
			<Pages pages={Dictionary.pages.about} icon={"icon-chat"} />
		</nav>
</aside>
