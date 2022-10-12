<script lang="ts">
    import './app.css';

    import Quote from '$lib/quote.svelte';

    import GeneralInfo from '$lib/general_info.svelte';

    import Links from '$lib/links.svelte';
    import Statistics from '$lib/statistics.svelte';
	import Menu from './menu.svelte';


</script>



<main>
  <div> <Menu></Menu></div>
  <div> 
    <section>
        <GeneralInfo></GeneralInfo>
    </section>
    <Statistics></Statistics>

    <slot/>
    <!-- {#if menu === 0}
    <h1>
    </h1>
    {:else if menu === 1}
    <Education></Education>
    {:else if menu === 2}
    <Expirience></Expirience>
    {:else if menu === 3}
    <section>
        <Skills></Skills>
    </section>
    {:else if menu === 4}
    <Education></Education>
    <Expirience></Expirience>
    <Skills></Skills>
    {:else} -->
    <!-- <h1>
        Page Not Found
    </h1>
    {/if} -->


    <section>
        <Links></Links>
    </section>
    <section>
        <div class="random_number">
            <Quote></Quote>
        <!-- <script src="bundle.js"></script> -->

    </section>
    
</div>
</main>

