<script>
	import { page } from '$app/stores';

	import iconCross from '$lib/images/icons/icon-menu-cross.svg';
	import iconTwitter from '$lib/images/icons/icon-twitter.svg';
	import iconInstagram from '$lib/images/icons/icon-instagram.svg';

	export let showMenu = false;
</script>

<div class="nav-wrapper" class:showMenu>
	<section class="buttons">
		<div class="social-links">
			<a href="https://twitter.com/PunctuationPics" target="_blank" rel="noreferrer noopener">
				<img src={iconTwitter} alt="Twitter" />
			</a>
			<a
				href="https://www.instagram.com/punctuationpictures/"
				target="_blank"
				rel="noreferrer noopener"
			>
				<img src={iconInstagram} alt="Instagram" />
			</a>
		</div>
		<button on:click>
			<img src={iconCross} alt="Cross" />
		</button>
	</section>
	<nav>
		<h1>The Travelling Salesman</h1>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li>
				<a
					href="https://github.com/punctuationpictures/travelling-salesman"
					target="_blank"
					rel="noreferrer noopener"
				>
					Github repo
				</a>
			</li>
			<li>
				<a
					href="https://www.figma.com/file/e1FyJbKmA5Fpa6sFotf0g9/PUNCTUATION_PICTURES_travelling_salesman"
					target="_blank"
					rel="noreferrer noopener"
				>
					Figma project
				</a>
			</li>
		</ul>
	</nav>
	<section>
		<h1 created>Created by:</h1>
		<ul>
			<li url>
				<a href="https://www.kaboomshebang.com" target="_blank" rel="noreferrer noopener"
					>Kaboom Shebang</a
				>
			</li>
			<li url>
				<a href="https://punctuation.pictures" target="_blank" rel="noreferrer noopener"
					>Punctuation Pictures</a
				>
			</li>
		</ul>
	</section>
</div>

<style>
	.nav-wrapper {
		position: absolute;
		top: -30rem;
		right: -1rem;
		display: flex;
		flex-direction: column;
		gap: 2rem;
		padding: 2rem;
		width: calc(100vw - 4rem);
		background-color: white;
		transition: top 200ms ease-in-out;
	}

	.showMenu {
		top: -1rem;
	}

	/* social media and close button */
	.buttons {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
	}

	.social-links {
		display: inline-flex;
		gap: 0.5rem;
	}

	.social-links > a > img {
		height: 1.25rem;
	}

	button {
		all: unset;
	}

	/* navigation */
	nav {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	h1 {
		font-size: 1rem;
		text-align: left;
		font-weight: 700;
	}

	h1[created] {
		font-size: 0.75rem;
	}

	nav > h1 {
		border-bottom: 0.25rem solid var(--color-orange);
	}

	ul {
		padding: 0;
		margin: 0;
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[url]::before {
		content: '↪ ';
		color: var(--color-orange);
		font-weight: 700;
	}

	a {
		color: black;
	}

	@media only screen and (min-width: 400px) {
		.nav-wrapper {
			width: 15rem;
		}
	}
</style>
