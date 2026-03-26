<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Convite do Pedro Calleb</title>
    <style>
        /* CORES E ESTILO DO TEMA */
        :root {
            --amarelo: #ffcc00;
            --azul-escuro: #0f172a;
            --azul-card: #1e293b;
            --vermelho: #ef4444;
            --branco: #ffffff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; }
        
        body { 
            background-color: #000; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
            overflow: hidden;
        }

        /* SIMULAÇÃO DO CELULAR */
        .celular {
            width: 100%;
            max-width: 400px;
            height: 100%;
            background: var(--azul-escuro);
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 50px rgba(0,0,0,0.8);
        }

        /* ANIMAÇÃO DE DESLIZAR (SLIDER) */
        .slider {
            display: flex;
            width: 200%;
            height: 100%;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .tela {
            width: 50%;
            height: 100%;
            padding: 30px 20px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* ANIMAÇÕES VISUAIS */
        @keyframes girar { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
        @keyframes flutuar { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-8px); } }

        /* --- TELA 1: CONVITE --- */
        .topo { display: flex; justify-content: space-between; width: 100%; align-items: center; margin-bottom: 20px; }
        .icone-animado { font-size: 35px; animation: flutuar 3s infinite ease-in-out; }
        
        .badge-cr7 { 
            background: var(--amarelo); color: #000; padding: 12px 18px; 
            border-radius: 50%; font-weight: 900; font-size: 22px;
            box-shadow: 0 0 20px var(--amarelo);
        }

        .chamada { text-align: center; color: var(--amarelo); text-transform: uppercase; margin: 20px 0; }
        
        .nome-box { 
            border: 3px solid var(--amarelo); padding: 12px 25px; 
            color: var(--amarelo); font-size: 26px; font-weight: 900; 
            margin-bottom: 25px; text-align: center;
            letter-spacing: 1px;
        }

        .idade-circulo {
            width: 110px; height: 110px; background: var(--vermelho);
            border: 4px solid var(--amarelo); border-radius: 50%;
            display: flex; flex-direction: column; justify-content: center;
            align-items: center; color: white; position: relative; margin-bottom: 30px;
        }
        .estrela { position: absolute; top: -12px; right: -12px; color: var(--amarelo); font-size: 28px; animation: girar 5s infinite linear; }

        .card-info { 
            background: var(--azul-card); width: 100%; border-radius: 20px; 
            padding: 25px; margin-bottom: 30px; border: 1px solid #334155;
        }
        .item-info { display: flex; align-items: center; margin-bottom: 15px; color: white; font-size: 15px; }
        .item-info:last-child { margin-bottom: 0; }
        .item-info span { color: var(--amarelo); margin-right: 15px; font-size: 20px; }

        .botao-presentes {
            background: var(--amarelo); color: black; width: 100%;
            padding: 20px; border-radius: 50px; border: none;
            font-weight: bold; font-size: 17px; cursor: pointer;
            box-shadow: 0 8px 20px rgba(255, 204, 0, 0.4);
            display: flex; justify-content: space-between; align-items: center;
            transition: transform 0.2s;
        }
        .botao-presentes:active { transform: scale(0.95); }

        /* --- TELA 2: PRESENTES --- */
        .titulo-presentes { color: var(--amarelo); text-align: center; font-size: 24px; margin-bottom: 5px; }
        .sub-presentes { color: white; font-size: 13px; margin-bottom: 25px; opacity: 0.8; }
        
        .lista-presentes { width: 100%; margin-bottom: 20px; }
        .presente-item {
            background: var(--azul-card); border-radius: 18px;
            padding: 15px; margin-bottom: 12px; display: flex; align-items: center;
            border-left: 6px solid var(--amarelo);
        }
        .icon-box { 
            width: 50px; height: 50px; border-radius: 15px; 
            display: flex; justify-content: center; align-items: center;
            margin-right: 15px; font-size: 24px; color: white;
        }
        .p-info { display: flex; flex-direction: column; }
        .p-nome { color: white; font-weight: bold; font-size: 16px; }
        .p-detalhe { color: #94a3b8; font-size: 13px; margin-top: 2px; }
        .destaque-amarelo { color: var(--amarelo); font-weight: bold; }

        .mensagem-final { color: var(--amarelo); font-size: 13px; text-align: center; margin: 15px 0; font-style: italic; }

        .botao-voltar {
            background: transparent; border: 2px solid var(--amarelo); color: var(--amarelo);
            padding: 12px 25px; border-radius: 30px; cursor: pointer; font-weight: bold;
            margin-top: 10px; margin-bottom: 40px;
        }
.tela {
    width: 100%;
    height: 100%;
    flex-shrink: 0;
    padding: 30px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    /* ESSA É A CHAVE: Permite rolar se o conteúdo for grande */
    overflow-y: auto; 
    /* Esconde a barra de rolagem visualmente em alguns navegadores */
    scrollbar-width: none; 
}

.tela::-webkit-scrollbar {
    display: none; /* Esconde a barra no Chrome/Safari */
}

/* Ajuste na lista para não cortar o último item */
.lista-presentes { 
    width: 100%; 
    margin-bottom: 20px;
    padding-bottom: 30px; 
}

/* Garante que o ícone de presente do topo tenha um espaço */
.tela > div:first-child {
    margin-top: 10px;
}
        /* GESTÃO DA TROCA DE TELA */
        .ver-presentes .slider { transform: translateX(-50%); }
    </style>
</head>
<body>

    <div class="celular" id="app">
        <div class="slider">
            
            <div class="tela">
                <div class="topo">
                    <div class="icone-animado">⚽</div>
                    <div class="badge-cr7">CR7</div>
                    <div class="icone-animado" style="animation-delay: 1.5s">🏆</div>
                </div>

                <div class="chamada">
                    <p style="font-size: 13px; letter-spacing: 2px;">Você está convidado para o</p>
                    <h1 style="font-size: 38px; font-weight: 900;">Aniversário</h1>
                    <p style="font-size: 15px; color: #fff; margin-top: 5px;">do craque</p>
                </div>

                <div class="nome-box">PEDRO CALLEB</div>

                <div class="idade-circulo">
                    <span class="estrela">★</span>
                    <h2 style="font-size: 50px; font-weight: 900;">7</h2>
                    <p style="font-size: 12px; font-weight: bold;">ANOS</p>
                </div>

                <div class="card-info">
                    <div class="item-info"><span>📅</span> <b>DATA:</b> &nbsp; 9 de Maio</div>
                    <div class="item-info"><span>🕒</span> <b>HORÁRIO:</b> &nbsp; 17h</div>
                    <div class="item-info"><span>📍</span> <b>LOCAL:</b> &nbsp; Bella Vista, n29 - Fazenda Grande III</div>
                </div>

                <button class="botao-presentes" onclick="navegar(true)">
                    <span>🎁 Sugestões de Presentes</span>
                    <span style="font-size: 20px;">❯</span>
                </button>
            </div>

            <div class="tela">
                <div style="font-size: 40px; margin-bottom: 10px;">🎁</div>
                <h2 class="titulo-presentes">SUGESTÕES DE PRESENTES</h2>
                <p class="sub-presentes">Para o craque Pedro Calleb</p>

                <div class="lista-presentes">
                    <div class="presente-item"><div class="icon-box" style="background: #22c55e;">⚽</div><div class="p-info"><p class="p-nome">#1 Bola de Futebol</p><p class="p-detalhe">Para treinar os dribles!</p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #3b82f6;">👟</div><div class="p-info"><p class="p-nome">#2 Sapato / Percata</p><p class="p-detalhe">Número <span class="destaque-amarelo">34</span></p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #ef4444;">👕</div><div class="p-info"><p class="p-nome">#3 Camisa</p><p class="p-detalhe">Tamanho <span class="destaque-amarelo">14 anos</span></p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #a855f7;">🩳</div><div class="p-info"><p class="p-nome">#4 Bermuda</p><p class="p-detalhe">Tamanho <span class="destaque-amarelo">14 anos</span></p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #06b6d4;">🚿</div><div class="p-info"><p class="p-nome">#5 Toalha</p><p class="p-detalhe">Para os treinos diários</p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #f97316;">🩴</div><div class="p-info"><p class="p-nome">#6 Sandália</p><p class="p-detalhe">Número <span class="destaque-amarelo">33</span></p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #b91c1c;">🛡️</div><div class="p-info"><p class="p-nome">#7 Camisa CR7 / Bahia</p><p class="p-detalhe">Do time do coração!</p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #6b21a8;">🎒</div><div class="p-info"><p class="p-nome">#8 Mochila</p><p class="p-detalhe">Para carregar as conquistas!</p></div></div>
                    <div class="presente-item"><div class="icon-box" style="background: #ec4899;">🪁</div><div class="p-info"><p class="p-nome">#9 Pipas</p><p class="p-detalhe">Diversão garantida!</p></div></div>
                </div>

                <p class="mensagem-final">💝 Qualquer presente será recebido com muito carinho!</p>

                <button class="botao-voltar" onclick="navegar(false)">❮ Voltar ao Convite</button>
            </div>

        </div>
    </div>

    <script>
        function navegar(irParaPresentes) {
            const app = document.getElementById('app');
            if(irParaPresentes) {
                app.classList.add('ver-presentes');
            } else {
                app.classList.remove('ver-presentes');
            }
        }
    </script>
</body>
</html>
