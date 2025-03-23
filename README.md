# Cotopaxierupci-n
Esta es una pagina web dedicada a la investigación de este volcán.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SIATC Latacunga</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
</head>
<body>
    <header>
        <div class="header-content">
            <h1>SIATC Latacunga</h1>
            <nav>
                <button data-section="inicio">Inicio</button>
                <button data-section="informacion">Información</button>
                <button data-section="alertas">Alertas</button>
                <button data-section="mapa">Mapa de Riesgo</button>
                <button data-section="comunicacion">Comunicación</button>
                <button data-section="kit-emergencia">Kit Emergencia</button>
            </nav>
        </div>
    </header>
    <main>
        <section id="inicio" class="active">
            <h2>¡Prepárate para el Cotopaxi!</h2>
            <div id="volcan-image">
                <img src="https://www.elpais.cr/wp-content/uploads/2023/09/Volcan-Cotopaxi.jpg" alt="Volcán Cotopaxi">
            </div>
            <p>Mantente informado y preparado ante la actividad del volcán Cotopaxi. El SIATC te proporciona información en tiempo real y herramientas para tu seguridad.</p>
            <div class="volcan-buttons">
                <button data-section="informacion">Información</button>
                <button data-section="alertas">Alertas</button>
                <button data-section="mapa">Mapa de Riesgo</button>
                <button data-section="comunicacion">Comunicación</button>
                <button data-section="kit-emergencia">Kit Emergencia</button>
            </div>
        </section>

        <section id="informacion" class="hidden">
            <h2>Información Crítica</h2>
            <div id="info-content">
                <h3>Zonas de Riesgo</h3>
                <ul>
                    <li>**La Vega:** Alto riesgo de lahares y flujos piroclásticos.</li>
                    <li>**Alaquez:** Alto riesgo de lahares y flujos piroclásticos.</li>
                    <li>**...** (Agrega más zonas de riesgo)</li>
                </ul>

                <h3>Zonas Seguras</h3>
                <ul>
                    <li>**Centro Histórico:** Zona relativamente segura en caso de erupción.</li>
                    <li>**Terrenos Altos:** Zonas elevadas con menor riesgo de lahares.</li>
                    <li>**...** (Agrega más zonas seguras)</li>
                </ul>

                <h3>Recomendaciones</h3>
                <ul>
                    <li>Mantente informado sobre las alertas y comunicados oficiales.</li>
                    <li>Prepara un kit de emergencia con los artículos esenciales.</li>
                    <li>Identifica las rutas de evacuación y zonas seguras cercanas.</li>
                    <li>Participa en simulacros y capacitaciones sobre gestión de riesgos.</li>
                    <li>Mantén la calma y sigue las indicaciones de las autoridades.</li>
                </ul>
            </div>
        </section>

        <section id="alertas" class="hidden">
            <h2>Alertas en Tiempo Real</h2>
            <div id="alert-content">
                <div id="alert-level"></div>
                <div id="seismic-activity"></div>
                <div id="gas-emissions"></div>
                <div id="latest-updates"></div>
            </div>
        </section>

        <section id="mapa" class="hidden">
            <h2>Mapa de Riesgo de Latacunga</h2>
            <div id="map"></div>
            <div id="map-controls">
                <div id="risk-scale">
                    <h3>Escala de Riesgo:</h3>
                    <ul>
                        <li><span class="high-risk">Rojo:</span> Alto riesgo (lahares, flujos piroclásticos)</li>
                        <li><span class="medium-risk">Naranja:</span> Riesgo moderado (caída de ceniza, flujos de lodo secundarios)</li>
                        <li><span class="low-risk">Amarillo:</span> Bajo riesgo (caída leve de ceniza)</li>
                        <li><span class="safe-zone">Verde:</span> Zona segura</li>
                    </ul>
                </div>
                <div id="compass">
                    <h3>Brújula:</h3>
                    <div id="compass-arrow"></div>
                </div>
                <div id="safe-zone-finder">
                    <h3>Encuentra la Zona Segura Más Cercana</h3>
                    <button id="find-safe-zone-btn">Buscar</button>
                    <p id="nearest-safe-zone"></p>
                    <div id="route-map"></div>
                </div>
            </div>
        </section>

        <section id="comunicacion" class="hidden">
            <h2>Comunicación</h2>
            <p>En caso de emergencia, contacta al <strong>911 Ecuador</strong>.</p>
            <p><strong>Otros contactos:</strong></p>
            <ul>
                <li><strong>ECU 911:</strong> 911</li>
                <li><strong>Bomberos Latacunga:</strong> 102</li>
                <li><strong>Policía Nacional:</strong> 101</li>
                <li><strong>Cruz Roja:</strong> 131</li>
            </ul>
            <p>También puedes contactarnos a través de nuestro formulario de contacto:</p>
            <form id="contact-form">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" placeholder="Nombre">
                <label for="email">Correo electrónico:</label>
                <input type="email" id="email" name="email" placeholder="Correo electrónico">
                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" placeholder="Mensaje"></textarea>
                <button type="submit">Enviar</button>
            </form>
        </section>

        <section id="kit-emergencia" class="hidden">
            <h2>Kit de Emergencia para Erupción del Cotopaxi</h2>
            <p>Prepara este kit esencial para protegerte a ti y a tu familia en caso de una erupción volcánica:</p>
            <div id="kit-items">
                <div class="kit-item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSOw7_Kg7doHRNm12SBRultC20oAVfHPNsFrQ&s" alt="Agua">
                    <h3>Agua Potable</h3>
                    <p>Mínimo 3 litros por persona para 3 días.</p>
                    <button class="ejemplos-btn" data-ejemplos="agua">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ1qbE3On13sZKC8ujO9zr-d0nTez1aoTezmQ&s" alt="Comida">
                    <h3>Comida No Perecedera</h3>
                    <p>Latas de conserva, barras energéticas, etc.</p>
                    <button class="ejemplos-btn" data-ejemplos="comida">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRK8fochvn-E4rQmA1fhZ5jdYPmbVtmYGKUPg&s" alt="Mascarillas">
                    <h3>Mascarillas N95</h3>
                    <p>Para protegerte de la ceniza y gases volcánicos.</p>
                    <button class="ejemplos-btn" data-ejemplos="mascarillas">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSaXBBE2h1oyt5xaGt1kDK2xaNM99WlQn93bw&s" alt="Gafas">
                    <h3>Gafas de Protección</h3>
                    <p>Para proteger tus ojos de la ceniza y partículas.</p>
                    <button class="ejemplos-btn" data-ejemplos="gafas">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://kywiec.vtexassets.com/arquivos/ids/179468-800-auto?v=638388675229100000&width=800&height=auto&aspect=true" alt="Linterna">
                    <h3>Linterna y Baterías</h3>
                    <p>Para iluminar en caso de cortes de energía.</p>
                    <button class="ejemplos-btn" data-ejemplos="linterna">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://ecuadorgps.com/wp-content/uploads/2018/01/Radios-Motorola-T400.jpg" alt="Radio">
                    <h3>Radio Portátil</h3>
                    <p>Para mantenerte informado sobre las alertas.</p>
                    <button class="ejemplos-btn" data-ejemplos="radio">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://static.wixstatic.com/media/544eb7_b70622c0dfc9431a9524b123e42e2182~mv2.jpg/v1/fill/w_598,h_595,al_c,lg_1,q_80/544eb7_b70622c0dfc9431a9524b123e42e2182~mv2.jpg" alt="Botiquín">
                    <h3>Botiquín de Primeros Auxilios</h3>
                    <p>Con medicamentos básicos y artículos de curación.</p>
                    <button class="ejemplos-btn" data-ejemplos="botiquin">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS78UdZZ91AjCkkvMMIX63l6rI6vJJYgzC67CRG27GcxSoW3O0RdnolBftoLKvsdivfz60&usqp=CAU" alt="Ropa">
                    <h3>Ropa y Mantas</h3>
                    <p>Ropa abrigada y mantas para protegerte del frío.</p>
                    <button class="ejemplos-btn" data-ejemplos="ropa">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://www.lahora.com.ec/wp-content/uploads/2022/03/cedulas-caducadas.jpeg" alt="Documentos">
                    <h3>Documentos Importantes</h3>
                    <p>Copias de cédulas, escrituras, etc. en una bolsa impermeable.</p>
                    <button class="ejemplos-btn" data-ejemplos="documentos">Ejemplos</button>
                </div>
                <div class="kit-item">
                    <img src="https://espanol.mycreditunion.gov/sites/default/files/2024-10/dollars-coins.jpg" alt="Dinero en efectivo">
                    <h3>Dinero en Efectivo</h3>
                    <p>Para compras en caso de que los cajeros no funcionen.</p>
                    <button class="ejemplos-btn" data-ejemplos="dinero">Ejemplos</button>
                </div>
            </div>
        </section>
    </main>
    <footer>
        <p>Contacto: info@siatclatacunga.com</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
