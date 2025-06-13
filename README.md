# Plan-Personal-de-Retiro
Imagina Ser
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía: La Realidad del Retiro en México</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <!-- 
    Plan de Narrativa y Estructura:
    1.  Introducción/Gancho: "La Realidad del Retiro en México". Un título fuerte para captar la atención.
    2.  Sección 1: El Cambio Demográfico. Visualizar con gráficos el envejecimiento de la población mexicana para establecer el contexto.
        - Data Point: % Población +65 años 2020 vs 2050. Goal: Comparar. Visualization: Bar Chart (Chart.js/Canvas). Justification: Ideal para una comparación directa y dramática.
        - Data Point: Proyección de Población en México. Goal: Cambio. Visualization: Line Chart (Chart.js/Canvas). Justification: Muestra claramente la tendencia ascendente de la población de adultos mayores frente a la población total.
    3.  Sección 2: La Incómoda Verdad del Retiro Actual. Crear el "dolor" o la necesidad emocional al mostrar la precariedad actual.
        - Data Point: % de hombres/mujeres en edad de retiro que necesitan trabajar. Goal: Informar. Visualization: Donut Charts (Chart.js/Canvas). Justification: Excelente para mostrar proporciones de un todo de forma impactante.
        - Data Point: Principales preocupaciones de los mayores de 65 años. Goal: Comparar. Visualization: Horizontal Bar Chart (Chart.js/Canvas). Justification: Efectivo para clasificar y comparar categorías textuales.
    4.  Sección 3: El Mito del AFORE. Abordar y desmentir la objeción más común.
        - Data Point: Tasa de reemplazo < 50%. Goal: Informar. Visualization: Bloque de texto con un "Single Big Number" y una comparación visual simple (HTML/CSS). Justification: Un gráfico complejo no es necesario; el impacto está en el número y la comparación directa.
    5.  Sección 4: La Solución: Tomar el Control. Introducir "Imagina Ser" y el poder de la planificación.
        - Data Point: El poder del interés compuesto. Goal: Cambio. Visualization: Area Chart (Chart.js/Canvas). Justification: El área rellenada enfatiza el volumen y el crecimiento acumulado del ahorro de manera muy visual.
        - Data Point: Rendimientos de Imagina Ser vs. otros instrumentos. Goal: Comparar. Visualization: Ordered Bar Chart (Chart.js/Canvas). Justification: Demuestra la superioridad o competitividad del producto de forma clara y ordenada.
    6.  Sección 5: Los Pilares de Imagina Ser. Explicar cómo funciona el producto de forma sencilla.
        - Data Point: Los 3 beneficios clave (Protección, Ahorro, Retiro). Goal: Organizar (Proceso). Visualization: Flow Chart (HTML/CSS/Tailwind). Justification: Al no poder usar Mermaid/SVG, una estructura de divs con bordes y flechas creadas con Tailwind es la mejor alternativa para mostrar un flujo de proceso.
    7.  Sección 6: Llamada a la Acción. Convertir el interés en una acción concreta.
        - Data Point: Información de contacto. Goal: Informar. Visualization: Bloque de texto estilizado con botón. Justification: Un CTA claro y directo es fundamental para la conversión.

    Confirmación: NI Mermaid JS NI SVG fueron utilizados en la creación de este artefacto. Toda la visualización se realiza a través de Chart.js (Canvas) y HTML/CSS con Tailwind.
    Paleta de Colores Seleccionada: "Brilliant Blues" para un look profesional, moderno y confiable.
    -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F0F2F5;
        }
        .chart-container {
            position: relative;
            width: 100%;
            height: 350px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .text-shadow-custom {
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        .card {
            background-color: white;
            border-radius: 0.75rem;
            padding: 1.5rem;
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
        }
        .flow-arrow {
            font-size: 2rem;
            color: #003F5C;
            line-height: 1;
        }
    </style>
</head>
<body class="text-gray-800">

    <header class="bg-[#003F5C] text-white text-center py-12 px-4">
        <h1 class="text-4xl md:text-6xl font-black text-shadow-custom">La Realidad del Retiro en México</h1>
        <p class="mt-4 text-lg md:text-xl max-w-3xl mx-auto">Una mirada profunda a nuestro futuro y la urgencia de tomar el control hoy.</p>
    </header>

    <main class="container mx-auto mt-[-2rem] px-4">

        <section id="demografia" class="py-12">
            <div class="card">
                <h2 class="text-3xl font-bold text-center mb-2 text-[#003F5C]">Un País que Envejece</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">La estructura de la población en México está cambiando a un ritmo acelerado. Vivimos más tiempo, lo que presenta tanto oportunidades como desafíos monumentales para nuestro sistema de retiro.</p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div>
                        <h3 class="text-xl font-bold text-center mb-2">Población de +65 años: Hoy vs. Futuro</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">El porcentaje de adultos mayores en México se duplicará para 2050, lo que significa una mayor presión sobre los sistemas de pensiones y servicios de salud.</p>
                        <div class="chart-container max-w-md mx-auto">
                            <canvas id="poblacion65Chart"></canvas>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-center mb-2">Proyección de Población al 2100</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">Mientras la población total de México se estabilizará y comenzará a decrecer, la población de adultos mayores seguirá en aumento, cruzándose en un punto crítico alrededor de 2080.</p>
                         <div class="chart-container max-w-md mx-auto">
                            <canvas id="proyeccionPoblacionChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="realidad" class="py-12">
            <div class="card">
                <h2 class="text-3xl font-bold text-center mb-2 text-[#BC5090]">La Incómoda Verdad del Retiro Actual</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">Para la gran mayoría, llegar a la "edad de jubilación" no significa descanso. La realidad económica obliga a millones a seguir trabajando, enfrentando un futuro con preocupaciones constantes.</p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                    <div>
                        <h3 class="text-xl font-bold text-center mb-4">¿Descanso o Necesidad? La Realidad Laboral</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">Los datos son contundentes: un altísimo porcentaje de la población en edad de retiro permanece económicamente activa por necesidad, no por elección.</p>
                        <div class="flex flex-col sm:flex-row justify-around gap-6">
                            <div class="text-center">
                                <div class="chart-container !h-60 !w-60 mx-auto">
                                    <canvas id="hombresActivosChart"></canvas>
                                </div>
                                <h4 class="font-bold mt-2">Hombres</h4>
                            </div>
                            <div class="text-center">
                                <div class="chart-container !h-60 !w-60 mx-auto">
                                    <canvas id="mujeresActivasChart"></canvas>
                                </div>
                                <h4 class="font-bold mt-2">Mujeres</h4>
                            </div>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-center mb-4">Principales Preocupaciones en la Vejez</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">Cuando se pregunta a los adultos mayores qué les quita el sueño, los problemas económicos y de salud superan con creces a otras inquietudes.</p>
                        <div class="chart-container max-w-lg mx-auto">
                            <canvas id="preocupacionesChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="afore" class="py-12">
            <div class="card">
                <h2 class="text-3xl font-bold text-center mb-2 text-[#EF5675]">El Mito del AFORE</h2>
                 <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">Muchos mexicanos confían en que su AFORE será suficiente para un retiro cómodo. La realidad matemática muestra un panorama muy diferente y alarmante.</p>
                <div class="bg-[#003F5C] text-white rounded-lg p-8 flex flex-col md:flex-row items-center gap-8">
                    <div class="text-center md:text-left md:w-2/3">
                        <h3 class="text-2xl font-bold">La Tasa de Reemplazo: El Dato que Debes Conocer</h3>
                        <p class="mt-2">La tasa de reemplazo es el porcentaje de tu último salario que recibirás como pensión. En México, las estimaciones más optimistas la sitúan por debajo del 50%. En otras palabras, si hoy ganas $20,000, planea vivir con menos de $10,000.</p>
                    </div>
                    <div class="text-center md:w-1/3">
                        <div class="text-6xl font-black text-[#FFA600]">&lt;50%</div>
                        <div class="font-bold mt-2">de tu último sueldo</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="solucion" class="py-12">
            <div class="card">
                <h2 class="text-3xl font-bold text-center mb-2 text-[#7A5195]">La Solución: Tomar el Control con un Plan Personal</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">Frente a esta realidad, la única salida es la planificación proactiva. Un Plan Personal de Retiro (PPR) como <span class="font-bold">Imagina Ser</span> te pone en el asiento del conductor de tu futuro financiero.</p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div>
                        <h3 class="text-xl font-bold text-center mb-2">El Poder del Interés Compuesto</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">Empezar pronto y ser constante es la clave. La gráfica muestra cómo tus aportaciones (base) son superadas exponencialmente por los rendimientos (crecimiento), creando un patrimonio sólido.</p>
                        <div class="chart-container max-w-lg mx-auto">
                            <canvas id="interesCompuestoChart"></canvas>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-center mb-2">Rendimiento Real: Imagina Ser vs. Alternativas</h3>
                        <p class="text-sm text-gray-600 text-center mb-4">No todos los ahorros son iguales. Imagina Ser ofrece rendimientos competitivos diseñados para superar la inflación y maximizar tu patrimonio a largo plazo, superando a muchas opciones tradicionales.</p>
                         <div class="chart-container max-w-lg mx-auto">
                            <canvas id="rendimientoComparativoChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="pilares" class="py-12">
            <div class="card">
                <h2 class="text-3xl font-bold text-center mb-2 text-[#003F5C]">Los 3 Pilares de Imagina Ser</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">Este no es solo un plan de ahorro. Es una estrategia integral que se sostiene sobre tres pilares fundamentales que garantizan tu tranquilidad en cada etapa.</p>
                <div class="flex flex-col md:flex-row items-center justify-center gap-4 md:gap-8">
                    
                    <div class="text-center p-4 border-2 border-[#003F5C] rounded-lg flex-1">
                        <div class="text-5xl mb-2">🛡️</div>
                        <h3 class="text-xl font-bold">Protección Total</h3>
                        <p class="text-sm mt-2">Desde el día uno, tú y tu familia están protegidos. En caso de fallecimiento, tus beneficiarios reciben la suma asegurada. En caso de invalidez, nosotros nos hacemos cargo del plan por ti.</p>
                    </div>

                    <div class="transform rotate-90 md:rotate-0 flow-arrow">➔</div>

                    <div class="text-center p-4 border-2 border-[#7A5195] rounded-lg flex-1">
                         <div class="text-5xl mb-2">📈</div>
                        <h3 class="text-xl font-bold">Ahorro Inteligente</h3>
                        <p class="text-sm mt-2">Tu dinero crece en UDIs o Dólares para protegerte de la devaluación, con rendimientos garantizados y beneficios fiscales que puedes aprovechar cada año.</p>
                    </div>

                    <div class="transform rotate-90 md:rotate-0 flow-arrow">➔</div>

                    <div class="text-center p-4 border-2 border-[#FFA600] rounded-lg flex-1">
                        <div class="text-5xl mb-2">🏖️</div>
                        <h3 class="text-xl font-bold">Retiro Garantizado</h3>
                        <p class="text-sm mt-2">Al llegar a la meta, recibes una renta mensual ¡de por vida! Esto te da la certeza de un ingreso constante para vivir tu retiro como siempre lo soñaste, sin preocupaciones.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="cta" class="py-12">
            <div class="text-center bg-white rounded-lg p-10 shadow-xl">
                 <h2 class="text-3xl font-bold text-[#003F5C]">El mejor día para empezar fue ayer. El segundo mejor es hoy.</h2>
                <p class="mt-4 text-gray-600 max-w-2xl mx-auto">No dejes tu futuro al azar. Tomar una decisión informada ahora es el acto de responsabilidad más grande contigo mismo y con tu familia.</p>
                <a href="https://wa.me/524661479339?text=Hola%20Rodrigo,%20vi%20la%20infografía%20y%20me%20gustaría%20una%20asesoría%20sobre%20mi%20plan%20de%20retiro." target="_blank" class="mt-8 inline-block bg-gradient-to-r from-[#FF764A] to-[#FFA600] text-white font-bold py-4 px-8 rounded-lg text-lg shadow-lg hover:scale-105 transform transition-transform">
                    Agenda una Asesoría Gratuita
                </a>
                <p class="mt-4 text-sm text-gray-500">con Rodrigo Anaya, Asesor Profesional.</p>
            </div>
        </section>
    </main>

    <footer class="text-center py-6 bg-[#003F5C] text-white text-sm">
        <p>Infografía creada para fines educativos y de concienciación.</p>
        <p>Datos obtenidos de Seguros Monterrey New York Life y fuentes públicas como CONAPO e INEGI.</p>
    </footer>

    <script>
        const brilliantBluesPalette = {
            darkBlue: '#003F5C',
            purple: '#7A5195',
            pink: '#BC5090',
            redPink: '#EF5675',
            orange: '#FF764A',
            yellow: '#FFA600',
            lightGray: '#F0F2F5',
            darkGray: '#333333'
        };

        const tooltipTitleCallback = function(tooltipItems) {
            const item = tooltipItems[0];
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
              return label.join(' ');
            } else {
              return label;
            }
        };

        const wrapLabel = (label) => {
            const maxLength = 16;
            if (label.length <= maxLength) {
                return label;
            }
            const words = label.split(' ');
            let lines = [];
            let currentLine = '';
            words.forEach(word => {
                if ((currentLine + word).length > maxLength) {
                    lines.push(currentLine.trim());
                    currentLine = '';
                }
                currentLine += word + ' ';
            });
            lines.push(currentLine.trim());
            return lines;
        };

        const commonChartOptions = {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    labels: {
                        color: brilliantBluesPalette.darkGray,
                        font: {
                           family: "'Inter', sans-serif"
                        }
                    }
                },
                tooltip: {
                    callbacks: {
                        title: tooltipTitleCallback
                    }
                }
            },
            scales: {
                y: {
                    ticks: { color: brilliantBluesPalette.darkGray },
                    grid: { color: '#e0e0e0' }
                },
                x: {
                    ticks: { color: brilliantBluesPalette.darkGray },
                    grid: { display: false }
                }
            }
        };

        new Chart(document.getElementById('poblacion65Chart'), {
            type: 'bar',
            data: {
                labels: ['México 2020', 'México 2050'],
                datasets: [{
                    label: '% de Población +65 años',
                    data: [7.6, 16.9],
                    backgroundColor: [brilliantBluesPalette.pink, brilliantBluesPalette.redPink],
                    borderColor: '#ffffff',
                    borderWidth: 2
                }]
            },
            options: {...commonChartOptions}
        });

        new Chart(document.getElementById('proyeccionPoblacionChart'), {
            type: 'line',
            data: {
                labels: ['2020', '2030', '2040', '2050', '2060', '2070', '2080', '2090', '2100'],
                datasets: [{
                    label: 'Población Total (millones)',
                    data: [128.9, 140.9, 149.8, 155.2, 157.2, 156.3, 153.1, 147.9, 141.5],
                    borderColor: brilliantBluesPalette.purple,
                    backgroundColor: 'rgba(122, 81, 149, 0.1)',
                    fill: true,
                    tension: 0.4
                }, {
                    label: 'Población +65 años (millones)',
                    data: [9.8, 14.0, 20.6, 26.2, 32.3, 37.9, 41.6, 43.5, 44.0],
                    borderColor: brilliantBluesPalette.orange,
                    backgroundColor: 'rgba(255, 118, 74, 0.1)',
                    fill: true,
                    tension: 0.4
                }]
            },
            options: {...commonChartOptions}
        });

        new Chart(document.getElementById('hombresActivosChart'), {
            type: 'doughnut',
            data: {
                labels: ['Necesitan Trabajar', 'Jubilados/Pensionados'],
                datasets: [{
                    data: [83, 17],
                    backgroundColor: [brilliantBluesPalette.redPink, brilliantBluesPalette.lightGray],
                    borderColor: '#ffffff',
                    borderWidth: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: false },
                    tooltip: {
                         callbacks: {
                            title: tooltipTitleCallback
                        }
                    },
                    title: {
                        display: true,
                        text: '83%',
                        position: 'bottom',
                        font: { size: 24, weight: 'bold' },
                        color: brilliantBluesPalette.redPink,
                        padding: { top: -60 }
                    }
                }
            }
        });

        new Chart(document.getElementById('mujeresActivasChart'), {
            type: 'doughnut',
            data: {
                labels: ['Necesitan Trabajar', 'Jubiladas/Pensionadas'],
                datasets: [{
                    data: [95, 5],
                    backgroundColor: [brilliantBluesPalette.pink, brilliantBluesPalette.lightGray],
                    borderColor: '#ffffff',
                    borderWidth: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: false },
                    tooltip: {
                         callbacks: {
                            title: tooltipTitleCallback
                        }
                    },
                    title: {
                        display: true,
                        text: '95%',
                        position: 'bottom',
                        font: { size: 24, weight: 'bold' },
                        color: brilliantBluesPalette.pink,
                        padding: { top: -60 }
                    }
                }
            }
        });
        
        const preocupacionesLabels = [
            wrapLabel('Salud y bienestar'),
            wrapLabel('Problemas económicos'),
            'Vejez',
            wrapLabel('Problemas familiares'),
            'Desempleo'
        ];
        new Chart(document.getElementById('preocupacionesChart'), {
            type: 'bar',
            data: {
                labels: preocupacionesLabels,
                datasets: [{
                    label: '% de Preocupación',
                    data: [29, 29, 17, 10, 6],
                    backgroundColor: brilliantBluesPalette.purple,
                    borderColor: '#ffffff',
                    borderWidth: 2
                }]
            },
            options: {
                ...commonChartOptions,
                indexAxis: 'y',
                plugins: {
                    legend: { display: false },
                    tooltip: {
                         callbacks: {
                            title: tooltipTitleCallback
                        }
                    }
                }
            }
        });

        new Chart(document.getElementById('interesCompuestoChart'), {
            type: 'line',
            data: {
                labels: ['Año 0', 'Año 5', 'Año 10', 'Año 15', 'Año 20', 'Año 25', 'Año 30'],
                datasets: [{
                    label: 'Aportaciones',
                    data: [0, 60000, 120000, 180000, 240000, 300000, 360000],
                    borderColor: brilliantBluesPalette.pink,
                    backgroundColor: 'rgba(188, 80, 144, 0.1)',
                    fill: 'start'
                }, {
                    label: 'Capital con Rendimientos',
                    data: [0, 75000, 190000, 380000, 720000, 1300000, 2500000],
                     borderColor: brilliantBluesPalette.darkBlue,
                    backgroundColor: 'rgba(0, 63, 92, 0.2)',
                    fill: 'start',
                    tension: 0.3
                }]
            },
            options: {...commonChartOptions}
        });
        
        new Chart(document.getElementById('rendimientoComparativoChart'), {
            type: 'bar',
            data: {
                labels: ['Depósitos de Ahorro', 'CETES', 'Imagina Ser (UDI)'],
                datasets: [{
                    label: 'Rendimiento Nominal Últimos 12 meses (ejemplo)',
                    data: [4.08, 4.63, 10.52],
                    backgroundColor: [
                        brilliantBluesPalette.pink,
                        brilliantBluesPalette.purple,
                        brilliantBluesPalette.orange
                    ],
                    borderColor: '#ffffff',
                    borderWidth: 2
                }]
            },
            options: {
                ...commonChartOptions,
                 plugins: {
                    legend: { display: false },
                    tooltip: {
                         callbacks: {
                            title: tooltipTitleCallback
                        }
                    }
                }
            }
        });
    </script>
</body>
</html>
