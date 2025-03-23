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
