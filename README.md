# Naturalnezdjeciapl
Photographer website
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Joanna Markiewicz | Photographie</title>

  <style>
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: #faf6f0;
      color: #493b32;
      font: 16px/1.7 Arial, sans-serif;
    }
    header, section, footer { padding: 30px 7%; }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      border-bottom: 1px solid #ded3c7;
    }
    .brand { font: 25px Georgia, serif; }
    nav { display: flex; gap: 18px; }
    a { color: inherit; }
    nav a { text-decoration: none; font-size: 14px; }
    h1, h2, h3 {
      font-family: Georgia, serif;
      font-weight: normal;
      line-height: 1.15;
    }
    h1 { font-size: clamp(44px, 7vw, 78px); margin: 24px 0; }
    h2 { font-size: 36px; }
    h3 { font-size: 28px; }
    .hero {
      padding-top: 75px;
      padding-bottom: 75px;
      background: radial-gradient(ellipse at right, #e8d5bf, transparent 75%);
    }
    .hero p { max-width: 570px; }
    .label {
      font-size: 12px;
      letter-spacing: 3px;
      color: #805743;
    }
    .button, button {
      display: inline-block;
      background: #805743;
      color: white;
      border: 0;
      border-radius: 4px;
      padding: 11px 18px;
      cursor: pointer;
      font: inherit;
      text-decoration: none;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 25px;
    }
    .sessions { background: white; }
    .gallery .photo:not(:first-child) { display: none; }
    .gallery img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      border-radius: 80px 80px 4px 4px;
      display: block;
      cursor: zoom-in;
    }
    .gallery-open { margin-top: 12px; }
    .contact {
      text-align: center;
      background: #eee4d9;
      padding-top: 55px;
      padding-bottom: 55px;
    }
    footer { text-align: center; font-size: 13px; }
    dialog {
      width: min(1150px, 96vw);
      max-width: 96vw;
      max-height: 92vh;
      overflow: auto;
      border: 0;
      padding: 25px;
      background: #faf6f0;
      color: #493b32;
    }
    dialog::backdrop { background: #000b; }
    .grid-top, .controls {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
    }
    .photo-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 16px;
    }
    .photo-grid button {
      background: none;
      padding: 0;
      display: block;
    }
    .photo-grid img {
      width: 100%;
      height: 270px;
      object-fit: cover;
      display: block;
      border-radius: 4px;
    }
    #viewer { background: #201d1b; color: white; }
    #large {
      display: block;
      width: 100%;
      height: 72vh;
      object-fit: contain;
      margin-top: 15px;
    }
    a:focus-visible, button:focus-visible {
      outline: 3px solid #b78b6b;
      outline-offset: 3px;
    }
    @media (max-width: 700px) {
      header { flex-direction: column; }
      .grid { grid-template-columns: 1fr; }
      section { padding: 35px 7%; }
      .photo-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
      .photo-grid img { height: 180px; }
    }
    @media (max-width: 380px) {
      .photo-grid { grid-template-columns: 1fr; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
    }
  </style>
</head>

<body>
  <header>
    <div class="brand">Joanna Markiewicz</div>
    <nav aria-label="Navigation principale">
      <a href="#seances">Les séances</a>
      <a href="#approche">L’approche</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div class="label">GROSSESSE · NOUVEAU-NÉ · FAMILLE</div>
      <h1>De petits instants.<br>De grands souvenirs.</h1>
      <p>
        L’attente, les petites mains, la tendresse de vos gestes.
        Des séances photo pour célébrer votre famille,
        dès les premiers instants.
      </p>
      <a class="button" href="#seances">Découvrir les séances</a>
    </section>

    <section id="seances" class="sessions">
      <h2>Une séance pour chaque chapitre.</h2>

      <div class="grid">
        <article>
          <div class="gallery" id="grossesse">
            <div class="photo">
              <img src="assets/images/grossesse-01.jpg"
                   alt="Photographie de grossesse">
            </div>
          </div>
          <h3>Grossesse</h3>
          <p>
            Célébrez votre grossesse et l’émotion de cette attente,
            avant la rencontre avec votre bébé.
          </p>
        </article>

        <article>
          <div class="gallery" id="naissance">
            <div class="photo">
              <img src="assets/images/nouveau-ne-01.jpg"
                   alt="Photographie de nouveau-né 1" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-02.jpg"
                   alt="Photographie de nouveau-né 2" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-03.jpg"
                   alt="Photographie de nouveau-né 3" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-04.jpg"
                   alt="Photographie de nouveau-né 4" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-05.jpg"
                   alt="Photographie de nouveau-né 5" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-06.jpg"
                   alt="Photographie de nouveau-né 6" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-07.jpg"
                   alt="Photographie de nouveau-né 7" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-08.jpg"
                   alt="Photographie de nouveau-né 8" loading="lazy">
            </div>
            <div class="photo">
              <img src="assets/images/nouveau-ne-09.jpg"
                   alt="Photographie de nouveau-né 9" loading="lazy">
            </div>
          </div>
          <h3>Nouveau-né</h3>
          <p>
            Gardez une trace de ses premiers jours, de ses petits détails
            et de toute la tendresse qui l’entoure.
          </p>
        </article>

        <article>
          <div class="gallery" id="famille">
            <div class="photo">
              <img src="assets/images/famille-01.jpg"
                   alt="Photographie de famille" loading="lazy">
            </div>
          </div>
          <h3>Parents &amp; famille</h3>
          <p>
            Vos éclats de rire, vos câlins, votre complicité.
            Des souvenirs des liens qui rendent votre famille unique.
          </p>
        </article>
      </div>
    </section>

    <section id="approche">
      <div class="label">VOTRE HISTOIRE EN IMAGES</div>
      <h2>Imaginons votre séance ensemble.</h2>
      <p>
        Parlez-moi de votre famille et du moment que vous souhaitez
        photographier. Échangeons sur vos envies, les dates, le lieu
        et les tarifs pour préparer votre séance.
      </p>
    </section>

    <section class="contact" id="contact">
      <h2>Et si nous racontions votre histoire ?</h2>
      <p>
        Une séance grossesse, naissance ou famille ?
        Partagez vos envies et quelques mots sur vous.
      </p>
      <a class="button" href="mailto:naturalnezdjeciapl@gmail.com">
        Parlons de votre séance
      </a>
    </section>
  </main>

  <footer>
    Joanna Markiewicz · Photographie grossesse, nouveau-né et famille
  </footer>

  <dialog id="grid-view" aria-labelledby="grid-title">
    <div class="grid-top">
      <h2 id="grid-title">Galerie</h2>
      <button id="grid-close" type="button">Fermer la galerie</button>
    </div>
    <p>Cliquez sur une photo pour l’agrandir.</p>
    <div class="photo-grid" id="thumbnails"></div>
  </dialog>

  <dialog id="viewer" aria-label="Photographie agrandie">
    <div class="controls">
      <button id="prev" type="button" aria-label="Photo précédente">←</button>
      <span id="counter" aria-live="polite"></span>
      <button id="next" type="button" aria-label="Photo suivante">→</button>
      <button id="close" type="button">Fermer</button>
    </div>
    <img id="large" alt="">
  </dialog>

  <script>
    (() => {
      let photos = [];
      let index = 0;

      const viewer = document.getElementById('viewer');
      const grid = document.getElementById('grid-view');
      const large = document.getElementById('large');

      function show() {
        large.src = photos[index].src;
        large.alt = photos[index].alt;
        document.getElementById('counter').textContent =
          `${index + 1} / ${photos.length}`;
      }

      function move(step) {
        if (!photos.length) return;
        index = (index + step + photos.length) % photos.length;
        show();
      }

      document.querySelectorAll('.gallery').forEach(gallery => {
        const images = [...gallery.querySelectorAll('img')];
        if (!images.length) return;

        function openGallery() {
          photos = images;
          document.getElementById('grid-title').textContent =
            'Galerie — ' +
            gallery.closest('article').querySelector('h3').textContent;

          const thumbnails = document.getElementById('thumbnails');
          thumbnails.replaceChildren();

          images.forEach((image, i) => {
            const button = document.createElement('button');
            button.type = 'button';
            button.setAttribute('aria-label', `Agrandir la photo ${i + 1}`);

            const thumbnail = image.cloneNode();
            thumbnail.loading = 'eager';
            button.append(thumbnail);

            button.addEventListener('click', () => {
              index = i;
              show();
              viewer.showModal();
            });

            thumbnails.append(button);
          });

          grid.showModal();
        }

        const button = document.createElement('button');
        button.type = 'button';
        button.className = 'gallery-open';
        button.textContent = `Voir la galerie (${images.length})`;
        button.addEventListener('click', openGallery);
        gallery.after(button);

        images.forEach(image => {
          image.addEventListener('click', openGallery);
        });
      });

      document.getElementById('grid-close').onclick = () => grid.close();
      document.getElementById('close').onclick = () => viewer.close();
      document.getElementById('prev').onclick = () => move(-1);
      document.getElementById('next').onclick = () => move(1);

      viewer.addEventListener('keydown', event => {
        if (event.key === 'ArrowRight') {
          event.preventDefault();
          move(1);
        }
        if (event.key === 'ArrowLeft') {
          event.preventDefault();
          move(-1);
        }
      });
    })();
  </script>
</body>
</html>
