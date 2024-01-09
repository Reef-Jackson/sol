<script>
    import Menu from "../components/menu.svelte";
    import Hero from "../components/hero.svelte";
    import AboutMe from "../components/aboutMe.svelte"
    import WorkItem from "../components/workItem.svelte";
    import Contact from "../components/contact.svelte";
</script>

<Menu />
<section id="home"></section>
<Hero />
<section id="about"></section>
<AboutMe 
    title="About me:"
    p1="
    A passionate film-maker from Chesterfield, England.
    I believe every shot needs to tell a story, and I'm here to help you do just that. As an experienced film-maker, I'll work closely to achieve your vision."
    p2="This portfolio shows my experience and skill in film, my chosen strong point is audio."
/>
<section id="work"></section>
<WorkItem />
<Contact />
<style>
    :global(html) {
        scroll-behavior: smooth;
    } 
</style>
