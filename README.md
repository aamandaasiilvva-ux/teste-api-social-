<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Painel de Controle v3.0</title>
    <style>
        body { background-color: #0d1117; color: #58a6ff; font-family: 'Courier New', monospace; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .panel { background: #161b22; border: 1px solid #30363d; border-radius: 8px; padding: 30px; width: 90%; max-width: 400px; text-align: center; }
        .progress-container { width: 100%; background-color: #30363d; border-radius: 5px; margin: 20px 0; display: none; }
        .progress-bar { width: 0%; height: 20px; background-color: #238636; border-radius: 5px; transition: width 0.5s; }
        #status-text { font-size: 12px; color: #8b949e; height: 40px; }
        button { width: 100%; padding: 12px; background-color: #238636; color: white; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; }
        input { width: 100%; padding: 12px; margin-bottom: 15px; background: #0d1117; border: 1px solid #30363d; color: white; border-radius: 5px; box-sizing: border-box; }
    </style>
</head>
<body>
    <div class="panel" id="main-panel">
        <h2 style="color: #c9d1d9;">System API Scan</h2>
        <input type="text" id="target" placeholder="@usuario_alvo">
        <button onclick="startHack()">INICIAR VARREDURA</button>
        
        <div class="progress-container" id="p-container">
            <div class="progress-bar" id="p-bar"></div>
        </div>
        <div id="status-text"></div>
    </div>

    <script>
        function startHack() {
            const target = document.getElementById('target').value;
            if(!target) return alert('Digite um alvo!');
            
            document.querySelector('button').style.display = 'none';
            document.getElementById('p-container').style.display = 'block';
            
            const logs = [
                "Buscando servidor proxy...",
                "Conectando à API do Instagram...",
                "Extraindo pacotes de dados...",
                "Bypass de criptografia SSL...",
                "Quase lá: organizando mensagens...",
                "ERRO: Acesso Restrito!"
            ];
            
            let i = 0;
            const bar = document.getElementById('p-bar');
            const text = document.getElementById('status-text');
            
            const interval = setInterval(() => {
                bar.style.width = (i + 1) * 16.6 + '%';
                text.innerText = logs[i];
                i++;
                
                if(i >= logs.length) {
                    clearInterval(interval);
                    alert('Para liberar os dados de ' + target + ', é necessário o pagamento da taxa de servidor.');
                    window.location.href = "https://www.google.com"; // Aqui o hacker colocaria o link de pagamento
                }
            }, 2000);
        }
    </script>
</body>
</html>
