<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(71, 71, 71, 0.25);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0 auto;
		padding: 0 2em;
		max-width: 56em;
		box-sizing: border-box;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: inline-block;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: #77CFDE;
		display: block;
		bottom: -1px;
	}

	a {
		color: #1E3576;
		display: block;
		padding: 1em 0.5em;
		text-decoration: none;
	}
</style>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">home</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">about</a></li>
		<li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li>
	</ul>
</nav>
