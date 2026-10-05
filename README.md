# Site-de-estudos-humanas
Estudo
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>História em Foco | 2ª Guerra Mundial e Holocausto</title>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        scroll-behavior: smooth;
    }

    :root {
        --bg: #0b1020;
        --card: #151c30;
        --card2: #1b243d;
        --text: #f4f6fb;
        --muted: #aab3c7;
        --accent: #e6a23c;
        --accent2: #d95f59;
        --border: rgba(255,255,255,.09);
    }

    body {
        font-family: Arial, Helvetica, sans-serif;
        background:
            radial-gradient(circle at top right, rgba(217,95,89,.15), transparent 30%),
            radial-gradient(circle at top left, rgba(230,162,60,.12), transparent 25%),
            var(--bg);
        color: var(--text);
        line-height: 1.7;
    }

    /* NAVBAR */

    nav {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
        background: rgba(11,16,32,.88);
        backdrop-filter: blur(15px);
        border-bottom: 1px solid var(--border);
    }

    .nav-container {
        max-width: 1200px;
        margin: auto;
        padding: 15px 25px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        font-size: 21px;
        font-weight: bold;
        color: var(--accent);
    }

    .logo span {
        color: white;
    }

    .nav-links {
        display: flex;
        gap: 20px;
        list-style: none;
    }

    .nav-links a {
        color: var(--muted);
        text-decoration: none;
        font-size: 14px;
        transition: .3s;
    }

    .nav-links a:hover {
        color: var(--accent);
    }

    /* HERO */

    .hero {
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 120px 20px 70px;
    }

    .hero-content {
        max-width: 900px;
    }

    .tag {
        display: inline-block;
        padding: 7px 15px;
        border: 1px solid rgba(230,162,60,.4);
        background: rgba(230,162,60,.08);
        color: var(--accent);
        border-radius: 30px;
        font-size: 13px;
        margin-bottom: 20px;
    }

    .hero h1 {
        font-size: clamp(45px, 7vw, 85px);
        line-height: 1.05;
        margin-bottom: 25px;
    }

    .hero h1 span {
        color: var(--accent);
    }

    .hero p {
        max-width: 700px;
        margin: auto;
        color: var(--muted);
        font-size: 18px;
    }

    .buttons {
        margin-top: 35px;
        display: flex;
        justify-content: center;
        gap: 15px;
        flex-wrap: wrap;
    }

    .btn {
        padding: 13px 22px;
        border-radius: 10px;
        text-decoration: none;
        font-weight: bold;
        transition: .3s;
    }

    .btn-primary {
        background: var(--accent);
        color: #111;
    }

    .btn-primary:hover {
        transform: translateY(-3px);
        box-shadow: 0 10px 25px rgba(230,162,60,.25);
    }

    .btn-secondary {
        border: 1px solid var(--border);
        color: white;
        background: rgba(255,255,255,.04);
    }

    .btn-secondary:hover {
        background: rgba(255,255,255,.08);
    }

    /* GENERAL */

    section {
        max-width: 1200px;
        margin: auto;
        padding: 90px 25px;
    }

    .section-title {
        margin-bottom: 45px;
    }

    .section-title small {
        color: var(--accent);
        font-weight: bold;
        text-transform: uppercase;
        letter-spacing: 2px;
    }

    .section-title h2 {
        font-size: 40px;
        margin-top: 5px;
    }

    .section-title p {
        color: var(--muted);
        max-width: 700px;
        margin-top: 10px;
    }

    /* CARDS */

    .cards {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
    }

    .card {
        background: linear-gradient(145deg, var(--card), #11182b);
        border: 1px solid var(--border);
        border-radius: 18px;
        padding: 28px;
        transition: .3s;
    }

    .card:hover {
        transform: translateY(-6px);
        border-color: rgba(230,162,60,.4);
    }

    .icon {
        width: 48px;
        height: 48px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 12px;
        background: rgba(230,162,60,.12);
        font-size: 23px;
        margin-bottom: 18px;
    }

    .card h3 {
        margin-bottom: 10px;
        font-size: 20px;
    }

    .card p {
        color: var(--muted);
        font-size: 15px;
    }

    /* ALERT */

    .important {
        margin: 30px 0;
        padding: 20px;
        border-left: 4px solid var(--accent2);
        background: rgba(217,95,89,.08);
        border-radius: 0 12px 12px 0;
        color: #ddd;
    }

    /* TIMELINE */

    .timeline {
        position: relative;
        max-width: 900px;
        margin: auto;
    }

    .timeline::before {
        content: "";
        position: absolute;
        left: 20px;
        top: 0;
        width: 2px;
        height: 100%;
        background: rgba(230,162,60,.35);
    }

    .timeline-item {
        position: relative;
        padding-left: 65px;
        margin-bottom: 35px;
    }

    .timeline-dot {
        position: absolute;
        left: 11px;
        top: 5px;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: var(--accent);
        box-shadow: 0 0 0 5px rgba(230,162,60,.12);
    }

    .timeline-year {
        color: var(--accent);
        font-weight: bold;
        font-size: 18px;
    }

    .timeline-item h3 {
        margin: 4px 0;
    }

    .timeline-item p {
        color: var(--muted);
    }

    /* CONTENT */

    .content-box {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: 20px;
        padding: 35px;
        margin-bottom: 25px;
    }

    .content-box h3 {
        color: var(--accent);
        margin-bottom: 12px;
    }

    .content-box p {
        color: #cbd1df;
        margin-bottom: 12px;
    }

    .content-box ul {
        padding-left: 22px;
        color: var(--muted);
    }

    /* GLOSSARY */

    .glossary {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
        gap: 15px;
    }

    .term {
        background: var(--card);
        padding: 20px;
        border-radius: 14px;
        border: 1px solid var(--border);
    }

    .term strong {
        color: var(--accent);
    }

    .term p {
        color: var(--muted);
        font-size: 14px;
        margin-top: 5px;
    }

    /* QUIZ */

    .quiz-container {
        max-width: 850px;
        margin: auto;
    }

    .question {
        display: none;
        background: var(--card);
        border: 1px solid var(--border);
        padding: 30px;
        border-radius: 18px;
    }

    .question.active {
        display: block;
        animation: fade .4s;
    }

    @keyframes fade {
        from {
            opacity: 0;
            transform: translateY(10px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .question-number {
        color: var(--accent);
        font-weight: bold;
        margin-bottom: 10px;
    }

    .question h3 {
        font-size: 21px;
        margin-bottom: 20px;
    }

    .options {
        display: grid;
        gap: 10px;
    }

    .option {
        padding: 15px;
        border-radius: 10px;
        background: var(--card2);
        border: 1px solid var(--border);
        color: white;
        cursor: pointer;
        text-align: left;
        transition: .2s;
    }

    .option:hover {
        border-color: var(--accent);
        transform: translateX(3px);
    }

    .option.correct {
        background: rgba(46,160,67,.2);
        border-color: #43c95b;
    }

    .option.wrong {
        background: rgba(217,95,89,.2);
        border-color: #e56b64;
    }

    .explanation {
        display: none;
        margin-top: 18px;
        padding: 15px;
        border-radius: 10px;
        background: rgba(255,255,255,.04);
        color: var(--muted);
    }

    .quiz-buttons {
        display: flex;
        justify-content: space-between;
        margin-top: 20px;
    }

    .quiz-btn {
        border: none;
        padding: 12px 20px;
        border-radius: 9px;
        cursor: pointer;
        background: var(--accent);
        font-weight: bold;
    }

    .quiz-btn:disabled {
        opacity: .4;
        cursor: not-allowed;
    }

    #result {
        display: none;
        text-align: center;
        background: var(--card);
        padding: 40px;
        border-radius: 20px;
        border: 1px solid var(--border);
    }

    #score {
        font-size: 55px;
        color: var(--accent);
        font-weight: bold;
        margin: 15px;
    }

    /* FOOTER */

    footer {
        border-top: 1px solid var(--border);
        text-align: center;
        padding: 35px 20px;
        color: var(--muted);
    }

    footer strong {
        color: var(--accent);
    }

    /* RESPONSIVE */

    @media(max-width: 700px) {
        .nav-links {
            display: none;
        }

        .hero h1 {
            font-size: 48px;
        }

        .section-title h2 {
            font-size: 32px;
        }

        section {
            padding: 70px 18px;
        }
    }
</style>
</head>

<body>

<!-- NAVBAR -->

<nav>
    <div class="nav-container">

        <div class="logo">
            História<span> em Foco</span>
        </div>

        <ul class="nav-links">
            <li><a href="#inicio">Início</a></li>
            <li><a href="#guerra">Guerra</a></li>
            <li><a href="#holocausto">Holocausto</a></li>
            <li><a href="#linha">Linha do tempo</a></li>
            <li><a href="#quiz">Quiz</a></li>
        </ul>

    </div>
</nav>


<!-- HERO -->

<header class="hero" id="inicio">

    <div class="hero-content">

        <span class="tag">📚 SITE DE ESTUDOS • HISTÓRIA</span>

        <h1>
            Segunda Guerra<br>
            <span>Mundial</span> & Holocausto
        </h1>

        <p>
            Um guia interativo para entender os principais acontecimentos,
            causas, consequências e conceitos relacionados a um dos períodos
            mais importantes e trágicos da história contemporânea.
        </p>

        <div class="buttons">
            <a href="#guerra" class="btn btn-primary">
                Começar a estudar →
            </a>

            <a href="#quiz" class="btn btn-secondary">
                Fazer o quiz
            </a>
        </div>

    </div>

</header>


<!-- VISÃO GERAL -->

<section>

    <div class="section-title">
        <small>Visão geral</small>
        <h2>O que você precisa saber</h2>
        <p>
            Comece pelos conceitos fundamentais antes de avançar para os
            acontecimentos específicos.
        </p>
    </div>

    <div class="cards">

        <div class="card">
            <div class="icon">🌍</div>
            <h3>Segunda Guerra Mundial</h3>
            <p>
                Conflito militar global ocorrido entre 1939 e 1945,
                envolvendo diversas potências e regiões do mundo.
            </p>
        </div>

        <div class="card">
            <div class="icon">⚔️</div>
            <h3>Eixo e Aliados</h3>
            <p>
                Os principais grupos envolvidos foram as potências do Eixo
                e os países Aliados.
            </p>
        </div>

        <div class="card">
            <div class="icon">✡️</div>
            <h3>Holocausto</h3>
            <p>
                Perseguição e assassinato sistemático de milhões de pessoas
                pelo regime nazista e seus colaboradores.
            </p>
        </div>

        <div class="card">
            <div class="icon">🕊️</div>
            <h3>Consequências</h3>
            <p>
                A guerra provocou enormes perdas humanas, mudanças
                territoriais e transformações políticas internacionais.
            </p>
        </div>

    </div>

</section>


<!-- GUERRA -->

<section id="guerra">

    <div class="section-title">
        <small>01 • Segunda Guerra</small>
        <h2>Segunda Guerra Mundial</h2>
        <p>
            Entenda como o conflito começou e quais foram seus principais
            acontecimentos.
        </p>
    </div>

    <div class="content-box">

        <h3>📌 Contexto</h3>

        <p>
            A Segunda Guerra Mundial ocorreu entre 1939 e 1945. Ela foi
            resultado de uma combinação de fatores políticos, econômicos
            e territoriais que se desenvolveram especialmente no período
            entre as duas guerras mundiais.
        </p>

        <p>
            Entre os fatores importantes estavam as consequências da
            Primeira Guerra Mundial, o Tratado de Versalhes, o crescimento
            de regimes autoritários, o expansionismo territorial e as
            tensões internacionais.
        </p>

    </div>

    <div class="cards">

        <div class="card">

            <div class="icon">🇩🇪</div>

            <h3>A Alemanha Nazista</h3>

            <p>
                Sob Adolf Hitler e o Partido Nazista, a Alemanha adotou
                uma política expansionista e totalitária.
            </p>

        </div>

        <div class="card">

            <div class="icon">🇮🇹</div>

            <h3>Itália Fascista</h3>

            <p>
                A Itália de Benito Mussolini participou da guerra ao lado
                das potências do Eixo.
            </p>

        </div>

        <div class="card">

            <div class="icon">🇯🇵</div>

            <h3>Japão</h3>

            <p>
                O Japão buscava ampliar sua influência e seu território
                na Ásia e no Pacífico.
            </p>

        </div>

        <div class="card">

            <div class="icon">🤝</div>

            <h3>Países Aliados</h3>

            <p>
                Entre os principais Aliados estavam Reino Unido, União
                Soviética, Estados Unidos, China e França.
            </p>

        </div>

    </div>

    <div class="important">
        <strong>⚠️ Importante:</strong>
        A guerra não começou por uma única causa. Ela foi resultado
        de um conjunto de processos políticos, econômicos, ideológicos
        e territoriais.
    </div>

</section>


<!-- HOLOCAUSTO -->

<section id="holocausto">

    <div class="section-title">
        <small>02 • Perseguição e genocídio</small>
        <h2>O Holocausto</h2>

        <p>
            Estude o Holocausto dentro de seu contexto histórico,
            compreendendo a perseguição nazista e suas consequências.
        </p>
    </div>

    <div class="content-box">

        <h3>O que foi o Holocausto?</h3>

        <p>
            O Holocausto foi a perseguição e o assassinato sistemático
            de aproximadamente seis milhões de judeus europeus pela
            Alemanha nazista e seus colaboradores durante a Segunda
            Guerra Mundial.
        </p>

        <p>
            Outros grupos também foram perseguidos pelo regime nazista,
            incluindo pessoas com deficiência, povos Roma e Sinti,
            prisioneiros de guerra soviéticos, opositores políticos,
            pessoas LGBTQIA+ e outros grupos considerados indesejáveis
            pela ideologia nazista.
        </p>

    </div>


    <div class="cards">

        <div class="card">

            <div class="icon">📢</div>

            <h3>Propaganda</h3>

            <p>
                A propaganda nazista ajudou a espalhar ideias
                antissemitas e a construir uma imagem de inimigos
                internos e externos.
            </p>

        </div>

        <div class="card">

            <div class="icon">🚫</div>

            <h3>Leis discriminatórias</h3>

            <p>
                As Leis de Nuremberg, de 1935, retiraram direitos
                e estabeleceram critérios raciais dentro da legislação
                nazista.
            </p>

        </div>

        <div class="card">

            <div class="icon">🏚️</div>

            <h3>Guetos</h3>

            <p>
                Comunidades judaicas foram confinadas em áreas
                controladas e submetidas a condições extremamente
                precárias.
            </p>

        </div>

        <div class="card">

            <div class="icon">⚠️</div>

            <h3>Campos de concentração</h3>

            <p>
                O sistema de campos nazista foi utilizado para
                aprisionamento, exploração, perseguição e assassinato.
            </p>

        </div>

    </div>

</section>


<!-- LINHA DO TEMPO -->

<section id="linha">

    <div class="section-title">

        <small>03 • Cronologia</small>

        <h2>Linha do tempo</h2>

        <p>
            Alguns dos principais acontecimentos relacionados à Segunda
            Guerra Mundial e ao Holocausto.
        </p>

    </div>


    <div class="timeline">

        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1919</div>

            <h3>Tratado de Versalhes</h3>

            <p>
                O tratado estabeleceu condições para a Alemanha após
                a Primeira Guerra Mundial e tornou-se parte importante
                do contexto político posterior.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1933</div>

            <h3>Hitler chega ao poder</h3>

            <p>
                Adolf Hitler tornou-se chanceler da Alemanha e o regime
                nazista iniciou a consolidação de uma ditadura.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1935</div>

            <h3>Leis de Nuremberg</h3>

            <p>
                Foram criadas leis que institucionalizaram a discriminação
                racial contra judeus na Alemanha nazista.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1938</div>

            <h3>Noite dos Cristais</h3>

            <p>
                Uma onda de violência antissemita atingiu comunidades
                judaicas em territórios controlados pela Alemanha.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1939</div>

            <h3>Início da Segunda Guerra Mundial</h3>

            <p>
                A Alemanha invadiu a Polônia em setembro de 1939.
                Reino Unido e França declararam guerra à Alemanha.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1941</div>

            <h3>Expansão da guerra</h3>

            <p>
                A Alemanha atacou a União Soviética e, no mesmo ano,
                o Japão atacou Pearl Harbor, levando os Estados Unidos
                a entrarem diretamente na guerra.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-dot"></div>

            <div class="timeline-year">1944</div>

            <h3>Desembarque da Normandia</h3>

            <p>
                Forças Aliadas desembarcaram na Normandia, abrindo uma
                importante frente de combate na Europa Ocidental.
            </p>

        </div>
