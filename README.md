<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Painel de Controle v3.0</title>
    <style>
        body { background-color: #0d1117; color: #58a6ff; font-family: 'Courier New', monospace; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .panel { background: #161b22; border: 1px solid #30363d; border-radius: 8px; padding: 30px; width: 90%; max-width: 400px; box-shadow: 0 8px 32px rgba(0,0,0,0.5); }
        .header { border-bottom: 1px solid #30363d; margin-bottom: 20px; padding-bottom: 10px; text-align: center; }
        .status { color: #3fb950; font-size: 14px; margin-bottom: 20px; }
        input { width: 100%; padding: 12px; margin-bottom: 15px; background: #0d1117; border: 1px solid #30363d; color: white; border-radius: 5px; box-sizing: border-box; }
        button { width: 100%; padding: 12px; background-color: #238636; color: white; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; transition: 0.3s; }
        button:hover { background-color: #2ea043; }
        .terminal-text { font-size: 11px; color: #8b949e; margin-top: 15px; line-height: 1.5; }
    </style>
</head>
<body>
    <div class="panel">
        <div class="header">
            <h2 style="color: #c9d1d9;">System Control API</h2>
            <div class="status">● Servidor Online - Latência: 24ms</div>
        </div>
        <p style="color: #8b949e; font-size: 13px;">Insira o identificador do alvo para iniciar a varredura:</p>
        <input type="text" placeholder="@usuario_alvo">
        <button type="button">INICIAR MONITORAMENTO</button>
        <div class="terminal-text">
            > Estabelecendo conexão segura...<br>
            > Bypass de criptografia ativado.<br>
            > Aguardando entrada de dados.
        </div>
    </div>
</body>
</html>
