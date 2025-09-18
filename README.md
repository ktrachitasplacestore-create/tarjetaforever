<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8" />
    <link rel="icon" href="https://placehold.co/32x32/000000/FFFFFF?text=CB" /> <!-- Puedes cambiar este favicon -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="theme-color" content="#000000" />
    <meta name="description" content="Invitación interactiva para los quince años de Cristian Caleb Lombeida Garzón." />
    <meta name="keywords" content="quince años, Cristian Caleb, invitación, fiesta, cumpleaños, Shushufindi, Ecuador" />
    <meta property="og:title" content="¡Estás Invitado! Los Quince Años de Cristian Caleb" />
    <meta property="og:description" content="Prepárate para un momento mágico: la celebración de los quince años de Cristian Caleb Lombeida Garzón." />
    <meta property="og:image" content="https://placehold.co/1200x630/000000/FFFFFF?text=Invitacion+Cristian+Caleb" /> <!-- Imagen de marcador de posición -->
    <meta property="og:url" content="https://your-invitation-url.netlify.app" /> <!-- Reemplaza con la URL real -->
    <meta name="twitter:card" content="summary_large_image" />
    <title>Los XV de Cristian Caleb</title>

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <!-- Inter font from Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet" />

    <!-- Custom CSS for neon effects and animations -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* eliminate luminosity for neon effects */
        .neon-text {
            text-shadow: 0 0 2px #0ff, 0 0 4px #0ff, 0 0 8px #0ff; /* Valores reducidos */
        }

        .neon-text-large {
            text-shadow: 0 0 3px #0ff, 0 0 6px #0ff, 0 0 9px #0ff, 0 0 15px #0ff; /* Valores reducidos */
        }

        .neon-number {
            text-shadow: 0 0 2px #0ff, 0 0 4px #0ff, 0 0 6px #0ff; /* Valores reducidos */
        }

        /* Specific style for green neon text with less glow */
        .neon-text-green {
            text-shadow: 0 0 1px #84cc16, 0 0 2px #84cc16, 0 0 4px #84cc16; /* Brillo verde sutil */
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .animate-fadeIn {
            animation: fadeIn 1.5s ease-out forwards;
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 2px #0ff, 0 0 4px #0ff, 0 0 8px #0ff; } /* Valores reducidos */
            50% { text-shadow: 0 0 4px #0ff, 0 0 8px #0ff, 0 0 16px #0ff, 0 0 24px #0ff; } /* Valores reducidos */
        }
        .animate-glow {
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes slideUp {
            from { transform: translateY(50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .animate-slideUp {
            animation: slideUp 1s ease-out forwards;
        }
        .animate-slideUp.delay-1s {
            animation-delay: 1s;
        }

        @keyframes bounceIn {
            0% { transform: scale(0.5); opacity: 0; }
            50% { transform: scale(1.1); opacity: 1; }
            70% { transform: scale(0.9); }
            100% { transform: scale(1); }
        }
        .animate-bounceIn {
            animation: bounceIn 1s ease-out forwards;
        }

        @keyframes slideInDown {
            from { transform: translateY(-100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .animate-slideInDown {
            animation: slideInDown 1s ease-out forwards;
        }

        @keyframes slideInLeft {
            from { transform: translateX(-100px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        .animate-slideInLeft {
            animation: slideInLeft 1s ease-out forwards;
        }

        @keyframes slideInRight {
            from { transform: translateX(100px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        .animate-slideInRight {
            animation: slideInRight 1s ease-out forwards;
        }

        @keyframes slideInUp {
            from { transform: translateY(100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .animate-slideInUp {
            animation: slideInUp 1s ease-out forwards;
        }

        @keyframes zoomIn {
            from { transform: scale(0.8); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }
        .animate-zoomIn {
            animation: zoomIn 0.8s ease-out forwards;
        }
        .animate-zoomIn.delay-0.2s { animation-delay: 0.2s; }
        .animate-zoomIn.delay-0.4s { animation-delay: 0.4s; }
        .animate-zoomIn.delay-0.6s { animation-delay: 0.6s; }

        /* Aspect Ratio for iframe */
        .aspect-w-16 {
            position: relative;
            width: 100%;
        }
        .aspect-w-16::before {
            content: '';
            display: block;
            padding-top: calc(var(--aspect-h, 9) / var(--aspect-w, 16) * 100%);
        }
        .aspect-w-16 > :first-child {
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
            width: 100%;
        }
        .aspect-h-9 {
            --aspect-h: 9;
        }
    </style>
</head>
<body>
    <noscript>Necesitas habilitar JavaScript para ver esta invitación.</noscript>
    <div id="root"></div>

    <!-- React and ReactDOM CDNs -->
    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <!-- Babel for JSX transformation -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <script type="text/babel">
        const { useState, useEffect } = React;

        // Main App Component
        const App = () => {
          const [showWelcome, setShowWelcome] = useState(true);
          const [countdown, setCountdown] = useState({
            days: 0,
            hours: 0,
            minutes: 0,
            seconds: 0,
          });
          const eventDate = new Date('2025-07-25T19:00:00'); // July 25, 2025, 7 PM (19:00)

          useEffect(() => {
            // Function to calculate countdown
            const calculateCountdown = () => {
              // Set the target date and time in the specified timezone (Puyo, Pastaza, Ecuador - UTC-5)
              // Note: JavaScript Date objects are based on the local time zone of the user's browser.
              // To ensure accuracy for a specific timezone, we can calculate the difference.
              // For a robust solution in production, consider a library like `moment-timezone`.
              // For this example, we'll assume the client's clock is reasonably synced or
              // adjust for a fixed offset. Puyo is UTC-5.
              const now = new Date();
              const targetTime = eventDate.getTime();
              const currentTime = now.getTime();

              const timeDifference = targetTime - currentTime;

              if (timeDifference <= 0) {
                setCountdown({ days: 0, hours: 0, minutes: 0, seconds: 0 });
                return;
              }

              const seconds = Math.floor((timeDifference / 1000) % 60);
              const minutes = Math.floor((timeDifference / (1000 * 60)) % 60);
              const hours = Math.floor((timeDifference / (1000 * 60 * 60)) % 24);
              const days = Math.floor(timeDifference / (1000 * 60 * 60 * 24));

              setCountdown({ days, hours, minutes, seconds });
            };

            // Update countdown every second
            const interval = setInterval(calculateCountdown, 1000);

            // Initial calculation
            calculateCountdown();

            // Cleanup interval on component unmount
            return () => clearInterval(interval);
          }, []);

          const handleEnterClick = () => {
            setShowWelcome(false);
            // Optional: Play background music here
            // const audio = new Audio('path/to/your/music.mp3');
            // audio.play();
          };

          const userPhotos = [
  "foto1.jpeg",
  "foto2.jpeg",
  "foto3.jpeg",
  "foto4.jpeg",
  "foto5.jpeg",
  "foto6.jpeg"
];

          return (
            <div className="min-h-screen bg-gray-950 text-white font-inter antialiased flex flex-col items-center justify-center overflow-x-hidden">
              {/* Welcome Screen */}
              {showWelcome ? (
                <div className="welcome-screen flex flex-col items-center justify-center text-center p-6 bg-gray-950 w-full h-screen animate-fadeIn">
                  <h1 className="text-5xl md:text-7xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-purple-600 mb-4 animate-glow">
                    ¡Hola!
                  </h1>
                  <p className="text-xl md:text-2xl text-gray-300 mb-8 animate-slideUp">
                    Este detalle es para ti :)
                  </p>
                  <p className="text-2xl md:text-4xl font-semibold text-white leading-relaxed max-w-4xl animate-slideUp delay-1s neon-text">
                    ⚽​El viernes 25 de julio de 2025 nuestro crack favorito pelotero imparable, mente brillante y campeón absoluto de hacernos reír, cumple 15 gloriosos años. Sus orgullosísimos padres, Criss y Gaby, ya no cabemos de emoción y queremos celebrarlo por todo lo alto.⚽​
                  </p>
                  <button
                    onClick={handleEnterClick}
                    className="mt-12 px-10 py-4 bg-gradient-to-r from-blue-600 to-purple-700 text-white text-xl font-bold rounded-full shadow-lg hover:shadow-blue-500/50 transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-4 focus:ring-blue-500/50 animate-bounceIn"
                  >
                    CLICK AQUÍ
                  </button>
                </div>
              ) : (
                // Main Invitation Content
                <div className="main-invitation w-full max-w-5xl mx-auto p-6 md:p-10 lg:p-12 animate-fadeIn delay-1s">
                  {/* Header Section */}
                  <header className="text-center mb-16 mt-8">
                    <h1 className="text-5xl md:text-7xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-600 mb-4 neon-text-large animate-slideInDown">
                      Mis Quince Años
                    </h1>
                    {/* Name changed to green color */}
                    <h2 className="text-4xl md:text-5xl font-bold text-lime-400 mb-2 neon-text-green animate-slideInLeft">
                      Cristian Caleb
                    </h2>
                    <p className="text-2xl md:text-3xl text-lime-400 neon-text-green animate-slideInRight">
                      Lombeida Garzón
                    </p>
                    <p className="text-xl md:text-2xl text-gray-400 mt-4 animate-fadeIn delay-1s">
                      25 de julio del 2025
                    </p>
                  </header>

                  {/* Countdown Section */}
                  <section className="mb-16 text-center">
                    <h3 className="text-3xl md:text-4xl font-semibold text-blue-400 mb-8 neon-text animate-slideInUp">
                      ¡Cuenta Regresiva!
                    </h3>
                    <div className="grid grid-cols-2 md:grid-cols-4 gap-6">
                      <div className="countdown-item bg-gray-800 p-6 rounded-xl shadow-xl border border-blue-600 animate-zoomIn">
                        <p className="text-5xl md:text-6xl font-bold text-cyan-300 neon-number">{countdown.days}</p>
                        <p className="text-lg md:text-xl text-gray-400 mt-2">Días</p>
                      </div>
                      <div className="countdown-item bg-gray-800 p-6 rounded-xl shadow-xl border border-purple-600 animate-zoomIn delay-0.2s">
                        <p className="text-5xl md:text-6xl font-bold text-cyan-300 neon-number">{countdown.hours}</p>
                        <p className="text-lg md:text-xl text-gray-400 mt-2">Horas</p>
                      </div>
                      <div className="countdown-item bg-gray-800 p-6 rounded-xl shadow-xl border border-blue-600 animate-zoomIn delay-0.4s">
                        <p className="text-5xl md:text-6xl font-bold text-cyan-300 neon-number">{countdown.minutes}</p>
                        <p className="text-lg md:text-xl text-gray-400 mt-2">Minutos</p>
                      </div>
                      <div className="countdown-item bg-gray-800 p-6 rounded-xl shadow-xl border border-purple-600 animate-zoomIn delay-0.6s">
                        <p className="text-5xl md:text-6xl font-bold text-cyan-300 neon-number">{countdown.seconds}</p>
                        <p className="text-lg md:text-xl text-gray-400 mt-2">Segundos</p>
                      </div>
                    </div>
                  </section>

                  {/* Event Details Section */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-blue-700 animate-slideInLeft">
                    <h3 className="text-3xl md:text-4xl font-semibold text-blue-400 mb-6 neon-text">
                      Detalles del Evento
                    </h3>
                    <div className="space-y-6 text-gray-300 text-lg">
                      <p className="flex items-center">
                        <i className="fas fa-map-marker-alt text-purple-400 mr-3 text-2xl"></i>
                        <span className="font-semibold text-xl">Lugar:</span> Complejo Turístico Apikai
                      </p>
                      <p className="flex items-center">
                        <i className="fas fa-clock text-purple-400 mr-3 text-2xl"></i>
                        <span className="font-semibold text-xl">Hora:</span> A partir de las 19:00 horas
                      </p>
                      <div className="flex items-start">
                        <i className="fas fa-directions text-purple-400 mr-3 text-2xl mt-1"></i>
                        <div>
                          <span className="font-semibold text-xl block">Dirección:</span>
                          <p>
                            Shushufindi kilómetro 12 vía a Miss Ecuador
                          </p>
                          <a
                            href="https://www.google.com/maps/search/?api=1&query=Complejo+Tur%C3%ADstico+Apikai,+Shushufindi,+kil%C3%B3metro+12+v%C3%ADa+a+Miss+Ecuador"
                            target="_blank"
                            rel="noopener noreferrer"
                            className="text-blue-500 hover:underline mt-2 inline-block transition-colors duration-300 hover:text-blue-400"
                          >
                            Ver en Google Maps <i className="fas fa-external-link-alt ml-1 text-sm"></i>
                          </a>
                        </div>
                      </div>
                    </div>
                  </section>

                  {/* Dress Code Section */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-purple-700 animate-slideInRight">
                    <h3 className="text-3xl md:text-4xl font-semibold text-purple-400 mb-6 neon-text">
                      Código de Vestimenta
                    </h3>
                    <p className="text-xl text-gray-300">
                      Te invitamos a vestir <span className="font-bold text-cyan-300">Formal</span> para esta ocasión especial.
                    </p>
                  </section>

                  {/* Gift Suggestions Section */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-purple-700 animate-slideInLeft">
                    <h3 className="text-3xl md:text-4xl font-semibold text-purple-400 mb-6 neon-text">
                      Sugerencia de Regalos
                    </h3>
                    <p className="text-xl text-gray-300">
                      Tu presencia es nuestro mayor obsequio. Si deseas brindarnos un detalle, los regalos serán recibidos con gratitud en sobre cerrado.
                    </p>
                  </section>

                  {/* Photo Gallery Section */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-blue-700 animate-slideInRight">
                    <h3 className="text-3xl md:text-4xl font-semibold text-blue-400 mb-6 neon-text">
                      Galería de Fotos
                    </h3>
                    <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                      {/* Las fotos de usuario irán aquí. Reemplaza las URLs de marcador de posición en el array userPhotos de arriba con tus URLs de imagen reales. */}
                      {userPhotos.map((imageUrl, index) => (
                        <div key={index} className="rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300 flex items-center justify-center">
                          <img
                            src={`images/${imageUrl}`} /* Se asume que las imágenes están en la carpeta 'images/' */
                            alt={`Cristian Caleb ${index + 1}`}
                            className="w-full h-48 object-contain rounded-lg" /* Altura original h-48, object-contain para ajustar */
                            loading="lazy" /* Carga perezosa para imágenes */
                            onError={(e) => { e.target.onerror = null; e.target.src = 'https://placehold.co/400x300/1a202c/a0aec0?text=Error+Carga'; }} /* Fallback para imágenes rotas */
                          />
                        </div>
                      ))}
                    </div>
                    <p className="text-center text-gray-400 text-sm mt-6">
                      ¡Momentos especiales capturados!
                    </p>
                  </section>

                            {/* Personalized Message Section */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-blue-700 animate-slideInLeft">
                    <h3 className="text-3xl md:text-4xl font-semibold text-blue-400 mb-6 neon-text">
                      Un Mensaje Especial
                    </h3>
                    <p className="text-xl text-gray-300 leading-relaxed italic">
                      Estimados familiares y amigos:
Nos llena de profunda alegría y gratitud invitarles a la celebración del décimo quinto cumpleaños de nuestro amado hijo, Cristian Caleb Lombeida Garzón. Ha sido un privilegio acompañar su crecimiento y verlo convertirse en el joven excepcional que es hoy un muchacho cuya inteligencia, energía y calidez iluminan nuestra vida cada día.
Deseamos compartir este hito tan significativo con quienes han sido testigos y parte esencial de su historia. Su presencia hará de esta ocasión un recuerdo imborrable para Cristian y para toda nuestra familia.
Gracias, de corazón, por el cariño, la guía y el apoyo que siempre nos han brindado. Esperamos contar con su compañía para celebrar juntos este momento tan especial.
Con sincero agradecimiento,
Criss & Gaby
                    </p>
                    <p className="text-right text-gray-400 mt-4 text-lg font-semibold">
                      Con cariño, <br />
                      La Familia Lombeida Garzón
                    </p>
                  </section>

                  {/* Music Playlist Section */}
<section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-purple-700 animate-slideInUp">
  <h3 className="text-3xl md:text-4xl font-semibold text-purple-400 mb-6 neon-text">
    Cancion favorita de Caleb
  </h3>
  <div className="aspect-w-16 aspect-h-9 w-full rounded-lg overflow-hidden shadow-xl">
    <iframe
      style={{ borderRadius: '12px' }}
      src="https://open.spotify.com/embed/track/7D0RhFcb3CrfPuTJ0obrod?utm_source=generator&theme=0&autoplay=1"
      width="100%"
      height="352"
      frameBorder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
      allowFullScreen
      loading="lazy"
      className="rounded-lg"
    ></iframe>
  </div>
  <p className="text-center text-gray-400 text-sm mt-6">
    ¡Prepárate para disfrutar con Coldplay!
  </p>
</section>
          
{/* RSVP Section - Google Form Embed */}
                  <section className="mb-16 bg-gray-800 p-8 rounded-xl shadow-xl border border-blue-700 animate-slideInUp">
                    <h3 className="text-3xl md:text-4xl font-semibold text-blue-400 mb-6 neon-text">
                      Confirma tu Asistencia (RSVP)
                    </h3>
                    <p className="text-lg text-gray-300 mb-6">
                      Por favor, ayúdanos a planificar este día tan importante confirmando tu asistencia antes del <span className="font-semibold text-cyan-300">20 de julio del 2025</span>.
                    </p>
                    <div className="w-full max-w-full overflow-hidden rounded-lg shadow-lg" style={{backgroundColor: '#1a202c'}}> {/* Contenedor con fondo oscuro */}
                      <iframe
                        src="https://docs.google.com/forms/d/e/1FAIpQLSd9NlyAz8PZffB1SAozcF-35tODMd0-cMv0pcRyXBUcfmkHcQ/viewform?embedded=true"
                        width="100%"
                        height="1052"
                        frameBorder="0"
                        marginHeight="0"
                        marginWidth="0"
                        className="rounded-lg"
                        style={{backgroundColor: 'transparent'}} /* Intento de hacer el fondo del iframe transparente */
                      >
                        Cargando…
                      </iframe>
                    </div>
                    <p className="text-center text-gray-400 text-sm mt-6">
                      Para cualquier duda, por favor contáctanos.
                    </p>
                  </section>
                    
                  {/* Footer */}
                  <footer className="text-center text-gray-500 text-sm mt-16">
                    <p>&copy; 2025 Los Quince Años de Cristian Caleb. Todos los derechos reservados.</p>
                  </footer>
                </div>
              )}
            </div>
          );
        };

        ReactDOM.createRoot(document.getElementById('root')).render(<App />);
    </script>
</body>
</html>
