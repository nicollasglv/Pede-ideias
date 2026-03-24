
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pede Ideias 💡</title>
<link href="https://fonts.googleapis.com" rel="stylesheet">
<style>
    :root {
        --primary-color: #ffeb3b; 
        --accent-color: #fbc02d;
        --bg-gradient: radial-gradient(circle at top right, #1e1b4b, #0f172a);
        --glass-bg: rgba(255, 255, 255, 0.03);
        --glass-border: rgba(255, 255, 255, 0.1);
    }

    * { box-sizing: border-box; transition: all 0.3s ease; }

    body {
        margin: 0;
        font-family: 'Inter', sans-serif;
        background: var(--bg-gradient);
        background-attachment: fixed;
        color: #f8fafc;
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        padding: 20px;
        overflow-x: hidden;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    .container {
        width: 100%;
        max-width: 480px;
        background: var(--glass-bg);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
        padding: 50px 40px;
        border-radius: 32px;
        box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        border: 1px solid var(--glass-border);
        animation: fadeIn 0.8s ease-out;
    }

    h1 {
        font-size: 2.8rem;
        font-weight: 800;
        margin: 0 0 10px 0;
        text-align: center;
        letter-spacing: -2px;
        background: linear-gradient(to bottom, #fff, #94a3b8);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    p.subtitle {
        text-align: center;
        color: #94a3b8;
        margin-bottom: 35px;
        font-size: 1rem;
        line-height: 1.5;
    }

    form {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    input, textarea {
        width: 100%;
        padding: 16px 20px;
        border-radius: 16px;
        border: 1px solid var(--glass-border);
        background: rgba(15, 23, 42, 0.4);
        color: #fff;
        font-size: 1rem;
        outline: none;
    }

    input:focus, textarea:focus {
        border-color: var(--primary-color);
        background: rgba(15, 23, 42, 0.6);
        box-shadow: 0 0 0 4px rgba(255, 235, 59, 0.1);
    }

    textarea { resize: none; min-height: 130px; }

    button {
        padding: 18px;
        margin-top: 10px;
        border: none;
        border-radius: 16px;
        background: var(--primary-color);
        color: #0f172a;
        font-size: 1.1rem;
        font-weight: 700;
        letter-spacing: 0.5px;
        cursor: pointer;
        box-shadow: 0 10px 20px -10px rgba(255, 235, 59, 0.4);
    }

    button:hover {
        background: #fff;
        transform: translateY(-2px);
    }

    .footer-text {
        text-align: center;
        margin-top: 25px;
        font-size: 0.8rem;
        color: #64748b;
        opacity: 0.8;
    }

    ::placeholder { color: #64748b; }

    .bg-glow {
        position: fixed;
        width: 400px;
        height: 400px;
        background: var(--primary-color);
        filter: blur(150px);
        opacity: 0.05;
        z-index: -1;
        border-radius: 50%;
        top: 10%;
        left: 10%;
    }
</style>
</head>
<body>

<div class="bg-glow"></div>

<div class="container">
    <h1>PEDE IDEIAS 💡</h1>
    <p class="subtitle">Transforme problemas em soluções. Mande sua ideia direto para nosso WhatsApp.</p>

    <form id="contactForm">
        <input type="text" id="nome" placeholder="Seu nome" required>
        <input type="email" id="email" placeholder="gmail" required>
        <textarea id="problemas" placeholder="Qual a sua ideia ou o problema que precisa resolver?" required></textarea>
        <button type="submit">Enviar Mensagem</button>
    </form>
<a href="https://discord.gg/JYs6xdN7M" target="_blank" class="discord-btn">
    Entrar no Discord
</a>
    <div class="footer-text">
        © 2026 Pede Ideias - Todos os direitos reservados.
    </div>
</div>

<script>
document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    const nome = document.getElementById('nome').value;
    const email = document.getElementById('email').value;
    const problemas = document.getElementById('problemas').value;

    const mensagem = `*NOVA IDEIA RECEBIDA*%0A%0A*Nome:* ${nome}%0A*Email:* ${email}%0A*Ideia/Problema:* ${problemas}`;
    
    window.open(`https://wa.me/5511979872476?text=${mensagem}`, '_blank');
});
</script>

</body>
</html>
