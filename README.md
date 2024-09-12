# curso-autocad-2d
curso de autocad 2d archivos
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapa Mental Detallado de AutoCAD 2D</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .mind-map {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .toolbar {
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            cursor: pointer;
        }
        .tool {
            background-color: #2196F3;
            color: white;
            padding: 10px;
            margin: 5px 0;
            border-radius: 5px;
            cursor: pointer;
        }
        .options {
            background-color: #FFC107;
            padding: 10px;
            margin: 5px 0;
            border-radius: 5px;
        }
        .hidden {
            display: none;
        }
        .toolbar::after, .tool::after {
            content: " [+]";
            float: right;
        }
        .expanded::after {
            content: " [-]";
        }
    </style>
</head>
<body>
    <div class="mind-map">
        <h1>Mapa Mental Detallado de AutoCAD 2D</h1>
        
        <div class="toolbar" onclick="toggle(this)">
            Dibujo / Draw
            <div class="hidden">
                <p>Descripción: Esta barra contiene herramientas para crear objetos geométricos básicos.</p>
                
                <div class="tool" onclick="toggle(this, event)">
                    Línea / Line
                    <div class="hidden">
                        <p>Descripción: Crea líneas rectas.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Desde punto (From point): Especifica el punto de inicio.</li>
                                <li>A punto (To point): Especifica el punto final.</li>
                                <li>Deshacer (Undo): Elimina el último segmento dibujado.</li>
                                <li>Cerrar (Close): Cierra el polígono conectando el último punto con el primero.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="tool" onclick="toggle(this, event)">
                    Círculo / Circle
                    <div class="hidden">
                        <p>Descripción: Dibuja círculos.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Centro, Radio (Center, Radius): Especifica el centro y luego el radio.</li>
                                <li>Centro, Diámetro (Center, Diameter): Especifica el centro y luego el diámetro.</li>
                                <li>2 Puntos (2 Points): Define el círculo por dos puntos del diámetro.</li>
                                <li>3 Puntos (3 Points): Define el círculo por tres puntos de su circunferencia.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="tool" onclick="toggle(this, event)">
                    Arco / Arc
                    <div class="hidden">
                        <p>Descripción: Crea arcos circulares.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>3 Puntos (3 Points): Define el arco por punto inicial, punto intermedio y punto final.</li>
                                <li>Inicio, Centro, Fin (Start, Center, End): Especifica punto inicial, centro y punto final.</li>
                                <li>Inicio, Centro, Ángulo (Start, Center, Angle): Define por punto inicial, centro y ángulo.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="toolbar" onclick="toggle(this)">
            Modificar / Modify
            <div class="hidden">
                <p>Descripción: Contiene herramientas para editar y transformar objetos existentes.</p>
                
                <div class="tool" onclick="toggle(this, event)">
                    Copiar / Copy
                    <div class="hidden">
                        <p>Descripción: Duplica objetos seleccionados.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Selección de objetos (Select objects): Elige los objetos a copiar.</li>
                                <li>Punto base (Base point): Especifica un punto de referencia.</li>
                                <li>Punto de desplazamiento (Displacement point): Define dónde se colocará la copia.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="tool" onclick="toggle(this, event)">
                    Mover / Move
                    <div class="hidden">
                        <p>Descripción: Desplaza objetos de un lugar a otro.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Selección de objetos (Select objects): Elige los objetos a mover.</li>
                                <li>Punto base (Base point): Especifica un punto de referencia en los objetos.</li>
                                <li>Punto de desplazamiento (Displacement point): Define el nuevo lugar para los objetos.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="tool" onclick="toggle(this, event)">
                    Escala / Scale
                    <div class="hidden">
                        <p>Descripción: Cambia el tamaño de los objetos.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Selección de objetos (Select objects): Elige los objetos a escalar.</li>
                                <li>Punto base (Base point): Especifica el punto de referencia para el escalado.</li>
                                <li>Factor de escala (Scale factor): Define cuánto aumentará o disminuirá el tamaño.</li>
                                <li>Referencia (Reference): Permite escalar basándose en una longitud de referencia.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="toolbar" onclick="toggle(this)">
            Capas / Layers
            <div class="hidden">
                <p>Descripción: Permite organizar y gestionar las capas del dibujo.</p>
                
                <div class="tool" onclick="toggle(this, event)">
                    Propiedades de Capa / Layer Properties
                    <div class="hidden">
                        <p>Descripción: Abre el administrador de propiedades de capas.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Nueva capa (New layer): Crea una nueva capa.</li>
                                <li>Eliminar capa (Delete layer): Borra una capa existente.</li>
                                <li>Establecer corriente (Set current): Define la capa activa para dibujar.</li>
                                <li>On/Off: Activa o desactiva la visibilidad de la capa.</li>
                                <li>Freeze/Thaw: Congela o descongela capas para mejorar el rendimiento.</li>
                                <li>Lock/Unlock: Bloquea o desbloquea capas para prevenir modificaciones.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="toolbar" onclick="toggle(this)">
            Acotar / Dimension
            <div class="hidden">
                <p>Descripción: Contiene herramientas para añadir dimensiones y medidas al dibujo.</p>
                
                <div class="tool" onclick="toggle(this, event)">
                    Cota Lineal / Linear Dimension
                    <div class="hidden">
                        <p>Descripción: Crea cotas lineales horizontales o verticales.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Primer punto de extensión (First extension line origin): Define el inicio de la medida.</li>
                                <li>Segundo punto de extensión (Second extension line origin): Define el final de la medida.</li>
                                <li>Ubicación de línea de cota (Dimension line location): Especifica dónde se colocará la línea de cota.</li>
                                <li>Texto de cota (Dimension text): Permite editar el texto de la cota.</li>
                                <li>Ángulo de texto (Text angle): Ajusta el ángulo del texto de la cota.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="tool" onclick="toggle(this, event)">
                    Cota Alineada / Aligned Dimension
                    <div class="hidden">
                        <p>Descripción: Crea cotas paralelas a los objetos medidos.</p>
                        <div class="options">
                            Opciones:
                            <ul>
                                <li>Primer punto de extensión (First extension line origin): Define el inicio de la medida.</li>
                                <li>Segundo punto de extensión (Second extension line origin): Define el final de la medida.</li>
                                <li>Ubicación de línea de cota (Dimension line location): Especifica dónde se colocará la línea de cota.</li>
                                <li>Texto de cota (Dimension text): Permite editar el texto de la cota.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>

    <script>
        function toggle(element, event) {
            if (event) {
                event.stopPropagation();
            }
            const content = element.querySelector(':scope > div');
            content.classList.toggle('hidden');
            element.classList.toggle('expanded');
        }
    </script>
</body>
</html>
