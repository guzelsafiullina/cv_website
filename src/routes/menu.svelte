
<script lang="ts">
    import { page } from '$app/stores';
	import { base } from '$app/paths';
</script>

<header>
    <nav>
        <ul>
            <li class:active={$page.url.pathname === '/'}>
                <a href="{base}/">Home</a>
            </li>
            <li class:active={$page.url.pathname === '/education'}>
                <a href="{base}/education">Education</a>
            <li class:active={$page.url.pathname === '/expirience'}>
                <a href="{base}/expirience">Expirience</a>
            <li class:active={$page.url.pathname === '/skills'}>
                <a href="{base}/skills">Skills</a>

            </li> 
        </ul>
    </nav>
</header>

<style>

    nav {
		display: flex;
		justify-content: center;
	}
    ul {
		position: relative;
        padding: 1em;
		margin: 1em;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
        margin: 1em;
		height: 100%;
	}
</style>