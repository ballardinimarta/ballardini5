<body>
	<main>
		<section id="info">
			<h1>Märta Ballardini</h1>
			<h2>Frontend Developer</h2>
			<h3>Stockholm, Sweden</h3>
		</section>
		<section id="projects">
			<div class="imagelink">
				<a
					href="/img/CVMarta.pdf"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="View my CV"
				>
					<img src="/img/CV.png" alt="CV Preview" />
				</a>
			</div>
			<div class="imagelink">
				<a
					href="https://besatt.org/"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="Besatt - Magazine Website"
				>
					<img src="/img/BESATT.png" alt="Screenshot from https://besatt.org/" />
				</a>
			</div>
			<div class="imagelink">
				<a
					href="https://www.williamjwolffelt.com/"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="William J Wolffelt - Artist Portfolio"
				>
					<img src="/img/WW.png" alt="Screenshot from https://www.williamjwolffelt.com/" />
				</a>
			</div>
			<div class="imagelink">
				<a
					href="https://sl-hitta-avgang.onrender.com/"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="SL Departure Finder - Public Transport App"
				>
					<img src="/img/SL.png" alt="Screenshot from https://sl-hitta-avgang.onrender.com/" />
				</a>
			</div>
		</section>
		<section id="links">
			<div class="imagelink">
				<a
					href="https://github.com/ballardinimarta"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="Visit my GitHub"
				>
					<img src="/img/github.png" alt="GitHub logo" />
				</a>
			</div>

			<div class="imagelink">
				<a
					href="mailto:marta.ballardini@gmail.com"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="Send me an email"
				>
					<img src="/img/email-sign.gif" alt="Email Sign gif" />
				</a>
			</div>
			<div class="imagelink">
				<a
					href="https://www.linkedin.com/in/m%C3%A4rta-ballardini-403a6a165/"
					target="_blank"
					rel="noopener noreferrer"
					data-tooltip="Connect on LinkedIn"
				>
					<img src="/img/linkedin.png" alt="LinkedIn logo" />
				</a>
			</div>
			<div class="imagelink">
				<a href="tel:+46700623959" target="_blank" rel="noopener noreferrer" data-tooltip="Call me">
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
			rgb(102, 145, 232) 40%,
			rgba(51, 51, 51, 1) 80%
		);
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-family: 'VT323', monospace;
		color: #fff;
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
	h3 {
		font-size: 1.5rem;
		margin: 0;
		@media (max-width: 768px) {
			font-size: 1rem;
		}
	}
	#info {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 0.5rem;
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
		pointer-events: none;
	}
	#projects .imagelink,
	#links .imagelink {
		position: absolute;
		height: 5vh;
		transform-origin: 50% 50%;
		pointer-events: auto;
	}
	#projects {
		z-index: 1;
	}
	#links {
		z-index: 2;
	}
	#projects .imagelink {
		animation: orbit 10s linear infinite;
	}
	#links .imagelink {
		animation: orbit-reverse 10s linear infinite;
	}
	#projects .imagelink:hover,
	#links .imagelink:hover {
		animation-play-state: paused;
	}
	#projects .imagelink:nth-child(1),
	#links .imagelink:nth-child(1) {
		animation-delay: 0s;
	}
	#projects .imagelink:nth-child(2),
	#links .imagelink:nth-child(2) {
		animation-delay: -2.5s;
	}
	#projects .imagelink:nth-child(3),
	#links .imagelink:nth-child(3) {
		animation-delay: -5s;
	}
	#projects .imagelink:nth-child(4),
	#links .imagelink:nth-child(4) {
		animation-delay: -7.5s;
	}
	.imagelink {
		position: absolute;
		height: 5vh;
		transform-origin: 50% 50%;
		pointer-events: auto;
	}
	.imagelink a {
		position: relative;
		display: inline-block;
		height: 100%;
	}
	.imagelink img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
	.imagelink a::after {
		content: attr(data-tooltip);
		position: absolute;
		bottom: 100%;
		left: 50%;
		transform: translateX(-50%);
		padding: 0.5rem;
		background: rgba(0, 0, 0, 0.8);
		color: white;
		border-radius: 4px;
		font-size: 1rem;
		white-space: nowrap;
		opacity: 0;
		visibility: hidden;
		transition:
			opacity 0.2s,
			visibility 0.2s;
	}
	.imagelink:hover a::after {
		opacity: 1;
		visibility: visible;
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
