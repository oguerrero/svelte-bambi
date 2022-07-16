<script>
	import { fade } from 'svelte/transition';
	import { inview } from 'svelte-inview';

	let name;
	let isInView;
</script>

<section
	class="py-8 px-8 md:px-28 bg-slate-200 mix-blend-multiply scroll-m-2 md:scroll-m-2"
	id="contacto"
	use:inview={{ unobserveOnEnter: true, rootMargin: '-20%' }}
	on:change={({ detail }) => {
		isInView = detail.inView;
	}}
>
	{#if isInView}
		<div in:fade>
			<h1 class="text-center pt-4 pb-8">
				<span
					class="border-4 border-black py-2 px-4 text-3xl font-bold text-black"
					>Contacto</span
				>
			</h1>
			<article class="flex flex-col md:flex-row bg-white  py-8 px-8 rounded-xl">
				<div
					class="grid flex-grow-0 h-max card bg-white rounded-box place-items-center py-4 md:pl-8 "
				>
					<ul>
						<li class="py-2">
							<span>
								<img
									src="icons/phone.svg"
									class="w-6 h-6 inline-block mr-2"
									alt="phone"
								/>
							</span>
							<a href="tel://52364449" class="inline-block"
								>Telefono: 52-36-44-49</a
							>
						</li>
						<li class="py-2">
							<a
								href="https://www.google.com/maps/place/Jardin+de+Ni%C3%B1os+%22Bambi%22/@19.5059206,-99.2096572,15z/data=!4m2!3m1!1s0x0:0xda53c787db74872b?sa=X&ved=2ahUKEwjf4f663OTpAhVRnq0KHfXtCDYQ_BIwCnoECA8QCA"
							>
								<span class="">
									<img
										src="icons/map.svg"
										class="w-6 h-6 inline-block mb-16 md:mb-8 mr-2"
										alt="map"
									/>
									<p class="inline-block md:hidden">
										Av Hacienda de Narvarte #200,<br /> Prados del Rosario,
										Azcapotzalco
										<br />Ciudad de México
									</p>
									<p class="md:inline-block hidden ">
										Av Hacienda de Narvarte #200, Prados del Rosario,<br
										/>Azcapotzalco Ciudad de México
									</p>
								</span>
								<iframe
									src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15043.322589819662!2d-99.2096572!3d19.5059206!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xda53c787db74872b!2sJardin%20de%20Ni%C3%B1os%20%22Bambi%22!5e0!3m2!1ses-419!2smx!4v1591753745446!5m2!1ses-419!2smx"
									width="300"
									height="300"
									frameborder="0"
									style="border:0;"
									allowfullscreen=""
									aria-hidden="false"
									tabindex="0"
									title="map"
								/></a
							>
						</li>
						<li class="py-2">
							<a href="kinderbambi2020@gmail.com">
								<span>
									<img
										src="icons/mail.svg"
										class="w-6 h-6 inline-block mr-2"
										alt="mail"
									/>
								</span>
								<p class="inline-block">kinderbambi2020@gmail.com</p>
							</a>
						</li>
					</ul>
				</div>
				<div
					class="grid flex-grow h-max card ml-4 bg-white rounded-box place-items-center mt-4 md:mt-0"
				>
					<form action="" class="form-control flex max-w-screen-2xl">
						<div class="form-control w-full">
							<input
								type="text"
								id={name}
								placeholder="Nombre"
								class="input input-group-lg my-2 border-2 border-gray-300 input-accent w-full md:w-96"
							/>
						</div>
						<div class="form-control w-full max-w-xs">
							<input
								type="email"
								placeholder="email"
								class="input input-group-lg my-2 border-2 border-gray-300  input-accent w-full md:w-96"
							/>
						</div>
						<div class="form-control">
							<input
								type="text"
								placeholder="Asunto"
								class="input input-group-lg my-2 border-2 border-gray-300  input-accent w-full md:w-96"
							/>
						</div>
						<div class="form-control">
							<textarea
								id="message"
								name="message"
								rows="6"
								placeholder="Mensaje"
								class="textarea resize-none my-2 border-2 border-gray-300  textarea-accent"
							/>
						</div>
						<div class="py-4 text-center">
							<a
								class="btn bg-gradient-to-r from-secondary to-primary border-0 text-white"
								href="#placeholder">Enviar</a
							>
						</div>
					</form>
				</div>
			</article>
		</div>
	{/if}
</section>
