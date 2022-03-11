<script>
	//viene lo de euro
	let coins = [];
	let btc = {};
	let dolar = [];
	let dolarven = {};

	const loadCoins = async () => {
		const res = await fetch(
			"https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=false"
		);
		const data = await res.json();
		coins = data;
		btc = coins[0].current_price.toLocaleString();
		console.log(btc);
	};
	loadCoins();

	const loadDolar = async () => {
		const res = await fetch(
			"https://s3.amazonaws.com/dolartoday/data.json"
		);
		const data = await res.json();
		dolar = data;
		dolarven = dolar.USD.transferencia;
		const math = dolarven * btc;
	};

	loadDolar();
</script>

<main>
	<!-- <section id="menu"> -->
	<nav
		class="navbar navbar-expand-lg navbar-light  bg-primary py-2 border-0 "
		style=""
		id="menu"
	>
		<div class="container-fluid ">
			<a
				class="navbar-brand ms-3 py-3 text-white "
				style="font-size: 2rem;"
				href="/"
				><span style="font-weight: 900;">Remi</span><span
					style="font-weight: 300;">Transfer</span
				></a
			>
			<button
				class="navbar-toggler  me-3 bg-white"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbarSupportedContent"
				aria-controls="navbarSupportedContent"
				aria-expanded="false"
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon" style="font-size: 1.5rem;" />
			</button>
			<div class="collapse navbar-collapse " id="navbarSupportedContent">
				<ul class="navbar-nav ms-auto p-3 ">
					<li class="nav-item">
						<a
							class="nav-link active letra2 text-white"
							aria-current="page"
							href="/">Home</a
						>
					</li>
					<li class="nav-item">
						<a class="nav-link letra2 text-white" href="/#servicios"
							>Servicios</a
						>
					</li>
					<li class="nav-item">
						<a class="nav-link letra2 text-white" href="/#blog"
							>Blogs</a
						>
					</li>
					<li class="nav-item">
						<a class="nav-link  text-white" href="/contacto"
							>Contactanos</a
						>
					</li>
				</ul>
			</div>
		</div>
	</nav>

	<section class="bloque1 text-white">
		<!-- particles.js container -->
		<div id="particles-js" />

		<!-- <div class="custom-shape-divider-bottom-1645573179">
			<svg
				data-name="Layer 1"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 1200 120"
				preserveAspectRatio="none"
			>
				<path
					d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z"
					class="shape-fill"
				/>
			</svg>
		</div> -->
		<div class="container-fluid" style="background-color: #0f1833;">
			<div class="container py-5">
				<div class="row">
					<div class="col-md my-auto ">
						<div class="flex1">
							<div class="titulo-negocioremesas ">
								<h1 class="display-2   " style="">
									<strong
										>!Registrate para recibir las mejores
										tasas!</strong
									>
								</h1>

								<div class="row d-flex justify-content-around">
									<div class="col-xxl-4 col-lg-6 ">
										<a
											href="trading"
											class="btn btn-primary  rounded-pill px-4 my-2 "
											style="font-size: 1.2rem;"
											><i class="" /><i
												class="fas fa-chevron-circle-right"
											/> Resgistrate</a
										>
									</div>

									<div class="col">
										<a
											href="trading"
											class="btn text-white border rounded-pill my-2  "
											style="font-size: 1.2rem;"
											>$ Ver nuestras tasas</a
										>
									</div>
								</div>
								<br />
								<p style="font-size: 2rem;">
									Necesitas ayuda ? <span class="text-warning"
										>Contactanos</span
									>
								</p>
							</div>
						</div>
					</div>
					<div class="col  mx-auto contenedor-celular">
						<div class="d-flex justify-content-center celular">
							<img
								src="img/celular.png"
								alt=""
								class="img-fluid "
								style="max-height:550px "
							/>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<section class="container-fluid bg-white py-5">
		<div class="container  bg-white " style="">
			<h2 class="display-3 "><b>!Una Experiencia diferente! ...</b></h2>

			<br />

			<div class="row my-5">
				<div class="col-xxl-3 col-md-6 mb-5">
					<div
						class="d-flex justify-content-center align-items-center"
					>
						<div
							class="bg-black text-white circulo text-center rounded-circle d-flex justify-content-center align-items-center p-3 mx-1"
							style="font-size: 2.5rem;"
						>
							<i class="fa-regular fa-square-check" />
						</div>

						<h2 class="mb-0">Identidad</h2>
					</div>
					<br />
					<p style="font-size: 1.5rem;">
						Confirmamos tu identidad antes de realizar el envio.
					</p>
				</div>
				<div class="col-xxl-3 col-md-6 mb-5 ">
					<div
						class="d-flex justify-content-center align-items-center"
					>
						<div
							class="bg-black text-white circulo text-center rounded-circle d-flex justify-content-center align-items-center p-3 mx-1"
							style="font-size: 2.5rem;"
						>
							<i class="fa-solid fa-building-columns" />
						</div>

						<h2 class="mb-0">Bancos</h2>
					</div>
					<br />
					<p style="font-size: 1.5rem;">
						Verifica disponibilidad antes de una transaccion.
					</p>
				</div>
				<div class="col-xxl-3 col-md-6 mb-5">
					<div
						class="d-flex justify-content-center align-items-center"
					>
						<div
							class="bg-black text-white circulo text-center rounded-circle d-flex justify-content-center align-items-center p-3 mx-1"
							style="font-size: 2.5rem;"
						>
							<i class="fa-solid fa-user" />
						</div>

						<h2 class="mb-0">Atencion</h2>
					</div>

					<br />
					<p style="font-size: 1.5rem;">
						Envia dinero en nuestro horario de atencion al cliente
						8:00 am a 7:00 pm.
					</p>
				</div>
				<div class="col-xxl-3 col-md-6 mb-5">
					<div
						class="d-flex justify-content-center align-items-center"
					>
						<div
							class="bg-black text-white circulo text-center rounded-circle d-flex justify-content-center align-items-center p-3 mx-1"
							style="font-size: 2.5rem;"
						>
							<i class="fa-brands fa-whatsapp" />
						</div>

						<h2 class="mb-0">Whatsapp</h2>
					</div>

					<br />
					<p style="font-size: 1.5rem;">
						Contactanos via whatsapp y accede a nuestro grupo para
						consulta de tasas.
					</p>
				</div>
			</div>
		</div>
		<br />

		<div class="d-flex justify-content-center">
			<p class="btn btn-primary rounded-pill " style="font-size: 1.5rem;">
				Numeros autorizados para enviar tus remesas <b
					>+34-123456789 / +58-41212345678</b
				>
			</p>
		</div>

		<br />

		<div class="d-flex justify-content-center ">
			<p
				class=" display-5 btn border border-dark border-1 rounded-pill"
				style="font-size: 1.3rem;"
			>
				Unirme al grupo
			</p>
		</div>
	</section>

	<section class="container-fluid bg-white">
		<div class="container py-5">
			<div class="row">
				<div class="col-lg-8 col-sm-12">
					<h2 class="display-3">
						<b
							>Cotiza tasa actualizada y envia tu dinero desde
							Europa</b
						>
					</h2>

					<p class="display-5" style="">
						Obten ahora una tasa especial en tu primer envio.
					</p>
				</div>
				<div class="col-md-4 col-sm-12">
					<div class="btn btn-primary rounded p-3 my-1">
						<div class="d-flex">
							<img src="img/espana.png" alt="" style="" />
							<p class="my-auto mx-3 " style="font-size: 2.5rem;">
								España
							</p>
						</div>
					</div>

					<div class="btn btn-warning rounded p-3 my-1">
						<p class="text-start">Tasa de cambio</p>
						<div class="d-flex">
							{#if dolarven > 0}
								<p class="display-5">
									<strong>{dolarven} Bs / Usd</strong>
								</p>
							{:else}
								<p>Cargando...</p>
							{/if}
						</div>
					</div>

					<br /> <br />

					<div class="d-flex justify-content-center ">
						<p
							class="  btn btn-primary  px-5 py-2 rounded-pill"
							style="font-size: 1.5rem;"
						>
							Enviar dinero
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>

	<div class="criptos container-fluid  bg-warning py-1 mb-5 ">
		<div class="row">
			<div class="col text-center mt-2">
				<div class="  ">
					{#if coins.length > 0}
						<h2 class="ms-lg-5" style="font-size: 1.3rem;">
							<img
								src={coins[0].image}
								alt={coins[0].name}
								style="width: 3rem;"
							/>
							{coins[0].id.toUpperCase()}

							{coins[0].current_price.toLocaleString()} US$
						</h2>
					{:else}
						<p>Cargando...</p>
					{/if}
				</div>
			</div>

			<div class="col text-center mt-2">
				<div class=" ">
					{#if coins.length > 0}
						<h2 class="ms-lg-5" style="font-size: 1.3rem;">
							<img
								src={coins[1].image}
								alt={coins[1].name}
								style="width: 3rem;"
							/>
							{coins[1].id.toUpperCase()}
							<strong>
								{coins[1].current_price.toLocaleString()}</strong
							> US$
						</h2>
					{:else}
						<p>Cargando...</p>
					{/if}
				</div>
			</div>

			<div class="col text-center mt-2">
				<div class="  ">
					{#if coins.length > 0}
						<h2 class="ms-lg-5" style="font-size: 1.3rem;">
							<img
								src={coins[8].image}
								alt={coins[8].name}
								style="width: 3rem;"
							/>
							{coins[8].id.toUpperCase()}
							<strong>
								{coins[8].current_price.toLocaleString()}</strong
							> US$
						</h2>
					{:else}
						<p>Cargando...</p>
					{/if}
				</div>
			</div>
		</div>
	</div>

	<footer class="bg-dark text-center text-white footer pb-5 mt-5">
		<!-- Grid container -->
		<div class="container p-4 pb-0">
			<!-- Section: Social media -->
			<section class="mb-4">
				<!-- Facebook -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-facebook-f letra2" /></a
				>

				<!-- Twitter -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-twitter letra2" /></a
				>

				<!-- Google -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-google letra2" /></a
				>

				<!-- Instagram -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-instagram letra2" /></a
				>

				<!-- Linkedin -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-linkedin-in letra2" /></a
				>

				<!-- Github -->
				<a
					class="btn btn-outline-light btn-floating m-1"
					href="#!"
					role="button"><i class="fab fa-github letra2" /></a
				>
			</section>
			<!-- Section: Social media -->
		</div>
		<!-- Grid container -->

		<!-- Copyright -->
		<div
			class="text-center p-3 letra2"
			style="background-color: rgba(0, 0, 0, 0.2);"
		>
			Copyright © 2022 Criptoaprendes - Reservados todos los derechos
			<!--<a class="text-white" href="https://mdbootstrap.com/">MDBootstrap.com</a> -->
		</div>
		<!-- Copyright -->
	</footer>
</main>

<style>
	/* .custom-shape-divider-bottom-1645573179 {
		position: absolute;
		bottom: 0;
		height: 650px;
		left: 0;
		width: 100%;

		overflow: hidden;
		line-height: 0;
		z-index: -1;
	} */

	/* .custom-shape-divider-bottom-1645573179 svg {
		position: relative;
		display: block;
		width: calc(150% + 1.3px);
		height: 400px;
	} */

	.custom-shape-divider-bottom-1645573179 .shape-fill {
		fill: #0a44ca;
	}

	.celular {
		/* width: 40rem; */
	}

	.padding-100 {
		padding-top: 50px;
	}

	.fa-square-check {
		padding: 0;
		margin: 0;
	}

	@media screen and (max-width: 1629px) {
		.custom-shape-divider-bottom-1645573179 {
			height: 600px;
		}
	}

	@media screen and (max-width: 1200px) {
		.contenedor-celular {
			display: flex;
			justify-content: center;
			align-items: center;
		}
		.celular {
			max-width: 500px;
		}

		.custom-shape-divider-bottom-1645573179 svg {
			position: relative;
			display: block;
			width: calc(150% + 1.3px);
			height: 200px;
		}

		.custom-shape-divider-bottom-1645573179 {
			height: 500px;
		}
	}

	@media screen and (max-width: 992px) {
		.custom-shape-divider-bottom-1645573179 {
			height: 600px;
		}

		.custom-shape-divider-bottom-1645573179 svg {
			position: relative;
			display: block;
			width: calc(150% + 1.3px);
			height: 300px;
		}

		.padding-100 {
			padding-top: 70px;
		}
	}

	@media screen and (max-width: 768px) {
		.custom-shape-divider-bottom-1645573179 {
			height: 230px;
		}

		.padding-100 {
			padding-top: 30px;
		}
	}

	@media screen and (max-width: 490px) {
		.padding-100 {
			padding-top: 120px;
		}
	}

	@media screen and (max-width: 415px) {
		.padding-100 {
			padding-top: 50px;
		}
	}

	@media screen and (max-width: 400px) {
		.padding-100 {
			padding-top: 100px;
		}
	}
</style>
