<script lang="ts">
	import { fade } from 'svelte/transition';
	import { inview } from 'svelte-inview';

	let isInView;
</script>

<section
	class="-mt-8 md:-mt-32 px-8 pb-8 md:px-28 mix-blend-multiply scroll-m-16 md:scroll-m-10"
	id="evidencias"
	use:inview={{ unobserveOnEnter: true, rootMargin: '-20%' }}
	on:change={({ detail }) => {
		isInView = detail.inView;
	}}
>
	{#if isInView}
		<div in:fade>
			<h3 class="text-center pb-4">
				<p
					class="border-4 border-black py-2 px-4 text-3xl font-bold text-black"
				>
					Evidencias de Aprendizaje 2020-2022
				</p>
			</h3>
			<p
				class="py-4 md:py-0 prose max-w-none text-lg text-justify text-gray-700"
			>
				El compromiso del Jardin de Niños Bambi es que nuestros alumnos(as)
				aprendan a pesar de situaciones adversas... Nuestra experiencia de más
				de 40 años nos permite tener el personal, actividades, estrategias y
				avances tecnológicos para que su hijo(a) realmente aprenda... por lo que
				"ningún niño(a) se queda atrás, ni ningún niño(a) se queda fuera de
				adquirir aprendizajes". En estos momentos díficiles, en donde los padres
				de familia en casa apoyan para el aprendizaje de sus hijos(as) la
				inversión que hacen con el pago de colegiaturas se vuelve realmente
				fundamental... por lo que en el Jardin de Niños Bambi el aprendizaje de
				su hijo es nuestro único compromiso.
			</p>
			<p class="py-2 prose max-w-none text-lg text-justify text-gray-700">
				Las Evidencias de Aprendizaje que se presentan se refieren a la
				generación que por las circunstancias del Covid-19 tuvieron toda su
				educación preescolar con clases a distancia. Cursando desde preescolar 1
				hasta preescolar 3 en nuestro Colegio.
			</p>
			<div class="pt-2">
				<iframe
				class="w-4/5 h-60 md:h-96 mx-auto" 
					src="https://www.youtube.com/embed/videoseries?list=PLb2Rs3Ta9YFJ65dGvgcMiL5U1C05xgMdg"
					title="YouTube video player"
					frameborder="0"
					allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
					allowfullscreen
				/>
			</div>
			<h5 class="text-center pt-4 text-sm font-bold text-gray-600">
				Ciclo Escolar 2021-2022 únicamente clases a distancia
			</h5>
		</div>
	{/if}
</section>
