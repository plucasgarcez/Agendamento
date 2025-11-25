# Agendamento
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lash by Seu Nome • Extensão de Cílios</title>
  <meta name="description" content="Extensão de cílios fio a fio, volume russo e design de sobrancelhas. Agendamento online."/>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    :root {
      --dourado: #d4af37;
      --rosa-claro: #fdf2f8;
      --texto: #333;
    }
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: var(--rosa-claro);
      color: var(--texto);
      line-height: 1.6;
    }

    header {
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596462502278-7b600408b570?auto=format&fit=crop&q=80') center/cover;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: white;
      padding: 20px;
    }
    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 4.2rem;
      color: var(--dourado);
      text-shadow: 0 4px 10px rgba(0,0,0,0.5);
    }
    .btn {
      background: var(--dourado);
      color: white;
      padding: 14px 40px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      font-size: 1.2rem;
      transition: 0.3s;
      display: inline-block;
      margin-top: 20px;
    }

    section { padding: 80px 20px; text-align: center; }
    .container { max-width: 1100px; margin: 0 auto; }
    h2 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      color: var(--dourado);
      margin-bottom: 40px;
    }

    /* Serviços */
    .servico {
      background: white;
      padding: 40px;
      border-radius: 20px;
      border: 3px solid var(--dourado);
      margin-bottom: 40px;
      box-shadow: 0 20px 40px rgba(212,175,55,0.15);
    }
    .servico h3 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      color: var(--dourado);
    }

    /* Formulário */
    .agendamento {
      background: white;
      padding: 50px;
      border-radius: 20px;
      max-width: 800px;
      margin: auto;
      box-shadow: 0 0 40px rgba(0,0,0,0.1);
    }

    input, select, textarea {
      width: 100%;
      padding: 14px;
      margin: 10px 0;
      border: 2px solid #eee;
      border-radius: 12px;
      font-size: 1rem;
    }

    .horarios-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
      gap: 10px;
      margin-top: 20px;
    }

    .horario-btn {
      padding: 14px;
      background: #fff7fc;
      border: 2px solid var(--dourado);
      border-radius: 12px;
      cursor: pointer;
      transition: .3s;
    }
    .horario-btn:hover {
      background: var(--dourado);
      color: #fff;
    }
    .horario-btn.selecionado {
      background: var(--dourado);
      color: white;
      font-weight: bold;
    }

    /* Botões flutuantes */
    .float-btn {
      position: fixed;
      bottom: 30px;
      width: 65px;
      height: 65px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 30px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
      z-index: 999;
      transition: 0.3s;
    }
    .wpp { right: 30px; background:#25d366; }
    .insta { right:110px; background:#d62976; }

  </style>
</head>
<body>

<header>
  <div>
    <h1>Seu Nome Lash</h1>
    <p>Beleza que transforma o olhar</p>
    <a href="#agendamento" class="btn">Agendar Agora</a>
  </div>
</header>

<section>
  <h2>Serviços</h2>

  <div class="servico">
    <h3>Fio a Fio Clássico</h3>
    <p>Natural, leve e elegante.</p>
    <p><strong>R$ 280 • Manutenção R$ 140</strong></p>
    <a href="#agendamento" class="btn">Eu quero!</a>
  </div>

  <div class="servico">
    <h3>Volume Russo</h3>
    <p>Olhar cheio e dramático.</p>
    <p><strong>R$ 380 • Manutenção R$ 190</strong></p>
    <a href="#agendamento" class="btn">Eu quero!</a>
  </div>

  <div class="servico">
    <h3>Híbrido</h3>
    <p>Mix de clássico com volume.</p>
    <p><strong>R$ 350 • Manutenção R$ 160</strong></p>
    <a href="#agendamento" class="btn">Quero esse</a>
  </div>
</section>

<section id="agendamento">
  <h2>Agende seu horário</h2>

  <div class="agendamento">
    <form id="formAgendar" action="https://formspree.io/f/manzjgzr" method="POST">

      <input type="text" name="Nome" placeholder="Seu nome completo" required>
      <input type="tel" name="WhatsApp" placeholder="WhatsApp com DDD" required>
      <input type="email" name="Email" placeholder="Seu e-mail" required>

      <select name="Serviço" required>
        <option value="">Escolha o serviço</option>
        <option value="Fio a Fio Clássico">Fio a Fio Clássico</option>
        <option value="Volume Russo">Volume Russo</option>
        <option value="Híbrido">Híbrido</option>
      </select>

      <input type="date" name="Data" id="data" required>

      <p style="margin-top:20px; font-weight:bold;">Horários disponíveis</p>

      <div class="horarios-grid">
        <div class="horario-btn" onclick="selecionarHorario(this, '09:00')">09:00</div>
        <div class="horario-btn" onclick="selecionarHorario(this, '10:00')">10:00</div>
        <div class="horario-btn" onclick="selecionarHorario(this, '14:00')">14:00</div>
        <div class="horario-btn" onclick="selecionarHorario(this, '16:00')">16:00</div>
      </div>

      <input type="hidden" name="Horário" id="horario-selecionado">

      <textarea name="Observações" rows="3" placeholder="Primeira vez? Alguma alergia?"></textarea>

      <button type="submit" class="btn" style="width:100%">Confirmar</button>
    </form>
  </div>
</section>

<!-- Botões flutuantes -->
<a class="float-btn insta" href="https://instagram.com/seu_instagram" target="_blank">
  <i class="fab fa-instagram"></i>
</a>

<a class="float-btn wpp" href="https://wa.me/5585996546214?text=Oi%20vim%20pelo%20site%20e%20quero%20agendar" target="_blank">
  <i class="fab fa-whatsapp"></i>
</a>

<script>
  document.getElementById('data').min = new Date().toISOString().split('T')[0];

  function selecionarHorario(btn, horario) {
    document.querySelectorAll('.horario-btn').forEach(e => e.classList.remove('selecionado'));
    btn.classList.add('selecionado');
    document.getElementById('horario-selecionado').value = horario;
  }
</script>

</body>
</html>

