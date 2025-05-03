<body>
	<main>
		<section id="info">
			<h1>Märta Ballardini</h1>
			<h2>Frontend Developer</h2>
		</section>
		<section id="projects">
			<div class="project">
				<a href="/img/CVMarta.pdf" target="_blank" rel="noopener noreferrer">
					<img src="/img/CV.png" alt="CV Preview" />
				</a>
			</div>
			<div class="project">
				<a href="https://besatt.org/" target="_blank" rel="noopener noreferrer">
					<img src="/img/BESATT.png" alt="Screenshot from https://besatt.org/" />
				</a>
			</div>
			<div class="project">
				<a href="https://www.williamjwolffelt.com/" target="_blank" rel="noopener noreferrer">
					<img src="/img/WW.png" alt="Screenshot from https://www.williamjwolffelt.com/" />
				</a>
			</div>
			<div class="project">
				<a href="https://sl-hitta-avgang.onrender.com/" target="_blank" rel="noopener noreferrer">
					<img src="/img/SL.png" alt="Screenshot from https://sl-hitta-avgang.onrender.com/" />
				</a>
			</div>
		</section>
		<section id="links">
			<div class="project">
				<a href="https://github.com/ballardinimarta" target="_blank" rel="noopener noreferrer">
					<img src="/img/github.png" alt="GitHub logo" />
				</a>
			</div>

			<div class="project">
				<a href="mailto:marta.ballardini@gmail.com" target="_blank" rel="noopener noreferrer">
					<img src="/img/email-sign.gif" alt="Email Sign gif" />
				</a>
			</div>
			<div class="project">
				<a
					href="https://www.linkedin.com/in/m%C3%A4rta-ballardini-403a6a165/"
					target="_blank"
					rel="noopener noreferrer"
				>
					<img src="/img/linkedin.png" alt="LinkedIn logo" />
				</a>
			</div>
			<div class="project">
				<a href="tel:+46700623959" target="_blank" rel="noopener noreferrer">
					<img src="/img/phone-ringing.gif" alt="Phone Ringing gif" />
				</a>
			</div>
		</section>
	</main>
</body>

<style>
	@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
	body {
		margin: 0;
		font-size: 16px;
	}
	main {
		background: #ff7105;
		background: radial-gradient(
			circle,
			rgba(255, 113, 5, 1) 0%,
			rgba(87, 124, 199, 1) 30%,
			rgba(51, 51, 51, 1) 80%
		);
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-family: 'VT323', monospace;
		color: #fff;
		gap: 1rem;
	}
	h1 {
		letter-spacing: 0.1em;
		font-size: 4rem;

		margin: 0;
		@media (max-width: 768px) {
			font-size: 2rem;
		}
	}
	h2 {
		font-size: 3rem;
		margin: 0;
		@media (max-width: 768px) {
			font-size: 1.5rem;
		}
	}
	#info {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 1rem;
		height: 100vh;
	}
	#projects,
	#links {
		position: absolute;
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	#projects .project,
	#links .project {
		position: absolute;
		height: 5vh;
		transform-origin: 50% 50%;
	}
	#projects .project {
		animation: orbit 10s linear infinite;
	}
	#links .project {
		animation: orbit-reverse 10s linear infinite;
	}
	#projects .project:nth-child(1),
	#links .project:nth-child(1) {
		animation-delay: 0s;
	}
	#projects .project:nth-child(2),
	#links .project:nth-child(2) {
		animation-delay: -2.5s;
	}
	#projects .project:nth-child(3),
	#links .project:nth-child(3) {
		animation-delay: -5s;
	}
	#projects .project:nth-child(4),
	#links .project:nth-child(4) {
		animation-delay: -7.5s;
	}
	.project img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
	@keyframes orbit {
		from {
			transform: rotate(0deg) translate(25vw, 0) rotate(0deg);
		}
		to {
			transform: rotate(360deg) translate(25vw, 0) rotate(-360deg);
		}
	}
	@keyframes orbit-reverse {
		from {
			transform: rotate(0deg) translate(20vw, 0) rotate(0deg);
		}
		to {
			transform: rotate(-360deg) translate(20vw, 0) rotate(360deg);
		}
	}
</style>
