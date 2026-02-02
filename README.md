<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Software a Medida | Control Total</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            /* Paleta de colores: Seria, Tecnológica y Confiable */
            --primary-accent: #3B82F6; /* Azul brillante */
            --success-green: #10B981; /* Verde dinero/éxito */
            --bg-dark: #111827; /* Fondo oscuro elegante */
            --bg-card: #1F2937; /* Tarjetas */
            --text-main: #F9FAFB;
            --text-muted: #9CA3AF;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; background-color: var(--bg-dark); color: var(--text-main); line-height: 1.6; }
        .container { width: 90%; max-width: 1100px; margin: 0 auto; padding: 0 20px; }
        a { text-decoration: none; }

        /* --- BOTONES --- */
        .btn {
            display: inline-block; padding: 15px 30px; border-radius: 8px; font-weight: 700;
            text-transform: uppercase; letter-spacing: 0.5px; transition: all 0.3s ease; cursor: pointer; border: none;
        }
        .btn-whatsapp {
            background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
            color: white; box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
        }
        .btn-whatsapp:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(37, 211, 102, 0.5); }

        /* --- HEADER --- */
        header { padding: 25px 0; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .nav-flex { display: flex; justify-content: space-between; align-items: center; }
        .logo-box {
            width: 200px; height: 60px; background: rgba(255,255,255,0.05); border: 1px dashed rgba(255,255,255,0.2);
            display: flex; align-items: center; justify-content: center; color: var(--text-muted); font-size: 0.8rem;
        }

        /* --- HERO --- */
        .hero { padding: 80px 0; text-align: center; }
        .hero h1 { font-size: 3rem; font-weight: 800; margin-bottom: 20px; line-height: 1.2; background: linear-gradient(to right, #fff, #9CA3AF); -webkit-background-clip: text; -webkit-text-fill-color: transparent;}
        .hero p { font-size: 1.25rem; color: var(--text-muted); max-width: 800px; margin: 0 auto 40px; }
        .highlight { color: var(--success-green); font-weight: bold; }

        /* --- PROBLEMA (DOLOR) --- */
        .pain-section { padding: 60px 0; background: var(--bg-card); text-align: center; margin: 40px 0; border-radius: 12px; }
        .pain-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; margin-top: 40px; }
        .pain-item h3 { color: #EF4444; margin-bottom: 10px; font-size: 1.4rem; }
        .pain-item p { color: var(--text-muted); font-size: 1rem; }

        /* --- COMPARATIVA (GASTOS VS INVERSIÓN) --- */
        .comparison-section { padding: 80px 0; }
        .cards-container { display: flex; flex-wrap: wrap; justify-content: center; gap: 30px; align-items: center; }
        
        /* Tarjetas de Gastos (Negativas/Neutras) */
        .card-expense {
            background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.1);
            padding: 30px; border-radius: 15px; width: 300px; text-align: center;
        }
        .card-expense h4 { color: var(--text-muted); margin-bottom: 15px; font-weight: 600; }
        .price-tag-expense { font-size: 1.8rem; color: var(--text-main); font-weight: 700; display: block; margin-bottom: 10px; }
        .period { font-size: 0.8rem; color: var(--text-muted); text-transform: uppercase; }

        /* Tarjeta de Solución (Heroica) */
        .card-solution {
            background: linear-gradient(145deg, #1e3a8a, #172554); border: 2px solid var(--primary-accent);
            padding: 40px; border-radius: 20px; width: 350px; text-align: center;
            box-shadow: 0 0 30px rgba(59, 130, 246, 0.2); transform: scale(1.05); position: relative;
        }
        .badge {
            background: var(--success-green); color: #064E3B; font-weight: 800; padding: 5px 15px;
            border-radius: 20px; position: absolute; top: -15px; left: 50%; transform: translateX(-50%);
            font-size: 0.85rem; letter-spacing: 1px;
        }
        .card-solution h4 { color: white; margin-bottom: 10px; font-size: 1.4rem; }
        .price-tag-solution { font-size: 2.5rem; color: var(--primary-accent); font-weight: 800; display: block; margin: 15px 0; }
        .benefit-list { text-align: left; margin-top: 20px; list-style: none; }
        .benefit-list li { margin-bottom: 8px; color: #DBEAFE; font-size: 0.95rem; }
        .benefit-list li::before { content: '✓'; color: var(--success-green); margin-right: 10px; font-weight: bold; }

        /* --- CTA --- */
        .cta-footer { padding: 80px 0; text-align: center; }
        .whatsapp-large {
            display: inline-flex; align-items: center; gap: 10px;
            background-color: #25D366; color: white; font-size: 1.3rem; font-weight: bold;
            padding: 20px 50px; border-radius: 50px; text-decoration: none;
            box-shadow: 0 10px 20px rgba(0,0,0,0.3); transition: transform 0.2s;
        }
        .whatsapp-large:hover { transform: scale(1.05); }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .card-solution { transform: scale(1); width: 100%; }
            .card-expense { width: 100%; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-flex">
            <div class="logo-box">LOGO AQUÍ</div>
            <a href="https://wa.me/573114957971" class="btn btn-whatsapp">Agendar Demo</a>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Deja de perder dinero en <br>procesos que nadie controla.</h1>
            <p>Implementa <strong>El Cerebro de tu Negocio</strong>. Un software a la medida que elimina las "fugas invisibles" de dinero y te devuelve tu tiempo.</p>
            <p class="highlight">💻 Único Pago de por Vida. Sin mensualidades.</p>
        </div>
    </section>

    <div class="container">
        <section class="pain-section">
            <h2>¿Sabes cuánto dinero pierdes hoy?</h2>
            <div class="pain-grid">
                <div class="pain-item">
                    <h3>📉 Mermas Silenciosas</h3>
                    <p>Inventario que desaparece, insumos que se desperdician y cuentas que no cuadran al final del día.</p>
                </div>
                <div class="pain-item">
                    <h3>⏳ Esclavitud Operativa</h3>
                    <p>Horas pasadas en Excel uniendo datos manuales en lugar de estar vendiendo o descansando.</p>
                </div>
                <div class="pain-item">
                    <h3>❌ Errores Humanos</h3>
                    <p>Un dedo mal puesto en la calculadora que te cuesta miles de pesos al mes en facturación.</p>
                </div>
            </div>
        </section>
    </div>

    <section class="comparison-section">
        <div class="container">
            <div style="text-align: center; margin-bottom: 50px;">
                <h2>Perspectiva de Inversión</h2>
                <p style="color: var(--text-muted);">A veces gastamos más en entretenimiento temporal que en la herramienta que protege nuestro patrimonio.</p>
            </div>

            <div class="cards-container">
                
                <div class="card-expense">
                    <h4>Plataformas & Streaming</h4>
                    <p style="font-size: 0.9rem; margin-bottom: 10px;">(Costo anual promedio)</p>
                    
                    <span class="price-tag-expense">$ [COLOCA EL PRECIO AQUÍ]</span>
                    
                    <span class="period">Gasto Anual Recurrente</span>
                    <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 20px 0;">
                    <p style="color: #9CA3AF;">Entretenimiento que disfrutas, pero que no genera retorno.</p>
                </div>

                <div class="card-solution">
                    <span class="badge">MEJOR RETORNO DE INVERSIÓN</span>
                    <h4>Tu Sistema de Gestión</h4>
                    <p style="color: #BFDBFE; font-size: 0.9rem;">Software .EXE Propio</p>
                    
                    <span class="price-tag-solution">$ [COLOCA EL PRECIO AQUÍ]</span>
                    
                    <span class="period" style="color: var(--success-green);">PAGO ÚNICO DE POR VIDA</span>
                    
                    <ul class="benefit-list">
                        <li>Control total de inventarios</li>
                        <li>Eliminación de mermas y robos</li>
                        <li>Facturación automática</li>
                        <li>Tu base de datos privada</li>
                    </ul>
                </div>

                <div class="card-expense">
                    <h4>Salidas / Ocio / Café</h4>
                    <p style="font-size: 0.9rem; margin-bottom: 10px;">(Promedio 2 fines de semana)</p>
                    
                    <span class="price-tag-expense">$ [COLOCA EL PRECIO AQUÍ]</span>
                    
                    <span class="period">Gasto Efímero</span>
                    <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 20px 0;">
                    <p style="color: #9CA3AF;">Se disfruta el momento, pero el dinero desaparece.</p>
                </div>

            </div>
        </div>
    </section>

    <section class="cta-footer">
        <div class="container">
            <h2 style="font-size: 2rem; margin-bottom: 20px;">Toma el control de tu negocio hoy</h2>
            <p style="color: var(--text-muted); margin-bottom: 40px; max-width: 600px; margin-left: auto; margin-right: auto;">
                Sin suscripciones mensuales. Sin depender de internet. Un sistema robusto instalado en tu equipo para siempre.
            </p>
            
            <a href="https://wa.me/573114957971?text=Hola,%20quiero%20dejar%20de%20perder%20dinero%20y%20automatizar%20mi%20negocio.%20Me%20interesa%20el%20software." class="whatsapp-large">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg"><path d="M12.0316 0C5.39766 0 0 5.39414 0 12.0316C0 14.1539 0.553125 16.2305 1.60547 18.0539L0.267188 22.9336L5.26641 21.6211C7.01484 22.575 8.98125 23.0789 12.0281 23.0789C18.6621 23.0789 24.0598 17.6848 24.0598 11.0473C24.0598 4.41328 18.6656 0 12.0316 0ZM12.0316 21.143C9.375 21.143 7.02539 20.3555 5.09766 19.2129L4.54219 18.8836L2.34844 19.459L2.93555 17.318L2.57695 16.7484C1.35586 14.8078 0.706641 12.5695 0.706641 11.0473C0.706641 4.80234 5.78672 0.706641 12.0316 0.706641C18.2766 0.706641 23.3531 4.80234 23.3531 11.0473C23.3531 17.2922 18.2766 21.143 12.0316 21.143Z"/></svg>
                Hablar por WhatsApp
            </a>
            <p style="margin-top: 20px; font-size: 0.9rem; color: #6B7280;">Respuesta directa al 311 495 7971</p>
        </div>
    </section>

</body>
</html>
