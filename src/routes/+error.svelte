<script lang="ts">
	import { page } from '$app/stores';
	import '../styles.css';

	const pageDescription = 'Something went wrong!';
</script>

<svelte:head>
	<title>{$page.status} Error - Ematchi</title>
	<meta name="description" content={pageDescription} />
</svelte:head>

<main class="error-container">
	<div class="error-content">
		<h1>{$page.status} Error</h1>
		<p>Oops! {pageDescription}</p>
		<a href="/" class="home-link">Return to Home</a>
	</div>
</main>

<style>
	.error-container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		background: var(--bg-1);
		color: var(--fg);
		padding: 2rem;
	}

	.error-content {
		text-align: center;
		max-width: 600px;
		padding: 2rem;
		border: 1px solid var(--card-border);
		border-radius: 8px;
		background: var(--bg-2);
	}

	h1 {
		color: var(--accent);
		margin-bottom: 1rem;
	}

	p {
		margin-bottom: 2rem;
	}

	.home-link {
		display: inline-block;
		padding: 0.5rem 1rem;
		background: var(--accent);
		color: white;
		text-decoration: none;
		border-radius: 4px;
		transition: background 0.3s ease;
	}
</style>
