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
			<p class="py-4 md:py-0 prose max-w-none text-lg text-justify text-gray-700">
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
			<div class="container px-5 py-2 mx-auto lg:pt-12 lg:px-32">
				<div class="flex flex-wrap -m-1 md:-m-2 flex-col md:flex-row">
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/qLGe3qMMxFw"
								title="Evidencias de Aprendizaje 2020-2022"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/LVI2s_O9T3w"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/D1hV4HUSKW8"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/kdtB_dO6m70"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/VaRbgVGHklI"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/A6upjPZGgCo"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/bfEcwBMJAJ8"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
					<div class="flex flex-wrap py-4 md:py-0 md:w-1/2">
						<div class="w-full p-1 md:p-2">
							<iframe
								class="w-full aspect-video"
								src="https://www.youtube.com/embed/wN1gjYZYB6E"
								title="YouTube video player"
								allowfullscreen
							/>
						</div>
					</div>
				</div>
			</div>
			<h5 class="text-center pt-4 text-sm font-bold text-gray-600">Ciclo Escolar 2021-2022 únicamente clases a distancia</h5>
		</div>
	{/if}
</section>