/* --- Estilos Generales --- */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; /* Fuente moderna */
    margin: 0;
    line-height: 1.6;
    background-color: #f8f9fa; /* Gris claro suave */
    color: #343a40; /* Gris oscuro */
}

/* --- Encabezado --- */
header {
    background-color: #dc3545; /* Rojo Bootstrap */
    color: white;
    padding: 1rem 2rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

.header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
}

/* --- Navegación --- */
nav button {
    background-color: #e9ecef; /* Gris muy claro */
    color: #495057; /* Gris un poco más oscuro */
    padding: 0.5rem 1rem;
    border: none;
    cursor: pointer;
    margin-left: 0.5rem;
    border-radius: 0.25rem;
    transition: background-color 0.3s ease;
}

nav button:hover {
    background-color: #dee2e6; /* Gris claro */
}

/* --- Contenido Principal --- */
main {
    padding: 2rem;
    max-width: 1200px;
    margin: 2rem auto;
}

section {
    margin-bottom: 2rem;
    background-color: white;
    padding: 1.5rem;
    border-radius: 0.5rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

section.active {
    display: block;
}

.hidden {
    display: none;
}

/* --- Mapa --- */
#map {
    height: 500px;
    width: 100%;
    border-radius: 0.5rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

#map-controls {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 1rem;
}

