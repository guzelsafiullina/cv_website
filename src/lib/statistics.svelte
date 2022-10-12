<script lang='ts'>
	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
    <div class="statistics_view">
        <button on:click={toggle}>
            Show weekly views statistics
        </button>
        <p>
            Summary views for the day: 1
        </p>

    </div>


{/if}

{#if !user.loggedIn}
    <div class="statistics_view">
        <button on:click={toggle}>
            Show daily views statistics
        </button>
        <p>
            Summary views for the week: 10
        </p>

    </div>



{/if}

<style>
    .statistics_view{
        display: inline;
        font-style: italic;
    }
</style>