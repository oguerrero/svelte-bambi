<script>
	import Nav from '../components/nav-component.svelte';
	import Evidencias from '../components/evidencias-component.svelte';
	import Home from '../components/home-component.svelte';
	import About from '../components/aboutUs-component.svelte';
	import Levels from '../components/levels-component.svelte';
	import Testimonios from '../components/testimonios-component.svelte';
	import Galery from '../components/galery-component.svelte';
	import Contact from '../components/contacto-component.svelte';
	import Footer from '../components/footer-component.svelte';

	let y, oldY;
	let up = true;
	$: {
		if (y > oldY && y > 700) {
			up = false;
		} else {
			up = true;
		}
		oldY = y;
	}
</script>

<Nav {up} />
<Home />
<Evidencias />
<About />
<Testimonios />
<Levels />
<Galery />
<Contact />
<Footer />

<svelte:window bind:scrollY={y} />