/* --- Escala de Riesgo, Brújula, Buscador de Zonas Seguras --- */
#risk-scale,
#compass,
#safe-zone-finder {
    width: 30%;
    margin-bottom: 1rem;
}

#risk-scale ul {
    list-style: none;
    padding: 0;
}

#risk-scale li {
    display: inline-block;
    margin-right: 0.5rem;
}

.high-risk { color: red; }
.medium-risk { color: orange; }
.low-risk { color: yellow; }
.safe-zone { color: green; }

/* --- Brújula --- */
#compass { text-align: center; }

#compass-arrow {
    width: 50px;
    height: 50px;
    background-image: url('compass-arrow.png'); /* Reemplaza */
    background-size: contain;
    background-repeat: no-repeat;
    margin: 0 auto;
    transition: transform 0.5s ease;
}

/* --- Buscador de Zonas Seguras --- */
#safe-zone-finder { margin-top: 1rem; }

#route-map {
    height: 300px;
    width: 100%;
    margin-top: 0.5rem;
    border-radius: 0.5rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

/* --- Formulario de Contacto --- */
#contact-form input,
#contact-form textarea {
    width: 100%;
    padding: 0.5rem;
    margin-bottom: 0.5rem;
    border: 1px solid #ced4da; /* Gris borde Bootstrap */
    border-radius: 0.25rem;
}

#contact-form button {
    background-color: #28a745; /* Verde Bootstrap */
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    cursor: pointer;
    border-radius: 0.25rem;
    transition: background-color 0.3s ease;
}

#contact-form button:hover {
    background-color: #218838; /* Verde oscuro Bootstrap */
}

/* --- Animación del Volcán --- */
#volcan-animation {
    width: 200px;
    height: 200px;
    background-image: url('volcan-animation.gif'); /* Reemplaza */
    background-size: contain;
    background-repeat: no-repeat;
    margin: 1rem auto;
}

/* --- Información y Alertas --- */
#info-content,
#alert-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

#info-content div,
#alert-content div {
    width: 48%;
    margin-bottom: 1rem;
    padding: 1rem;
    background-color: #f8f9fa; /* Gris claro suave */
    border-radius: 0.5rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

/* --- Alertas --- */
#alert-content div { width: 100%; }

#alert-level {
    background-color: #ffc107; /* Amarillo Bootstrap */
    padding: 0.75rem;
    border-radius: 0.25rem;
    font-weight: bold;
}

#alert-level.high { background-color: #dc3545; color: white; }
#alert-level.medium { background-color: #ffc107; }

/* --- Kit de Emergencia --- */
#kit-emergencia { text-align: center; }

#kit-items {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.kit-item {
    width: 200px;
    margin: 1rem;
    padding: 1rem;
    border: 1px solid #dee2e6; /* Gris borde Bootstrap */
    border-radius: 0.5rem;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

.kit-item img {
    width: 100px;
    height: 100px;
    object-fit: contain;
    margin-bottom: 0.5rem;
}

/* --- Botones de Ejemplos --- */
.ejemplos-btn {
    background-color: #28a745; /* Verde Bootstrap */
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    cursor: pointer;
    border-radius: 0.25rem;
    transition: background-color 0.3s ease;
    margin-top: 0.5rem;
}

.ejemplos-btn:hover {
    background-color: #218838; /* Verde oscuro Bootstrap */
}

