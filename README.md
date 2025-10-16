<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Protejamos la Infancia, Construyamos Futuro</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 30px rgba(0,0,0,0.2);
        }

        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 60px 20px;
            text-align: center;
        }

        header h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        nav {
            background: #333;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        nav ul li {
            margin: 5px 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            border-radius: 5px;
            transition: background 0.3s;
        }

        nav ul li a:hover {
            background: #667eea;
        }

        section {
            padding: 50px 30px;
            border-bottom: 1px solid #eee;
        }

        section:nth-child(even) {
            background: #f9f9f9;
        }

        h2 {
            color: #667eea;
            font-size: 2em;
            margin-bottom: 25px;
            border-left: 5px solid #764ba2;
            padding-left: 15px;
        }

        h3 {
            color: #764ba2;
            margin: 25px 0 15px 0;
            font-size: 1.5em;
        }

        .intro-text {
            font-size: 1.1em;
            line-height: 1.8;
            margin-bottom: 20px;
        }

        .case-study {
            background: #fff3cd;
            border-left: 5px solid #ffc107;
            padding: 20px;
            margin: 20px 0;
            border-radius: 5px;
        }

        .maltrato-tipos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .maltrato-card {
            background: white;
            border: 2px solid #667eea;
            border-radius: 10px;
            padding: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .maltrato-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.3);
        }

        .maltrato-card h4 {
            color: #667eea;
            margin-bottom: 10px;
        }

        .estrategia-box {
            background: linear-gradient(135deg, #e0c3fc 0%, #8ec5fc 100%);
            padding: 25px;
            margin: 20px 0;
            border-radius: 10px;
            border-left: 5px solid #667eea;
        }

        .estrategia-box h4 {
            color: #333;
            margin-bottom: 10px;
            font-size: 1.3em;
        }

        .ruta-paso {
            background: white;
            border: 2px solid #28a745;
            border-radius: 8px;
            padding: 20px;
            margin: 15px 0;
            position: relative;
            padding-left: 60px;
        }

        .ruta-paso::before {
            content: attr(data-step);
            position: absolute;
            left: 15px;
            top: 20px;
            background: #28a745;
            color: white;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        .btn-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 30px 0;
        }

        .btn {
            display: inline-block;
            padding: 15px 30px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1em;
        }

        .btn:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.5);
        }

        .btn-emergency {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }

        .btn-success {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        .recursos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .recurso-card {
            background: white;
            border: 2px solid #28a745;
            border-radius: 10px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s;
        }

        .recurso-card:hover {
            transform: translateY(-5px);
        }

        .recurso-card h4 {
            color: #28a745;
            margin-bottom: 15px;
        }

        .quote-box {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            padding: 30px;
            margin: 20px 0;
            border-radius: 10px;
            font-style: italic;
            font-size: 1.2em;
            text-align: center;
            border-left: 5px solid #ff6b6b;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        ul {
            margin: 15px 0 15px 30px;
        }

        ul li {
            margin: 10px 0;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8em;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
            }

            .ruta-paso {
                padding-left: 20px;
            }

            .ruta-paso::before {
                position: relative;
                left: 0;
                top: 0;
                margin-bottom: 10px;
            }
        }

        .nivel-box {
            background: #e3f2fd;
            padding: 15px;
            margin: 10px 0;
            border-radius: 5px;
            border-left: 4px solid #2196f3;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
        }

        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 30px;
            border-radius: 10px;
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover {
            color: #000;
        }

        .form-group {
            margin: 20px 0;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
        }

        .form-group textarea {
            min-height: 100px;
            resize: vertical;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🌟 Protejamos la Infancia, Construyamos Futuro 🌟</h1>
            <p style="font-size: 1.2em; margin-top: 10px;">Por una crianza basada en el amor, el respeto y la comunicación</p>
        </header>

        <nav>
            <ul>
                <li><a href="#presentacion">Inicio</a></li>
                <li><a href="#diagnostico">Diagnóstico</a></li>
                <li><a href="#estrategias">Estrategias</a></li>
                <li><a href="#ruta">Ruta de Atención</a></li>
                <li><a href="#recursos">Recursos</a></li>
                <li><a href="#reflexion">Reflexión</a></li>
            </ul>
        </nav>

        <section id="presentacion">
            <h2>Presentación</h2>
            <p class="intro-text">
                La violencia es un problema de alcance mundial que tiene un impacto significativo en la infancia y la adolescencia en diversos países, dejando en los niños secuelas graves y a menudo permanentes. Sus consecuencias van más allá de las víctimas directas, ya que esta problemática influye negativamente en la sociedad.
            </p>
            <p class="intro-text">
                Puede frenar el progreso social, laboral y económico de las naciones debido a los grandes gastos que generan la atención médica (tanto física como psicológica) necesaria, la cual frecuentemente resulta ineficaz por basarse en estrategias de prevención tardías y políticas de cuidado deficientes.
            </p>
            <p class="intro-text">
                El maltrato infantil se presenta en muchas formas: física, psicológica, sexual, negligencia o abandono. Su impacto deja huellas profundas en el cuerpo, la mente y el corazón de quienes lo sufren.
            </p>
            
            <div style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); padding: 30px; border-radius: 10px; margin-top: 30px;">
                <h3 style="color: #333; text-align: center;">Nuestro Propósito</h3>
                <p style="text-align: center; font-size: 1.1em;">
                    Sensibilizar a la comunidad educativa y familiar sobre la importancia de una crianza basada en el amor, el respeto y la comunicación, brindando información y estrategias de prevención y protección integral para fortalecer los vínculos familiares, prevenir los malos tratos y promover una cultura del buen trato.
                </p>
            </div>
        </section>

        <section id="diagnostico">
            <h2>Diagnóstico: El Problema del Maltrato Infantil</h2>
            
            <div style="background: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                <h3>¿Qué es el maltrato infantil?</h3>
                <p style="font-size: 1.05em;">
                    Según la OMS (2020), el maltrato infantil se define como los abusos y la desatención de que son objeto los menores de 18 años, e incluye todos los tipos de maltrato físico o psicológico, abuso sexual, desatención, negligencia y explotación comercial o de otro tipo que causen o puedan causar un daño a la salud, desarrollo o dignidad del niño, o poner en peligro su supervivencia, en el contexto de una relación de responsabilidad, confianza o poder.
                </p>
            </div>

            <h3>Tipos de Maltrato Infantil</h3>
            <div class="maltrato-tipos">
                <div class="maltrato-card">
                    <h4>💔 Maltrato Físico</h4>
                    <p>Golpes, castigos corporales y lesiones como método de "corrección".</p>
                </div>
                <div class="maltrato-card">
                    <h4>😢 Maltrato Emocional</h4>
                    <p>Insultos, humillaciones, amenazas y violencia psicológica.</p>
                </div>
                <div class="maltrato-card">
                    <h4>🚫 Maltrato por Omisión</h4>
                    <p>Falta de atención afectiva, escaso acompañamiento y negligencia.</p>
                </div>
                <div class="maltrato-card">
                    <h4>⚠️ Abuso Sexual</h4>
                    <p>Cualquier actividad sexual con un menor de edad.</p>
                </div>
            </div>

            <div class="case-study">
                <h3>📖 Caso Real: La Historia de Doris</h3>
                <p style="margin-bottom: 15px;">
                    En una institución educativa, una estudiante de tercer grado llamada Doris fue víctima de maltrato físico por parte de su madre, quien la golpeaba con correa y cable como método de "corrección". La denuncia del caso permitió activar la ruta de atención con Policía de Infancia y Adolescencia, Comisaría de Familia y psicología escolar.
                </p>
                <p><strong>Resultado:</strong> Gracias a esta intervención, la niña y su familia iniciaron un proceso de acompañamiento y orientación para mejorar la convivencia familiar.</p>
                
                <h4 style="margin-top: 20px; color: #856404;">Formas de maltrato identificadas en Doris:</h4>
                <ul>
                    <li><strong>Maltrato físico:</strong> golpes y castigos como forma de corrección</li>
                    <li><strong>Maltrato emocional:</strong> insultos, humillaciones y amenazas</li>
                    <li><strong>Maltrato por omisión:</strong> falta de atención afectiva, escaso acompañamiento escolar y poco diálogo familiar</li>
                </ul>
            </div>

            <h3>Modelo Sociointeraccional de Belsky (1980)</h3>
            <p style="margin-bottom: 15px;">El maltrato infantil surge de la interacción de varios niveles:</p>
            
            <div class="nivel-box">
                <strong>🧠 Nivel Individual:</strong> Baja autoestima, estrés y falta de habilidades parentales.
            </div>
            <div class="nivel-box">
                <strong>👨‍👩‍👧 Nivel Familiar:</strong> Conflictos, comunicación deficiente y violencia intrafamiliar.
            </div>
            <div class="nivel-box">
                <strong>🏘️ Nivel Social:</strong> Pobreza, desempleo, aislamiento.
            </div>
            <div class="nivel-box">
                <strong>🌍 Nivel Cultural:</strong> Creencias que justifican el castigo físico como forma de disciplina.
            </div>
        </section>

        <section id="estrategias">
            <h2>Acciones Estratégicas del Plan de Protección Integral</h2>
            <p class="intro-text">
                Cada acción está pensada para aplicarse en la escuela, la familia y la comunidad, aprovechando el poder de la comunicación, la educación y la tecnología para prevenir el maltrato infantil.
            </p>

            <h3>🛡️ 1. Prevención Primaria — Antes del maltrato</h3>
            
            <div class="estrategia-box">
                <h4>🏫 Escuela y familia conectadas</h4>
                <p>Creamos espacios de encuentro entre docentes, padres y orientadores para fortalecer la comunicación, los valores familiares y las pautas de crianza positivas.</p>
            </div>

            <div class="estrategia-box">
                <h4>📱 Campañas digitales de sensibilización</h4>
                <p>Publicaciones, infografías y foros en línea sobre derechos de los niños, empatía, disciplina sin violencia y bienestar emocional.</p>
            </div>

            <div class="estrategia-box">
                <h4>🎨 Talleres creativos</h4>
                <p>Actividades presenciales y virtuales para enseñar a los niños y cuidadores sobre emociones, respeto y autocuidado.</p>
            </div>

            <div class="estrategia-box">
                <h4>⏰ Tiempo de calidad</h4>
                <p>Promovemos el uso de herramientas digitales (aplicaciones familiares, retos semanales, diarios virtuales) para fortalecer el vínculo madre-hija mediante el juego, la lectura y la conversación.</p>
            </div>

            <div class="estrategia-box">
                <h4>📚 Formación para padres</h4>
                <p>Cursos virtuales gratuitos sobre comunicación afectiva, límites sin castigo y manejo del estrés.</p>
            </div>

            <h3 style="margin-top: 40px;">⚠️ 2. Prevención Secundaria — Cuando existen riesgos</h3>
            <ul style="font-size: 1.05em;">
                <li><strong>Detección temprana:</strong> Los docentes, orientadores y trabajadores sociales deben identificar señales de maltrato o negligencia a través de la observación y el diálogo.</li>
                <li><strong>Orientación personalizada:</strong> Apoyo psicológico y consejería familiar a niños y padres que presenten dificultades en la crianza.</li>
                <li><strong>Red de apoyo institucional:</strong> Coordinación con el área de salud, defensoría de familia y comisarías para atender los casos en riesgo de manera oportuna.</li>
                <li><strong>Rutas de atención:</strong> Socialización clara con los estudiantes y padres sobre cómo y dónde denunciar situaciones de maltrato (líneas 141, ICBF, comisarías).</li>
            </ul>

            <h3 style="margin-top: 40px;">🩹 3. Prevención Terciaria — Después del maltrato</h3>
            <ul style="font-size: 1.05em;">
                <li><strong>Atención integral a la víctima:</strong> Acompañamiento psicológico y social para disminuir las secuelas emocionales del maltrato.</li>
                <li><strong>Capacitación familiar:</strong> Talleres de reparación emocional, reconciliación y fortalecimiento del vínculo afectivo.</li>
                <li><strong>Seguimiento comunitario:</strong> Los docentes y orientadores harán seguimiento periódico para garantizar que el entorno familiar siga siendo seguro y protector.</li>
                <li><strong>Movilización social:</strong> Participación en cursos sobre derechos de la niñez del SNBF y la Defensoría del Pueblo.</li>
            </ul>
        </section>

        <section id="ruta">
            <h2>Ruta Paso a Paso (Ley 1620 de 2013)</h2>
            <p class="intro-text" style="background: #fff3cd; padding: 15px; border-radius: 5px;">
                <strong>Aplicación práctica basada en el caso de Doris</strong> — Protocolo para docentes y orientadores ante lesiones físicas repetidas.
            </p>

            <div class="ruta-paso" data-step="1">
                <h3>Identificación inmediata (detección en el aula)</h3>
                <p><strong>Qué hacer:</strong> Si detectas signos físicos (moretones, marcas de correa/cable) o cambios de conducta (miedo a ir a casa, retraimiento, agresividad), registra fecha, hora y descripción objetiva (qué viste, palabras del niño/a).</p>
                <p><strong>Por qué:</strong> La Ley obliga al establecimiento a identificar y registrar casos que afecten la convivencia y los derechos.</p>
            </div>

            <div class="ruta-paso" data-step="2">
                <h3>Medida de protección inmediata en la escuela</h3>
                <p><strong>Qué hacer:</strong> Garantiza que el niño/a se quede en un lugar seguro dentro del colegio (orientación, aula de apoyo) y evita exponerlo ante otros. Informa discretamente al rector/rectora y a la docente orientadora.</p>
                <p><strong>Por qué:</strong> La prioridad es proteger la integridad física y emocional del NNA mientras se toman acciones.</p>
            </div>

            <div class="ruta-paso" data-step="3">
                <h3>Registro formal del caso (documentación)</h3>
                <p><strong>Qué hacer:</strong> Completa el registro institucional: observador del estudiante, acta de caso especial o formato de "Ruta de Atención". Firma y fecha. NO subir fotos a redes sociales.</p>
                <p><strong>Por qué:</strong> La Ley crea un Sistema de Información Unificado para documentar y hacer seguimiento.</p>
            </div>

            <div class="ruta-paso" data-step="4">
                <h3>Notificación y conformación del Comité de Convivencia</h3>
                <p><strong>Qué hacer:</strong> Convoca al Comité Escolar de Convivencia (rectoría, docente orientador, docente responsable, representante de padres) para evaluar el caso y coordinar la ruta. Mantén la confidencialidad.</p>
                <p><strong>Por qué:</strong> La Ley y la Ruta exigen que las instituciones actúen articuladamente a través del comité.</p>
            </div>

            <div class="ruta-paso" data-step="5">
                <h3>Activar la Ruta de Atención Integral (remisión externa)</h3>
                <p><strong>Qué hacer:</strong> Si se confirma riesgo o daño, remite el caso inmediatamente a las autoridades competentes: ICBF (Línea 141), Policía de Infancia y Adolescencia, Comisaría de Familia y/o EPS para valoración médica y de salud mental.</p>
                <p><strong>Por qué:</strong> La Ruta establece la coordinación interinstitucional para protección y atención integral.</p>
            </div>

            <div class="ruta-paso" data-step="6">
                <h3>Valoración médica y psicosocial</h3>
                <p><strong>Qué hacer:</strong> Acompaña al niño/a para valoración en salud (urgencias o centro designado) y solicita valoración psicológica; registra los informes (historia clínica, evaluación psicológica).</p>
                <p><strong>Por qué:</strong> La documentación clínica es necesaria para acciones legales y medidas de protección.</p>
            </div>

            <div class="ruta-paso" data-step="7">
                <h3>Denuncia formal (si aplica) y protección judicial</h3>
                <p><strong>Qué hacer:</strong> Si hay evidencia de delito (golpes recurrentes, lesiones), la institución o acudiente debe presentar denuncia ante la Policía o la Fiscalía; la Comisaría de Familia puede solicitar medidas de protección provisionales.</p>
                <p><strong>Por qué:</strong> Cuando hay indicios de conductas punibles, el Sistema Judicial debe intervenir.</p>
            </div>

            <div class="ruta-paso" data-step="8">
                <h3>Acompañamiento psicosocial y medidas familiares</h3>
                <p><strong>Qué hacer:</strong> Organiza intervención con psicólogo escolar y refiere a programas de apoyo familiar (terapia familiar, seguimiento EPS, cursos parentales). Facilita la participación de la familia en talleres.</p>
                <p><strong>Por qué:</strong> La prevención terciaria busca reducir secuelas y evitar la repetición del maltrato.</p>
            </div>

            <div class="ruta-paso" data-step="9">
                <h3>Seguimiento, monitoreo y registro</h3>
                <p><strong>Qué hacer:</strong> El Comité de Convivencia realiza seguimiento mensual (bitácora), registra avances en el Sistema de Información Unificado de Convivencia Escolar y mantiene comunicación con ICBF/Comisaría.</p>
                <p><strong>Por qué:</strong> La Ley exige registro y seguimiento para garantizar reparación y prevención.</p>
            </div>

            <div class="ruta-paso" data-step="10">
                <h3>Prevención institucional y cierre del ciclo</h3>
                <p><strong>Qué hacer:</strong> Implementa medidas preventivas escolares: talleres obligatorios para padres, programas de educación emocional en el currículo, protocolos actualizados y difusión de rutas en la web del colegio.</p>
                <p><strong>Por qué:</strong> La educación preventiva y la transparencia institucional fortalecen la convivencia y reducen la recurrencia.</p>
            </div>
        </section>

        <section id="recursos">
            <h2>Recursos de Apoyo</h2>
            
            <h3>📞 Rutas de atención y líneas de ayuda en Colombia</h3>
            
            <div class="recursos-grid">
                <div class="recurso-card">
                    <h4>📞 Línea 141 - ICBF</h4>
                    <p>Instituto Colombiano de Bienestar Familiar</p>
                    <p><strong>Atención 24 horas</strong> para denunciar casos de maltrato, abuso o negligencia infantil.</p>
                    <a href="tel:141" class="btn btn-emergency" style="margin-top: 15px;">Llamar 141</a>
                </div>

                <div class="recurso-card">
                    <h4>🚔 Policía 123</h4>
                    <p>Policía de Infancia y Adolescencia</p>
                    <p>Atención inmediata en casos de violencia o riesgo.</p>
                    <a href="tel:123" class="btn btn-emergency" style="margin-top: 15px;">Llamar 123</a>
                </div>

                <div class="recurso-card">
                    <h4>🏛️ Comisaría de Familia</h4>
                    <p>Recibe denuncias y orienta sobre medidas de protección.</p>
                    <p>Contacta la comisaría de tu localidad.</p>
                </div>

                <div class="recurso-card">
                    <h4>🏫 Orientadores Escolares</h4>
                    <p>Docentes orientadores y coordinadores escolares</p>
                    <p>Primeros contactos dentro del entorno educativo.</p>
                </div>

                <div class="recurso-card">
                    <h4>🏥 Centros de Salud</h4>
                    <p>Hospitales y centros de salud</p>
                    <p>Atención médica y psicológica a las víctimas.</p>
                </div>
            </div>

            <h3 style="margin-top: 40px;">🛠️ Herramientas para Docentes</h3>
            
            <div class="btn-container">
                <button class="btn" onclick="openModal()">📝 Reportar caso confidencial</button>
                <a href="tel:141" class="btn btn-emergency">📞 Llamar ICBF 141</a>
                <a href="tel:123" class="btn btn-emergency">🚔 Llamar Policía 123</a>
                <button class="btn btn-success" onclick="alert('Funcionalidad de descarga de plantillas - En un sitio web real, aquí se descargarían los documentos PDF')">📄 Descargar Plantillas</button>
            </div>

            <div style="background: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 30px;">
                <h4>📋 Plantillas disponibles:</h4>
                <ul>
                    <li>Acta de caso especial</li>
                    <li>Formato de remisión a ICBF</li>
                    <li>Checklist para denuncia a Fiscalía</li>
                    <li>Bitácora de seguimiento de casos</li>
                    <li>Formato de observador del estudiante</li>
                </ul>
            </div>
        </section>

        <section id="reflexion">
            <h2>Mensajes de Sensibilización</h2>
            
            <div style="text-align: center; margin: 40px 0;">
                <h3 style="color: #667eea; font-size: 1.8em;">El maltrato infantil deja heridas profundas, pero también puede prevenirse con amor, diálogo y acompañamiento.</h3>
                <p style="font-size: 1.3em; margin-top: 20px; color: #764ba2;"><strong>Cada palabra, cada gesto y cada abrazo cuenta.</strong></p>
            </div>

            <div class="quote-box">
                "Un niño criado con amor y respeto será un ser humano sano, feliz y útil a la sociedad."
            </div>

            <div class="quote-box">
                "El silencio también maltrata. Denunciar es proteger."
            </div>

            <div class="quote-box">
                "La mejor herencia que puedes dejarle a un hijo es una infancia sin miedo."
            </div>

            <div class="quote-box">
                "Corregir con palabras es educar; golpear es destruir."
            </div>

            <div style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); padding: 40px; border-radius: 15px; margin-top: 40px; text-align: center;">
                <h3 style="color: #333; font-size: 2em; margin-bottom: 20px;">💪 Educar sin violencia no es debilidad</h3>
                <p style="font-size: 1.3em; color: #333;">Es una forma poderosa de construir un mundo mejor</p>
            </div>

            <div style="margin-top: 50px; text-align: center;">
                <h3 style="color: #667eea;">🤝 Comprométete con la infancia</h3>
                <p style="font-size: 1.1em; margin: 20px 0;">
                    Cada acción cuenta. Ya sea como padre, madre, docente, orientador o miembro de la comunidad, 
                    todos tenemos la responsabilidad de proteger a nuestros niños y niñas.
                </p>
                <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-top: 30px;">
                    <div style="background: white; padding: 25px; border-radius: 10px; box-shadow: 0 3px 10px rgba(0,0,0,0.1); flex: 1; min-width: 250px; max-width: 300px;">
                        <h4 style="color: #667eea;">👂 Escucha</h4>
                        <p>Presta atención a lo que los niños dicen y cómo se comportan.</p>
                    </div>
                    <div style="background: white; padding: 25px; border-radius: 10px; box-shadow: 0 3px 10px rgba(0,0,0,0.1); flex: 1; min-width: 250px; max-width: 300px;">
                        <h4 style="color: #764ba2;">🗣️ Habla</h4>
                        <p>Comunícate con empatía y respeto, sin gritos ni amenazas.</p>
                    </div>
                    <div style="background: white; padding: 25px; border-radius: 10px; box-shadow: 0 3px 10px rgba(0,0,0,0.1); flex: 1; min-width: 250px; max-width: 300px;">
                        <h4 style="color: #28a745;">🛡️ Protege</h4>
                        <p>Denuncia cualquier situación de maltrato que conozcas.</p>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <h3 style="color: white; margin-bottom: 20px;">Protejamos la Infancia, Construyamos Futuro</h3>
            <p>© 2025 - Proyecto de Prevención del Maltrato Infantil</p>
            <p style="margin-top: 15px;">Basado en la Ley 1620 de 2013 y las directrices del Sistema Nacional de Bienestar Familiar</p>
            <div style="margin-top: 30px;">
                <p><strong>Líneas de emergencia:</strong></p>
                <p>ICBF: 141 | Policía: 123 | Emergencias: 112</p>
            </div>
        </footer>
    </div>

    <!-- Modal para reportar caso -->
    <div id="reportModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 style="color: #667eea; margin-bottom: 20px;">Reportar Caso Confidencial</h2>
            <p style="margin-bottom: 20px;">Este formulario es confidencial y será enviado directamente al orientador escolar y rector/a de la institución.</p>
            
            <form id="reportForm" onsubmit="submitReport(event)">
                <div class="form-group">
                    <label>Nombre del docente que reporta:</label>
                    <input type="text" id="teacherName" required>
                </div>
                
                <div class="form-group">
                    <label>Fecha y hora de detección:</label>
                    <input type="datetime-local" id="detectionDate" required>
                </div>
                
                <div class="form-group">
                    <label>Nombre del estudiante (iniciales o código):</label>
                    <input type="text" id="studentName" required>
                </div>
                
                <div class="form-group">
                    <label>Grado y grupo:</label>
                    <input type="text" id="grade" required>
                </div>
                
                <div class="form-group">
                    <label>Descripción objetiva de lo observado (señales físicas, conducta, palabras del estudiante):</label>
                    <textarea id="description" required></textarea>
                </div>
                
                <div class="form-group">
                    <label>Tipo de maltrato sospechado:</label>
                    <select id="abuseType" style="width: 100%; padding: 10px; border: 1px solid #ddd; border-radius: 5px;">
                        <option value="">Seleccione...</option>
                        <option value="fisico">Maltrato físico</option>
                        <option value="emocional">Maltrato emocional</option>
                        <option value="negligencia">Negligencia o abandono</option>
                        <option value="sexual">Abuso sexual</option>
                        <option value="multiple">Múltiples tipos</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>¿Es urgente? (requiere acción inmediata)</label>
                    <select id="urgency" style="width: 100%; padding: 10px; border: 1px solid #ddd; border-radius: 5px;">
                        <option value="no">No</option>
                        <option value="si">Sí - Requiere atención inmediata</option>
                    </select>
                </div>
                
                <button type="submit" class="btn" style="width: 100%; margin-top: 20px;">Enviar Reporte Confidencial</button>
            </form>
        </div>
    </div>

    <script>
        function openModal() {
            document.getElementById('reportModal').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('reportModal').style.display = 'none';
        }

        window.onclick = function(event) {
            const modal = document.getElementById('reportModal');
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        }

        function submitReport(event) {
            event.preventDefault();
            
            const formData = {
                teacherName: document.getElementById('teacherName').value,
                detectionDate: document.getElementById('detectionDate').value,
                studentName: document.getElementById('studentName').value,
                grade: document.getElementById('grade').value,
                description: document.getElementById('description').value,
                abuseType: document.getElementById('abuseType').value,
                urgency: document.getElementById('urgency').value
            };

            // En un sitio web real, aquí se enviaría la información al servidor
            console.log('Reporte enviado:', formData);
            
            alert('✅ Reporte enviado exitosamente.\n\n' +
                  'El orientador escolar y el rector han sido notificados.\n' +
                  'En un caso real, este formulario enviaría la información de manera segura y confidencial al sistema interno de la institución.\n\n' +
                  'Próximos pasos:\n' +
                  '1. El Comité de Convivencia será convocado\n' +
                  '2. Se activará la ruta de atención según el protocolo\n' +
                  '3. Recibirás confirmación de las acciones tomadas\n\n' +
                  'Gracias por proteger a nuestros niños y niñas.');
            
            document.getElementById('reportForm').reset();
            closeModal();
        }

        // Smooth scroll para la navegación
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
