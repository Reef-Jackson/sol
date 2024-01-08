<script>
    import Menu from "../components/menu.svelte";
    import Hero from "../components/hero.svelte";
    import AboutMe from "../components/aboutMe.svelte"
    import WorkItem from "../components/workItem.svelte";
</script>

<Menu />
<section id="home"></section>
<Hero />
<section id="about"></section>
<AboutMe 
    title="About me:"
    p1="Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."
	p2="Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."
/>
<section id="work"></section>
<WorkItem />
<style>
    :global(html) {
        scroll-behavior: smooth;
    } 
</style>