/* --- Estilos Responsivos --- */
@media (max-width: 768px) {
    #map-controls,
    #info-content,
    #alert-content {
        flex-direction: column;
    }

    #risk-scale,
    #compass,
    #safe-zone
    #safe-zone-finder {
        width: 100%;
    }

    .kit-item {
        width: 48%;
    }
}

/* --- Pie de Página --- */
footer {
    text-align: center;
    padding: 1rem;
    background-color: #e9ecef; /* Gris muy claro */
    color: #6c757d; /* Gris medio */
    border-top: 1px solid #dee2e6; /* Gris borde Bootstrap */
}

/* --- Clases de utilidad --- */
.text-center { text-align: center; }
.text-danger { color: #dc3545; }
.text-success { color: #28a745; }
.text-warning { color: #ffc107; }
.mt-1 { margin-top: 0.25rem; }
.mt-2 { margin-top: 0.5rem; }
.mt-3 { margin-top: 1rem; }
.mt-4 { margin-top: 1.5rem; }
.mt-5 { margin-top: 3rem; }
.mb-1 { margin-bottom: 0.25rem; }
.mb-2 { margin-bottom: 0.5rem; }
.mb-3 { margin-bottom: 1rem; }
.mb-4 { margin-bottom: 1.5rem; }
.mb-5 { margin-bottom: 3rem; }
// --- Inicialización del Mapa ---
function initMap() {
    try {
        const latlng = [-0.935, -78.411]; // Latacunga
        const map = L.map('map').setView(latlng, 12);

        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; OpenStreetMap contributors'
        }).addTo(map);

        // Zonas de riesgo (ejemplo)
        const riskZones = [
            { lat: -0.94, lng: -78.42, risk: 'high', name: 'La Vega' },
            { lat: -0.95, lng: -78.43, risk: 'high', name: 'Alaquez' },
            // ... más zonas de riesgo
        ];

        riskZones.forEach(zone => {
            const iconUrl = getRiskIcon(zone.risk);
            L.marker([zone.lat, zone.lng], { icon: L.icon({ iconUrl }) })
                .addTo(map)
                .bindPopup(zone.name);
        });

        // Zonas seguras (ejemplo)
        const safeZones = [
            { lat: -0.925, lng: -78.405, name: 'Centro Histórico' },
            { lat: -0.915, lng: -78.41, name: 'Terrenos Altos' },
            // ... más zonas seguras
        ];

        safeZones.forEach(zone => {
            L.marker([zone.lat, zone.lng], { icon: L.icon({ iconUrl: 'http://maps.google.com/mapfiles/ms/icons/green-dot.png' }) })
                .addTo(map)
                .bindPopup(zone.name);
        });

        // Función para encontrar la zona segura más cercana
        window.findNearestSafeZone = () => findNearestSafeZoneFn(safeZones);

    } catch (error) {
        console.error('Error al inicializar el mapa:', error);
    }
}

// --- Funciones Auxiliares del Mapa ---
function getRiskIcon(risk) {
    const icons = {
        high: 'http://maps.google.com/mapfiles/ms/icons/red-dot.png',
        medium: 'http://maps.google.com/mapfiles/ms/icons/orange-dot.png',
        low: 'http://maps.google.com/mapfiles/ms/icons/yellow-dot.png'
    };
    return icons[risk] || icons.low; // Default a low risk
}

function findNearestSafeZoneFn(safeZones) {
    if (!navigator.geolocation) {
        alert('Geolocalización no soportada.');
        return;
    }

    navigator.geolocation.getCurrentPosition(position => {
        const userLocation = { lat: position.coords.latitude, lng: position.coords.longitude };
        let nearestZone = null;
        let nearestDist = Infinity;

        safeZones.forEach(zone => {
            const dist = L.latLng(userLocation.lat, userLocation.lng).distanceTo(L.latLng(zone.lat, zone.lng));
            if (dist < nearestDist) {
                nearestZone = zone;
                nearestDist = dist;
            }
        });

        document.getElementById('nearest-safe-zone').textContent = `Zona segura más cercana: ${nearestZone.name}`;
    }, () => alert('No se pudo obtener la ubicación.'));
}

// --- Carga de Datos ---
function loadInfoData() {
    try {
        document.getElementById('info-content').innerHTML = `
            <div>
                <h3>Zonas de Riesgo</h3>
                <ul>
                    <li>**La Vega:** Alto riesgo de lahares y flujos piroclásticos.</li>
                    <li>**Alaquez:** Alto riesgo de lahares y flujos piroclásticos.</li>
                    <li>**...** (Agrega más zonas de riesgo)</li>
                </ul>
            </div>
            <div>
                <h3>Zonas Seguras</h3>
                <ul>
                    <li>**Centro Histórico:** Zona relativamente segura en caso de erupción.</li>
                    <li>**Terrenos Altos:** Zonas elevadas con menor riesgo de lahares.</li>
                    <li>**...** (Agrega más zonas seguras)</li>
                </ul>
            </div>
            <div>
                <h3>Recomendaciones</h3>
                <ul>
                    <li>Mantente informado sobre las alertas y comunicados oficiales.</li>
                    <li>Prepara un kit de emergencia con los artículos esenciales.</li>
                    <li>Identifica las rutas de evacuación y zonas seguras cercanas.</li>
                    <li>Participa en simulacros y capacitaciones sobre gestión de riesgos.</li>
                    <li>Mantén la calma y sigue las indicaciones de las autoridades.</li>
                </ul>
            </div>
        `;
    } catch (error) {
        console.error('Error al cargar la info:', error);
    }
}

function loadAlertData() {
    try {
        const alertLevel = document.getElementById('alert-level');
        const seismicActivity = document.getElementById('seismic-activity');
        const gasEmissions = document.getElementById('gas-emissions');
        const latestUpdates = document.getElementById('latest-updates');

        const alertData = generateAlertData(); // Genera datos de alerta aleatorios
        updateAlertUI(alertData, alertLevel, seismicActivity, gasEmissions, latestUpdates);

        setInterval(() => {
            const newAlertData = generateAlertData();
            updateAlertUI(newAlertData, alertLevel, seismicActivity, gasEmissions, latestUpdates);
        }, 300000); // Actualiza cada 5 minutos

    } catch (error) {
        console.error('Error al cargar las alertas:', error);
    }
}

// --- Funciones Auxiliares de Alertas ---
function generateAlertData() {
    return {
        nivelAlerta: Math.random() < 0.2 ? 'Rojo' : Math.random() < 0.5 ? 'Naranja' : 'Amarillo',
        actividadSismica: Math.random() < 0.3 ? 'Alta' : 'Moderada',
        emisionesGas: Math.random() < 0.4 ? 'Altas' : 'Leves',
        ultimaActualizacion: new Date().toLocaleString()
    };
}

function updateAlertUI(data, levelEl, seismicEl, gasEl, updatesEl) {
    levelEl.textContent = `Nivel: ${data.nivelAlerta}`;
    seismicEl.textContent = `Sísmica: ${data.actividadSismica}`;
    gasEl.textContent = `Gases: ${data.emisionesGas}`;
    updatesEl.textContent = `Actualizado: ${data.ultimaActualizacion}`;

    levelEl.className = data.nivelAlerta === 'Rojo' ? 'high' : data.nivelAlerta === 'Naranja' ? 'medium' : '';
}
// --- Manejo de Secciones ---
function showSection(sectionId) {
    document.querySelectorAll('main section').forEach(sec => sec.classList.add('hidden'));
    const section = document.getElementById(sectionId);
    if (section) {
        section.classList.remove('hidden');
        if (sectionId === 'informacion') loadInfoData();
        if (sectionId === 'alertas') loadAlertData();
    }
}

// --- Ejemplos del Kit ---
function showKitExamples(kitItem) {
    const examples = {
        agua: 'Botellas, bidones, pastillas purificadoras.',
        comida: 'Latas de conserva, galletas energéticas, barras de cereal.',
        mascarillas: 'Mascarillas N95, KN95.',
        gafas: 'Gafas de seguridad industrial, antiparras.',
        linterna: 'Linterna de mano, frontal, dinamo.',
        radio: 'Radio AM/FM, radio con manivela.',
        botiquin: 'Analgésicos, vendas, gasas, alcohol, antisépticos.',
        ropa: 'Ropa abrigada, impermeable, zapatos resistentes.',
        documentos: 'Copias de cédulas, escrituras, pasaportes, documentos importantes.',
        dinero: 'Billetes de baja denominación, monedas.'
    };
    alert(`Ejemplos de ${kitItem}: ${examples[kitItem] || 'No disponibles.'}`);
}

// --- Event Listeners ---
document.addEventListener('DOMContentLoaded', () => {
    document.querySelectorAll('nav button, .volcan-buttons button').forEach(btn => {
        btn.addEventListener('click', () => showSection(btn.dataset.section));
    });

    document.querySelectorAll('.ejemplos-btn').forEach(btn => {
        btn.addEventListener('click', () => showKitExamples(btn.dataset.ejemplos));
    });

    initMap();
    loadAlertData();
    document.getElementById('find-safe-zone-btn').addEventListener('click', findNearestSafeZone);
});
