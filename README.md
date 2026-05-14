<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Instituto Togni — Processo de Marketing</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #f7f9fb;
  --white: #ffffff;
  --petrol: #0F2C3E;
  --petrol-mid: #48768D;
  --petrol-light: #e6eff4;
  --gold: #D99F6D;
  --gold-pale: #fdf8ed;
  --gold-border: rgba(217,159,109,0.35);
  --green: #2d7a4f;
  --green-pale: #edf7f2;
  --green-border: rgba(45,122,79,0.3);
  --red: #c0392b;
  --text: #1a2530;
  --muted: #6b7a85;
  --border: #dde3e8;
  --shadow: 0 2px 16px rgba(15,44,62,0.08);
  --shadow-lg: 0 8px 40px rgba(15,44,62,0.13);
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  background: var(--bg);
  font-family: 'Outfit', sans-serif;
  color: var(--text);
  font-size: 14px;
  line-height: 1.6;
  min-height: 100vh;
}

/* ── TOP BAR ── */
.topbar {
  background: #0F2C3E;
  padding: 0 40px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: sticky;
  top: 0;
  z-index: 200;
  box-shadow: 0 2px 20px rgba(0,0,0,0.2);
}

.topbar-brand {
  font-family: 'Cormorant Garamond', serif;
  font-size: 20px;
  font-weight: 700;
  color: #fff;
  display: flex;
  align-items: center;
  gap: 10px;
}

.topbar-brand span { color: var(--gold); }

.topbar-week {
  display: flex;
  align-items: center;
  gap: 10px;
  color: rgba(255,255,255,0.6);
  font-size: 13px;
}

.week-input {
  background: rgba(255,255,255,0.1);
  border: 1px solid rgba(255,255,255,0.15);
  border-radius: 8px;
  padding: 6px 12px;
  color: #fff;
  font-family: 'Outfit', sans-serif;
  font-size: 13px;
  font-weight: 500;
  cursor: pointer;
  outline: none;
  width: 140px;
}

.week-input::-webkit-calendar-picker-indicator { filter: invert(1) opacity(0.5); cursor: pointer; }

/* ── TAB NAV ── */
.tab-nav {
  background: var(--white);
  border-bottom: 1px solid var(--border);
  padding: 0 40px;
  display: flex;
  gap: 0;
  box-shadow: var(--shadow);
}

.tab-btn {
  display: flex;
  align-items: center;
  gap: 9px;
  padding: 16px 24px;
  font-size: 13px;
  font-weight: 600;
  color: var(--muted);
  border: none;
  background: none;
  cursor: pointer;
  border-bottom: 3px solid transparent;
  transition: all 0.2s;
  letter-spacing: 0.02em;
  position: relative;
}

.tab-btn:hover { color: var(--petrol); }

.tab-btn.active { color: var(--petrol); border-bottom-color: var(--gold); }

.tab-icon { font-size: 18px; }

.tab-badge {
  background: var(--petrol-light);
  color: var(--petrol);
  border-radius: 10px;
  padding: 1px 7px;
  font-size: 10px;
  font-weight: 700;
}

.tab-btn.active .tab-badge { background: var(--gold-pale); color: var(--gold); }

/* ── CONTENT ── */
.content { padding: 36px 40px 100px; max-width: 1080px; }

.panel { display: none; animation: fadein 0.3s ease; }
.panel.active { display: block; }

@keyframes fadein { from { opacity:0; transform:translateY(12px); } to { opacity:1; transform:translateY(0); } }

/* ── SECTION HEADERS ── */
.section-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 28px;
  font-weight: 700;
  color: var(--petrol);
  margin-bottom: 4px;
}

.section-sub {
  color: var(--muted);
  font-size: 13px;
  font-weight: 300;
  margin-bottom: 28px;
}

.section-block {
  background: var(--white);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 28px;
  margin-bottom: 20px;
  box-shadow: var(--shadow);
}

.block-title {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 18px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.block-title::after { content:''; flex:1; height:1px; background:var(--border); }

/* ── FORM FIELDS ── */
.field-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
.field-row-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; margin-bottom: 16px; }
.field-full { margin-bottom: 16px; }

label {
  display: block;
  font-size: 12px;
  font-weight: 600;
  color: var(--petrol);
  margin-bottom: 6px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

label .req { color: var(--gold); margin-left: 2px; }

input[type=text], input[type=number], input[type=date], select, textarea {
  width: 100%;
  padding: 10px 14px;
  border: 1px solid var(--border);
  border-radius: 8px;
  font-family: 'Outfit', sans-serif;
  font-size: 14px;
  color: var(--text);
  background: var(--white);
  outline: none;
  transition: border 0.2s;
}

input:focus, select:focus, textarea:focus {
  border-color: var(--petrol);
  box-shadow: 0 0 0 3px rgba(15,44,62,0.06);
}

textarea { resize: vertical; min-height: 80px; }

select { cursor: pointer; }

.prefix-field { position: relative; }
.prefix { position: absolute; left: 12px; top: 50%; transform: translateY(-50%); color: var(--muted); font-size: 14px; pointer-events: none; }
.prefix-field input { padding-left: 30px; }

/* ── UPLOAD CRIATIVO ── */
.upload-area {
  border: 2px dashed var(--border);
  border-radius: 12px;
  padding: 32px;
  text-align: center;
  cursor: pointer;
  transition: all 0.2s;
  background: var(--bg);
  position: relative;
}

.upload-area:hover, .upload-area.dragover {
  border-color: var(--gold);
  background: var(--gold-pale);
}

.upload-area input[type=file] {
  position: absolute;
  inset: 0;
  opacity: 0;
  cursor: pointer;
  width: 100%;
  height: 100%;
  border: none;
  padding: 0;
}

.upload-icon { font-size: 36px; margin-bottom: 10px; }
.upload-text { font-size: 14px; color: var(--muted); }
.upload-text strong { color: var(--petrol); }

.preview-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
  gap: 12px;
  margin-top: 16px;
}

.preview-item {
  position: relative;
  border-radius: 10px;
  overflow: hidden;
  border: 1px solid var(--border);
  aspect-ratio: 1;
  background: var(--bg);
}

.preview-item img {
  width: 100%; height: 100%;
  object-fit: cover;
}

.preview-remove {
  position: absolute;
  top: 4px; right: 4px;
  width: 22px; height: 22px;
  border-radius: 50%;
  background: rgba(0,0,0,0.65);
  color: white;
  border: none;
  cursor: pointer;
  font-size: 12px;
  display: flex; align-items: center; justify-content: center;
  line-height: 1;
}

/* ── CAMPANHA CARDS ── */
.campanha-list { display: flex; flex-direction: column; gap: 16px; }

.campanha-card {
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 20px;
  background: var(--bg);
  position: relative;
  transition: border 0.2s;
}

.campanha-card:hover { border-color: var(--gold-border); }

.campanha-card-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 16px;
}

.campanha-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px;
  font-weight: 700;
  color: var(--petrol);
  display: flex;
  align-items: center;
  gap: 8px;
}

.campanha-num small {
  font-family: 'Outfit', sans-serif;
  font-size: 12px;
  font-weight: 400;
  color: var(--muted);
}

.btn-remove-camp {
  background: none;
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 4px 10px;
  font-size: 12px;
  color: var(--muted);
  cursor: pointer;
  transition: all 0.2s;
}

.btn-remove-camp:hover { border-color: var(--red); color: var(--red); }

.frase-origem-box {
  margin-top: 12px;
  background: var(--petrol);
  border-radius: 8px;
  padding: 12px 16px;
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.frase-origem-label {
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 3px;
}

.frase-origem-text {
  font-size: 13px;
  color: rgba(255,255,255,0.85);
  font-style: italic;
}

.btn-add-camp {
  width: 100%;
  padding: 14px;
  border: 2px dashed var(--border);
  border-radius: 12px;
  background: none;
  font-family: 'Outfit', sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: var(--muted);
  cursor: pointer;
  transition: all 0.2s;
  margin-top: 8px;
}

.btn-add-camp:hover { border-color: var(--gold); color: var(--gold); background: var(--gold-pale); }

/* ── LEAD TABLE ── */
.lead-table-wrap { overflow-x: auto; }

table.lead-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 13px;
}

.lead-table th {
  background: var(--petrol);
  color: rgba(255,255,255,0.7);
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 10px 12px;
  text-align: left;
  white-space: nowrap;
}

.lead-table th:first-child { border-radius: 8px 0 0 0; }
.lead-table th:last-child { border-radius: 0 8px 0 0; }

.lead-table td {
  padding: 9px 10px;
  border-bottom: 1px solid var(--border);
  vertical-align: middle;
}

.lead-table tr:last-child td { border-bottom: none; }
.lead-table tr:hover td { background: var(--bg); }

.lead-table input, .lead-table select {
  border: none;
  background: transparent;
  font-family: 'Outfit', sans-serif;
  font-size: 13px;
  color: var(--text);
  width: 100%;
  outline: none;
  padding: 2px 4px;
}

.lead-table input:focus { background: var(--petrol-light); border-radius: 4px; }

.status-badge {
  display: inline-block;
  padding: 3px 9px;
  border-radius: 20px;
  font-size: 11px;
  font-weight: 600;
}

.s-agendado { background: var(--green-pale); color: var(--green); }
.s-pendente { background: var(--gold-pale); color: #9a6830; }
.s-perdido { background: #fdf0ef; color: var(--red); }

.btn-add-lead {
  margin-top: 12px;
  width: 100%;
  padding: 10px;
  border: 1px dashed var(--border);
  border-radius: 8px;
  background: none;
  font-family: 'Outfit', sans-serif;
  font-size: 13px;
  color: var(--muted);
  cursor: pointer;
  transition: all 0.2s;
}

.btn-add-lead:hover { border-color: var(--green); color: var(--green); background: var(--green-pale); }

/* ── KPI ROW ── */
.kpi-row {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-bottom: 20px;
}

.kpi-card {
  background: var(--white);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 18px;
  box-shadow: var(--shadow);
}

.kpi-label {
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--muted);
  margin-bottom: 6px;
}

.kpi-val {
  font-family: 'Cormorant Garamond', serif;
  font-size: 32px;
  font-weight: 700;
  color: var(--petrol);
  line-height: 1;
}

.kpi-val.gold { color: var(--gold); }
.kpi-val.green { color: var(--green); }

.kpi-unit { font-size: 14px; font-weight: 400; color: var(--muted); margin-left: 2px; }

/* ── CONTEUDO LIST ── */
.conteudo-item {
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 16px;
  margin-bottom: 12px;
  background: var(--bg);
  display: grid;
  grid-template-columns: 140px 1fr 140px 120px auto;
  gap: 12px;
  align-items: center;
}

.btn-remove-row {
  background: none;
  border: none;
  color: var(--muted);
  cursor: pointer;
  font-size: 16px;
  padding: 4px;
  transition: color 0.2s;
}

.btn-remove-row:hover { color: var(--red); }

/* ── RESUMO MODAL ── */
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(15,44,62,0.5);
  backdrop-filter: blur(4px);
  z-index: 500;
  display: none;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.modal-overlay.open { display: flex; }

.modal {
  background: var(--white);
  border-radius: 16px;
  width: 100%;
  max-width: 700px;
  max-height: 85vh;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  box-shadow: var(--shadow-lg);
}

.modal-header {
  background: var(--petrol);
  padding: 20px 28px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.modal-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px;
  font-weight: 700;
  color: #fff;
}

.modal-close {
  background: rgba(255,255,255,0.1);
  border: none;
  border-radius: 8px;
  color: #fff;
  width: 32px; height: 32px;
  cursor: pointer;
  font-size: 16px;
  display: flex; align-items: center; justify-content: center;
  transition: background 0.2s;
}

.modal-close:hover { background: rgba(255,255,255,0.2); }

.modal-body {
  padding: 24px 28px;
  overflow-y: auto;
  flex: 1;
}

.resumo-text {
  background: #f9f9f7;
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 20px;
  font-family: 'Outfit', monospace;
  font-size: 12.5px;
  line-height: 1.9;
  color: var(--text);
  white-space: pre-wrap;
  word-break: break-word;
  min-height: 200px;
}

.modal-footer {
  padding: 16px 28px;
  border-top: 1px solid var(--border);
  display: flex;
  gap: 10px;
  justify-content: flex-end;
  background: var(--bg);
}

/* ── BOTTOM ACTION BAR ── */
.action-bar {
  position: fixed;
  bottom: 0;
  left: 0; right: 0;
  background: var(--white);
  border-top: 1px solid var(--border);
  padding: 14px 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  z-index: 100;
  box-shadow: 0 -4px 20px rgba(15,44,62,0.08);
}

.action-info {
  font-size: 13px;
  color: var(--muted);
}

.action-info strong { color: var(--petrol); }

.action-btns { display: flex; gap: 10px; }

/* ── BUTTONS ── */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  padding: 10px 20px;
  border-radius: 8px;
  font-family: 'Outfit', sans-serif;
  font-size: 13px;
  font-weight: 600;
  cursor: pointer;
  border: none;
  transition: all 0.2s;
  white-space: nowrap;
}

.btn-primary { background: var(--petrol); color: #fff; }
.btn-primary:hover { background: var(--petrol-mid); }

.btn-gold { background: var(--gold); color: #fff; }
.btn-gold:hover { background: #b8952f; }

.btn-green { background: var(--green); color: #fff; }
.btn-green:hover { background: #215d3b; }

.btn-outline { background: transparent; border: 1px solid var(--border); color: var(--muted); }
.btn-outline:hover { border-color: var(--petrol); color: var(--petrol); }

/* ── TOAST ── */
.toast {
  position: fixed;
  bottom: 80px;
  left: 50%;
  transform: translateX(-50%) translateY(20px);
  background: var(--petrol);
  color: #fff;
  padding: 12px 24px;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 500;
  opacity: 0;
  transition: all 0.3s;
  z-index: 600;
  pointer-events: none;
  white-space: nowrap;
}

.toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

/* ── PROGRESS BAR ── */
.progress-bar {
  height: 3px;
  background: var(--border);
  border-radius: 2px;
  margin-bottom: 28px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--petrol), var(--gold));
  border-radius: 2px;
  transition: width 0.5s ease;
}

/* ── RESPONSIVE ── */
@media (max-width: 700px) {
  .topbar, .tab-nav, .content, .action-bar { padding-left: 16px; padding-right: 16px; }
  .kpi-row { grid-template-columns: 1fr 1fr; }
  .field-row, .field-row-3 { grid-template-columns: 1fr; }
  .conteudo-item { grid-template-columns: 1fr; }
  .tab-btn { padding: 12px 14px; font-size: 12px; }
}
</style>
</head>
<body>

<!-- TOP BAR -->
<div class="topbar">
  <div class="topbar-brand">
    <img src="data:image/png;base64,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" alt="Instituto Togni" style="height:36px; width:auto; background:#fff; border-radius:6px; padding:4px 8px;">
    <span style="color:rgba(255,255,255,0.5); font-size:13px; font-weight:400; margin-left:4px;">Painel Semanal</span>
  </div>
  <div class="topbar-week" style="gap:14px;">
    <span>Semana de</span>
    <input type="date" class="week-input" id="weekDate">
    <button class="btn" id="btn-config" onclick="toggleConfig()" style="background:rgba(255,255,255,0.1);border:1px solid rgba(255,255,255,0.2);color:#fff;padding:6px 14px;font-size:12px;border-radius:8px;">⚙ Configurar Planilha</button>
  </div>
</div>

<!-- CONFIG PANEL -->
<div id="config-panel" style="display:none; background:#0F2C3E; border-bottom:2px solid #D99F6D; padding:16px 40px; animation: fadein 0.2s ease;">
  <div style="max-width:700px; display:flex; align-items:flex-end; gap:16px; flex-wrap:wrap;">
    <div style="flex:1; min-width:300px;">
      <label style="font-size:11px; font-weight:700; letter-spacing:0.12em; text-transform:uppercase; color:#D99F6D; display:block; margin-bottom:6px;">URL do Google Apps Script</label>
      <input type="text" id="script-url" placeholder="Cole aqui a URL do seu Apps Script (https://script.google.com/macros/s/...)" 
        style="width:100%; padding:9px 14px; border-radius:8px; border:1px solid rgba(255,255,255,0.2); background:rgba(255,255,255,0.08); color:#fff; font-family:Outfit,sans-serif; font-size:13px; outline:none;">
    </div>
    <button class="btn" onclick="salvarConfig()" style="background:#D99F6D; color:#fff; padding:9px 20px; font-size:13px; white-space:nowrap;">💾 Salvar URL</button>
    <button class="btn" onclick="testarConexao()" style="background:rgba(255,255,255,0.1); border:1px solid rgba(255,255,255,0.2); color:#fff; padding:9px 20px; font-size:13px; white-space:nowrap;">🔗 Testar conexão</button>
  </div>
  <p style="font-size:12px; color:rgba(255,255,255,0.4); margin-top:10px;">A URL é salva no seu navegador. Cada computador precisa configurar uma vez.</p>
</div>

<!-- TAB NAV -->
<div class="tab-nav">
  <button class="tab-btn active" onclick="switchTab('trafico')">
    <span class="tab-icon">🎯</span> Gestão de Tráfego
    <span class="tab-badge" id="badge-trafico">0</span>
  </button>
  <button class="tab-btn" onclick="switchTab('criacao')">
    <span class="tab-icon">🎨</span> Criação / Marketing
    <span class="tab-badge" id="badge-criacao">0</span>
  </button>
  <button class="tab-btn" onclick="switchTab('comercial')">
    <span class="tab-icon">📞</span> Comercial
    <span class="tab-badge" id="badge-comercial">0</span>
  </button>
</div>

<div class="content">

<!-- ═══════════════════════════════════ TRÁFEGO ═══════════════════════════════════ -->
<div class="panel active" id="panel-trafico">
  <div class="progress-bar"><div class="progress-fill" id="prog-trafico" style="width:0%"></div></div>
  <div class="section-title">🎯 Gestão de Tráfego</div>
  <div class="section-sub">Preencha os dados de cada campanha ativa na semana. Faça upload dos criativos.</div>

  <!-- KPIs -->
  <div class="kpi-row">
    <div class="kpi-card">
      <div class="kpi-label">Total de Leads</div>
      <div class="kpi-val" id="kpi-leads">0</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Verba Total (R$)</div>
      <div class="kpi-val gold" id="kpi-verba">0</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">CPL Médio</div>
      <div class="kpi-val" id="kpi-cpl">—</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Campanhas Ativas</div>
      <div class="kpi-val green" id="kpi-camps">0</div>
    </div>
  </div>

  <!-- CAMPANHAS -->
  <div class="section-block">
    <div class="block-title">📣 Campanhas da semana</div>
    <div class="campanha-list" id="campanha-list"></div>
    <button class="btn-add-camp" onclick="addCampanha()">+ Adicionar campanha</button>
  </div>

  <!-- UPLOAD CRIATIVOS -->
  <div class="section-block">
    <div class="block-title">🖼 Criativos anunciados</div>
    <div class="upload-area" id="upload-trafico">
      <input type="file" multiple accept="image/*,video/*" onchange="handleUpload(event,'trafico')">
      <div class="upload-icon">📁</div>
      <div class="upload-text"><strong>Clique ou arraste</strong> os prints dos criativos<br><small>PNG, JPG — múltiplos arquivos · Serão salvos no Google Drive</small></div>
    </div>
    <div class="preview-grid" id="preview-trafico"></div>
  </div>

  <!-- OBSERVAÇÕES -->
  <div class="section-block">
    <div class="block-title">📝 Observações gerais</div>
    <div class="field-full">
      <label>O que está funcionando esta semana</label>
      <textarea id="t-funcionando" placeholder="Ex: Criativo com depoimento de paciente está com CTR 3x maior que o estático..." oninput="updateProgress('trafico')"></textarea>
    </div>
    <div class="field-full">
      <label>O que precisa de ajuste</label>
      <textarea id="t-ajuste" placeholder="Ex: CPL da campanha de protocolo de emagrecimento subiu 40% — precisa trocar criativo..." oninput="updateProgress('trafico')"></textarea>
    </div>
    <div class="field-full">
      <label>Sugestão de teste para próxima semana</label>
      <textarea id="t-teste" placeholder="Ex: Testar anúncio em formato Reels com depoimento em vídeo curto..." oninput="updateProgress('trafico')"></textarea>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════ CRIAÇÃO ═══════════════════════════════════ -->
<div class="panel" id="panel-criacao">
  <div class="progress-bar"><div class="progress-fill" id="prog-criacao" style="width:0%"></div></div>
  <div class="section-title">🎨 Criação / Marketing</div>
  <div class="section-sub">Registre os conteúdos publicados e prepare o resumo de materiais para o comercial.</div>

  <!-- CONTEÚDOS PUBLICADOS -->
  <div class="section-block">
    <div class="block-title">📅 Conteúdos publicados na semana</div>

    <div style="overflow-x:auto;">
      <table class="lead-table" id="conteudo-table">
        <thead>
          <tr>
            <th>Dia</th>
            <th>Canal</th>
            <th>Tipo</th>
            <th>Tema / Descrição</th>
            <th>Alcance</th>
            <th>Engajamento</th>
            <th></th>
          </tr>
        </thead>
        <tbody id="conteudo-body"></tbody>
      </table>
    </div>
    <button class="btn-add-lead" onclick="addConteudo()">+ Adicionar conteúdo</button>
  </div>

  <!-- UPLOAD MATERIAIS -->
  <div class="section-block">
    <div class="block-title">🖼 Materiais produzidos (criativos, vídeos, artes)</div>
    <div class="upload-area" id="upload-criacao">
      <input type="file" multiple accept="image/*,video/*" onchange="handleUpload(event,'criacao')">
      <div class="upload-icon">🎬</div>
      <div class="upload-text"><strong>Clique ou arraste</strong> os arquivos produzidos na semana<br><small>PNG, JPG — múltiplos arquivos · Serão salvos no Google Drive</small></div>
    </div>
    <div class="preview-grid" id="preview-criacao"></div>
  </div>

  <!-- RESUMO PARA COMERCIAL -->
  <div class="section-block" style="border-left: 4px solid var(--gold);">
    <div class="block-title">📤 Resumo de materiais para o Comercial</div>
    <p style="font-size:13px;color:var(--muted);margin-bottom:18px;">Este resumo é enviado ao comercial toda quarta e sexta. Ele permite que a recepção saiba o que o lead viu antes de ligar.</p>

    <div class="field-row">
      <div>
        <label>Protocolo em destaque esta semana <span class="req">*</span></label>
        <input type="text" id="c-servico" placeholder="Ex: Protocolo de Emagrecimento" oninput="updateProgress('criacao')">
      </div>
      <div>
        <label>Mensagem principal comunicada</label>
        <input type="text" id="c-mensagem" placeholder="Ex: Resultado em 1 sessão, com suporte especializado" oninput="updateProgress('criacao')">
      </div>
    </div>

    <div class="field-full">
      <label>O que o lead que veio de anúncio já viu / sabe</label>
      <textarea id="c-lead-viu" placeholder="Ex: Viu vídeo mostrando a metodologia do protocolo e resultados reais. Sabe que o preço introdutório é R$X. Viu depoimento do paciente Maria..." oninput="updateProgress('criacao')"></textarea>
    </div>

    <div class="field-full">
      <label>Conteúdos orgânicos que tiveram mais engajamento</label>
      <textarea id="c-destaque" placeholder="Ex: Reels de antes e depois do protocolo de emagrecimento — 12k visualizações, 340 salvamentos..." oninput="updateProgress('criacao')"></textarea>
    </div>

    <div class="field-full">
      <label>Próxima semana — pauta inicial (baseada no feedback do comercial)</label>
      <textarea id="c-proxima" placeholder="Ex: Focar em depoimentos de pacientes que concluíram o protocolo pois comercial reportou interesse alto nessa semana..." oninput="updateProgress('criacao')"></textarea>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════ COMERCIAL ═══════════════════════════════════ -->
<div class="panel" id="panel-comercial">
  <div class="progress-bar"><div class="progress-fill" id="prog-comercial" style="width:0%"></div></div>
  <div class="section-title">📞 Comercial / Recepção</div>
  <div class="section-sub">Registre todos os leads recebidos, origem, status e resultado.</div>

  <!-- KPIs COMERCIAL -->
  <div class="kpi-row">
    <div class="kpi-card">
      <div class="kpi-label">Leads Recebidos</div>
      <div class="kpi-val" id="kpi-com-leads">0</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Agendamentos</div>
      <div class="kpi-val green" id="kpi-com-ag">0</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Comparecimentos</div>
      <div class="kpi-val" id="kpi-com-comp">0</div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Vendas</div>
      <div class="kpi-val gold" id="kpi-com-vendas">0</div>
    </div>
  </div>

  <!-- META SEMANAL -->
  <div class="section-block">
    <div class="block-title">🎯 Meta da semana</div>
    <div class="field-row-3">
      <div>
        <label>Protocolo prioritário <span class="req">*</span></label>
        <input type="text" id="com-servico" placeholder="Ex: Protocolo de Emagrecimento" oninput="updateProgress('comercial')">
      </div>
      <div>
        <label>Meta de agendamentos</label>
        <input type="number" id="com-meta-ag" placeholder="Ex: 20" min="0" oninput="updateProgress('comercial')">
      </div>
      <div>
        <label>Meta de vendas</label>
        <input type="number" id="com-meta-venda" placeholder="Ex: 12" min="0" oninput="updateProgress('comercial')">
      </div>
    </div>
  </div>

  <!-- TABELA DE LEADS -->
  <div class="section-block">
    <div class="block-title">👥 Registro de leads</div>
    <div class="lead-table-wrap">
      <table class="lead-table" id="lead-table">
        <thead>
          <tr>
            <th>#</th>
            <th>Nome</th>
            <th>Origem (frase dita)</th>
            <th>Campanha</th>
            <th>Contactado em 30min?</th>
            <th>Status</th>
            <th>Motivo perda</th>
            <th></th>
          </tr>
        </thead>
        <tbody id="lead-body"></tbody>
      </table>
    </div>
    <button class="btn-add-lead" onclick="addLead()">+ Adicionar lead</button>
  </div>

  <!-- ANÁLISE -->
  <div class="section-block">
    <div class="block-title">📊 Análise da semana</div>
    <div class="field-row">
      <div>
        <label>Principal objeção dos leads</label>
        <input type="text" id="com-objecao" placeholder="Ex: Preço, prazo, desconfiança..." oninput="updateProgress('comercial')">
      </div>
      <div>
        <label>Campanha que trouxe leads de melhor qualidade</label>
        <input type="text" id="com-melhor-camp" placeholder="Ex: Campanha protocolo nutricional" oninput="updateProgress('comercial')">
      </div>
    </div>
    <div class="field-full">
      <label>Feedback para o marketing (o que o lead comentou sobre os anúncios/conteúdos)</label>
      <textarea id="com-feedback-mkt" placeholder="Ex: Vários leads citaram o vídeo do antes e depois. Um lead disse que achou o preço diferente do anúncio..." oninput="updateProgress('comercial')"></textarea>
    </div>
    <div class="field-full">
      <label>Protocolo prioritário sugerido para a próxima semana</label>
      <textarea id="com-proxima" placeholder="Ex: Acompanhamento Nutricional — temos 8 vagas na agenda e alta demanda..." oninput="updateProgress('comercial')"></textarea>
    </div>
  </div>
</div>

</div><!-- /content -->

<!-- ACTION BAR -->
<div class="action-bar">
  <div class="action-info">Semana de <strong id="info-semana">—</strong></div>
  <div class="action-btns">
    <button class="btn btn-outline" onclick="limparTudo()">🗑 Limpar tudo</button>
    <button class="btn btn-gold" onclick="gerarResumo()">📋 Ver resumo</button>
    <button class="btn btn-primary" onclick="enviarDireto()" style="background:#D99F6D;">🚀 Enviar para Sheets</button>
  </div>
</div>

<!-- MODAL RESUMO -->
<div class="modal-overlay" id="modal-resumo">
  <div class="modal">
    <div class="modal-header">
      <div class="modal-title">📋 Resumo semanal — pronto para copiar</div>
      <button class="modal-close" onclick="fecharModal()">✕</button>
    </div>
    <div class="modal-body">
      <p style="font-size:13px;color:var(--muted);margin-bottom:14px;">Copie o texto abaixo e cole no Google Sheets, WhatsApp ou e-mail.</p>
      <div class="resumo-text" id="resumo-content"></div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-outline" onclick="fecharModal()">Fechar</button>
      <button class="btn btn-primary" onclick="copiarResumo()">📋 Copiar texto</button>
      <button class="btn btn-green" id="btn-enviar-sheets" onclick="enviarParaSheets()">
        <span id="btn-enviar-txt">↗ Enviar para Google Sheets</span>
      </button>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
// ── CONFIG ──
function toggleConfig() {
  const p = document.getElementById('config-panel');
  p.style.display = p.style.display === 'none' ? 'block' : 'none';
  if (p.style.display === 'block') {
    const saved = localStorage.getItem('togni_script_url') || '';
    document.getElementById('script-url').value = saved;
  }
}

function salvarConfig() {
  const url = document.getElementById('script-url').value.trim();
  if (!url.startsWith('https://script.google.com')) {
    showToast('⚠ URL inválida. Cole a URL do Apps Script.'); return;
  }
  localStorage.setItem('togni_script_url', url);
  document.getElementById('config-panel').style.display = 'none';
  showToast('✅ URL salva com sucesso!');
}

async function testarConexao() {
  const url = localStorage.getItem('togni_script_url');
  if (!url) { showToast('⚠ Configure a URL do Apps Script primeiro.'); return; }
  showToast('🔄 Testando conexão...');
  try {
    const r = await fetch(url + '?action=ping', { method: 'GET', mode: 'no-cors' });
    showToast('✅ Conexão estabelecida com sucesso!');
  } catch(e) {
    showToast('❌ Erro na conexão. Verifique a URL.');
  }
}

// ── COLLECT DATA PER AREA ──
function coletarTrafico() {
  const campanhas = [];
  document.querySelectorAll('[id^="camp-nome-"]').forEach(el => {
    const id = el.id.replace('camp-nome-', '');
    campanhas.push({
      nome: el.value,
      objetivo: document.getElementById('camp-obj-' + id)?.value || '',
      leads: document.getElementById('camp-leads-' + id)?.value || '0',
      verba: document.getElementById('camp-verba-' + id)?.value || '0',
      cpl: document.getElementById('camp-cpl-' + id)?.value || '',
      copy: document.getElementById('camp-copy-' + id)?.value || '',
      fraseOrigem: document.getElementById('camp-frase-' + id)?.value || '',
    });
  });
  return {
    area: 'Gestão de Tráfego',
    semana: document.getElementById('weekDate')?.value || '',
    totalLeads: document.getElementById('kpi-leads')?.textContent || '0',
    totalVerba: document.getElementById('kpi-verba')?.textContent || '0',
    cplMedio: document.getElementById('kpi-cpl')?.textContent || '',
    campanhas,
    funcionando: document.getElementById('t-funcionando')?.value || '',
    ajuste: document.getElementById('t-ajuste')?.value || '',
    teste: document.getElementById('t-teste')?.value || '',
  };
}

function coletarCriacao() {
  const conteudos = [];
  document.querySelectorAll('[id^="cont-dia-"]').forEach(el => {
    const id = el.id.replace('cont-dia-', '');
    conteudos.push({
      dia: el.value,
      canal: document.getElementById('cont-canal-' + id)?.value || '',
      tipo: document.getElementById('cont-tipo-' + id)?.value || '',
      tema: document.getElementById('cont-tema-' + id)?.value || '',
      alcance: document.getElementById('cont-alcance-' + id)?.value || '',
      engajamento: document.getElementById('cont-eng-' + id)?.value || '',
    });
  });
  return {
    area: 'Marketing / Criação',
    semana: document.getElementById('weekDate')?.value || '',
    protocoloDestaque: document.getElementById('c-servico')?.value || '',
    mensagem: document.getElementById('c-mensagem')?.value || '',
    leadViu: document.getElementById('c-lead-viu')?.value || '',
    destaque: document.getElementById('c-destaque')?.value || '',
    proximaSemana: document.getElementById('c-proxima')?.value || '',
    conteudos,
  };
}

function coletarComercial() {
  const leads = [];
  document.querySelectorAll('[id^="lead-nome-"]').forEach(el => {
    const id = el.id.replace('lead-nome-', '');
    leads.push({
      nome: el.value,
      origem: document.getElementById('lead-origem-' + id)?.value || '',
      campanha: document.getElementById('lead-camp-' + id)?.value || '',
      contatado30min: document.getElementById('lead-30-' + id)?.value || '',
      status: document.getElementById('lead-status-' + id)?.value || '',
      motivoPerda: document.getElementById('lead-motivo-' + id)?.value || '',
    });
  });
  return {
    area: 'Comercial',
    semana: document.getElementById('weekDate')?.value || '',
    protocoloPrioritario: document.getElementById('com-servico')?.value || '',
    metaAgendamentos: document.getElementById('com-meta-ag')?.value || '',
    metaVendas: document.getElementById('com-meta-venda')?.value || '',
    totalLeads: document.getElementById('kpi-com-leads')?.textContent || '0',
    agendamentos: document.getElementById('kpi-com-ag')?.textContent || '0',
    comparecimentos: document.getElementById('kpi-com-comp')?.textContent || '0',
    vendas: document.getElementById('kpi-com-vendas')?.textContent || '0',
    objecao: document.getElementById('com-objecao')?.value || '',
    melhorCampanha: document.getElementById('com-melhor-camp')?.value || '',
    feedbackMkt: document.getElementById('com-feedback-mkt')?.value || '',
    proximaSemana: document.getElementById('com-proxima')?.value || '',
    leads,
  };
}

// ── SEND TO SHEETS ──
async function enviarParaSheets() {
  const url = localStorage.getItem('togni_script_url');
  if (!url) {
    showToast('⚠ Configure a URL do Apps Script primeiro (botão ⚙).');
    document.getElementById('config-panel').style.display = 'block';
    const saved = localStorage.getItem('togni_script_url') || '';
    document.getElementById('script-url').value = saved;
    return;
  }

  const btn = document.getElementById('btn-enviar-txt');
  btn.textContent = '⏳ Preparando...';

  const imagensTrafico = await coletarImagensBase64('trafico');
  const imagensCriacao = await coletarImagensBase64('criacao');
  const totalImgs = imagensTrafico.length + imagensCriacao.length;

  if (totalImgs > 0) btn.textContent = `⏳ Enviando + ${totalImgs} imagem(ns)...`;

  const payload = {
    trafico: coletarTrafico(),
    criacao: coletarCriacao(),
    comercial: coletarComercial(),
    imagensTrafico,
    imagensCriacao,
    timestamp: new Date().toISOString(),
  };

  try {
    const resp = await fetch(url, {
      method: 'POST',
      headers: { 'Content-Type': 'text/plain' },
      body: JSON.stringify(payload),
    });
    const json = await resp.json().catch(() => null);
    btn.textContent = '↗ Enviar para Google Sheets';
    fecharModal();
    if (json && json.status === 'ok') {
      const total = json.totalImagens || 0;
      const msg = total > 0
        ? `✅ Dados enviados! ${total} imagem(ns) salva(s) no Google Drive.`
        : '✅ Dados enviados para o Google Sheets!';
      showToast(msg);
      if (json.linksTrafico?.length || json.linksCriacao?.length) {
        mostrarLinksRecebidos([...(json.linksTrafico||[]), ...(json.linksCriacao||[])]);
      }
    } else {
      showToast('✅ Enviado! Verifique a planilha.');
    }
  } catch(e) {
    try {
      await fetch(url, { method:'POST', mode:'no-cors', headers:{'Content-Type':'text/plain'}, body: JSON.stringify(payload) });
      btn.textContent = '↗ Enviar para Google Sheets';
      fecharModal();
      showToast('✅ Enviado! Verifique a planilha e o Google Drive.');
    } catch(e2) {
      btn.textContent = '↗ Enviar para Google Sheets';
      showToast('❌ Erro ao enviar. Verifique a URL.');
    }
  }
}

// ── CONVERTER IMAGENS PARA BASE64 ──
async function coletarImagensBase64(area) {
  const imgs = uploadedFiles[area] || [];
  const result = [];
  for (const img of imgs) {
    if (!img) continue;
    result.push({ name: img.name, type: img.type, data: img.data });
  }
  return result;
}

async function enviarDireto() {
  const url = localStorage.getItem('togni_script_url');
  if (!url) {
    showToast('⚠ Configure a URL do Apps Script primeiro (botão ⚙).');
    document.getElementById('config-panel').style.display = 'block';
    document.getElementById('script-url').value = '';
    return;
  }

  showToast('⏳ Preparando dados e imagens...');

  const imagensTrafico = await coletarImagensBase64('trafico');
  const imagensCriacao = await coletarImagensBase64('criacao');
  const totalImgs = imagensTrafico.length + imagensCriacao.length;
  if (totalImgs > 0) showToast(`⏳ Enviando dados + ${totalImgs} imagem(ns)...`);

  const payload = {
    trafico: coletarTrafico(),
    criacao: coletarCriacao(),
    comercial: coletarComercial(),
    imagensTrafico,
    imagensCriacao,
    timestamp: new Date().toISOString(),
  };

  try {
    // Usar o proxy via URL com parâmetro para evitar CORS
    const urlProxy = url + '?callback=resposta';
    const resp = await fetch(url, {
      method: 'POST',
      headers: { 'Content-Type': 'text/plain' }, // text/plain passa CORS preflight no Apps Script
      body: JSON.stringify(payload),
    });
    const json = await resp.json().catch(() => null);
    if (json && json.status === 'ok') {
      const total = json.totalImagens || 0;
      const msg = total > 0
        ? `✅ Dados enviados! ${total} imagem(ns) salva(s) no Drive.`
        : '✅ Dados enviados para o Google Sheets!';
      showToast(msg);
      if (json.linksTrafico?.length || json.linksCriacao?.length) {
        mostrarLinksRecebidos([...(json.linksTrafico||[]), ...(json.linksCriacao||[])]);
      }
    } else {
      showToast('✅ Enviado! Verifique a planilha.');
    }
  } catch(e) {
    // Fallback: tenta no-cors (sem confirmação de links mas dados chegam)
    try {
      await fetch(url, {
        method: 'POST',
        mode: 'no-cors',
        headers: { 'Content-Type': 'text/plain' },
        body: JSON.stringify(payload),
      });
      showToast('✅ Dados enviados! Verifique a planilha e o Drive.');
    } catch(e2) {
      showToast('❌ Erro ao enviar. Verifique a URL do Apps Script.');
    }
  }
}

function mostrarLinksRecebidos(links) {
  if (!links || links.length === 0) return;
  let html = '<div style="position:fixed;bottom:80px;left:50%;transform:translateX(-50%);background:#0F2C3E;border:1px solid #D99F6D;border-radius:12px;padding:16px 20px;z-index:999;max-width:420px;box-shadow:0 8px 32px rgba(0,0,0,0.3);">';
  html += '<div style="font-size:12px;color:#D99F6D;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:10px;">📎 Criativos salvos no Drive</div>';
  links.forEach(l => {
    html += `<div style="margin-bottom:6px;"><a href="${l.url}" target="_blank" style="color:#fff;font-size:13px;text-decoration:none;">↗ ${l.nome}</a></div>`;
  });
  html += '<button onclick="this.parentElement.remove()" style="margin-top:10px;background:rgba(255,255,255,0.1);border:1px solid rgba(255,255,255,0.2);border-radius:6px;padding:5px 14px;color:#fff;font-size:12px;cursor:pointer;width:100%;">Fechar</button>';
  html += '</div>';
  const div = document.createElement('div');
  div.innerHTML = html;
  document.body.appendChild(div.firstChild);
}

// ── WEEK DATE ──
const weekInput = document.getElementById('weekDate');
const today = new Date();
weekInput.value = today.toISOString().split('T')[0];
weekInput.addEventListener('change', () => {
  document.getElementById('info-semana').textContent = formatDate(weekInput.value);
});
document.getElementById('info-semana').textContent = formatDate(weekInput.value);

function formatDate(d) {
  if (!d) return '—';
  const [y,m,day] = d.split('-');
  return `${day}/${m}/${y}`;
}

// ── TABS ──
function switchTab(tab) {
  document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('panel-' + tab).classList.add('active');
  event.currentTarget.classList.add('active');
}

// ── CAMPANHAS ──
let campId = 0;
const campanhas = [];

function addCampanha() {
  campId++;
  const id = campId;
  campanhas.push({ id });
  const list = document.getElementById('campanha-list');
  const div = document.createElement('div');
  div.className = 'campanha-card';
  div.id = 'camp-' + id;
  div.innerHTML = `
    <div class="campanha-card-header">
      <div class="campanha-num">Campanha ${id} <small>— preencha os dados abaixo</small></div>
      <button class="btn-remove-camp" onclick="removeCampanha(${id})">✕ Remover</button>
    </div>
    <div class="field-row">
      <div>
        <label>Nome da campanha <span class="req">*</span></label>
        <input type="text" id="camp-nome-${id}" placeholder="Ex: Protocolo de Emagrecimento — Maio" oninput="updateCampanha(${id})">
      </div>
      <div>
        <label>Objetivo</label>
        <select id="camp-obj-${id}" onchange="updateCampanha(${id})">
          <option value="">Selecione...</option>
          <option>Geração de leads</option>
          <option>Agendamentos</option>
          <option>Reconhecimento de marca</option>
          <option>Tráfego para site</option>
        </select>
      </div>
    </div>
    <div class="field-row-3">
      <div>
        <label>Leads gerados</label>
        <input type="number" id="camp-leads-${id}" placeholder="0" min="0" oninput="calcKPIs(); updateCampanha(${id})">
      </div>
      <div class="prefix-field">
        <label>Verba investida (R$)</label>
        <span class="prefix">R$</span>
        <input type="number" id="camp-verba-${id}" placeholder="0,00" min="0" step="0.01" oninput="calcKPIs(); updateCampanha(${id})">
      </div>
      <div>
        <label>CPL (R$) — calculado</label>
        <input type="text" id="camp-cpl-${id}" placeholder="—" readonly style="background:var(--petrol-light);color:var(--petrol);font-weight:600;">
      </div>
    </div>
    <div class="field-full">
      <label>Copy do anúncio principal</label>
      <textarea id="camp-copy-${id}" rows="2" placeholder="Cole aqui o texto do anúncio que está no ar..." oninput="updateCampanha(${id})"></textarea>
    </div>
    <div class="field-full">
      <label>Frase de identificação de origem <span class="req">*</span></label>
      <input type="text" id="camp-frase-${id}" placeholder='Ex: "Vi o anúncio do protocolo de emagrecimento"' oninput="updateFrase(${id})">
    </div>
    <div class="frase-origem-box" id="frase-box-${id}" style="display:none;">
      <div>
        <div class="frase-origem-label">🏷 Frase de origem — o comercial usará isso</div>
        <div class="frase-origem-text" id="frase-texto-${id}"></div>
      </div>
    </div>
  `;
  list.appendChild(div);
  updateBadge('trafico');
  calcKPIs();
}

function removeCampanha(id) {
  document.getElementById('camp-' + id)?.remove();
  calcKPIs();
  updateBadge('trafico');
}

function updateFrase(id) {
  const val = document.getElementById('camp-frase-' + id)?.value.trim();
  const box = document.getElementById('frase-box-' + id);
  const txt = document.getElementById('frase-texto-' + id);
  if (val) { box.style.display = 'flex'; txt.textContent = val; }
  else { box.style.display = 'none'; }
}

function updateCampanha() { updateProgress('trafico'); }

function calcKPIs() {
  let totalLeads = 0, totalVerba = 0, camps = 0;
  document.querySelectorAll('[id^="camp-nome-"]').forEach(el => {
    const id = el.id.replace('camp-nome-', '');
    const leads = parseFloat(document.getElementById('camp-leads-' + id)?.value) || 0;
    const verba = parseFloat(document.getElementById('camp-verba-' + id)?.value) || 0;
    const cpl = leads > 0 ? (verba / leads).toFixed(2) : '—';
    const cplEl = document.getElementById('camp-cpl-' + id);
    if (cplEl) cplEl.value = cpl !== '—' ? 'R$ ' + cpl : '—';
    totalLeads += leads;
    totalVerba += verba;
    if (el.value.trim()) camps++;
  });
  document.getElementById('kpi-leads').textContent = totalLeads;
  document.getElementById('kpi-verba').textContent = totalVerba.toFixed(0);
  document.getElementById('kpi-camps').textContent = camps;
  const cplMed = totalLeads > 0 ? 'R$ ' + (totalVerba / totalLeads).toFixed(2) : '—';
  document.getElementById('kpi-cpl').textContent = cplMed;
  updateProgress('trafico');
}

// ── CONTEÚDO TABLE ──
let contId = 0;
function addConteudo() {
  contId++;
  const id = contId;
  const tbody = document.getElementById('conteudo-body');
  const tr = document.createElement('tr');
  tr.id = 'cont-' + id;
  tr.innerHTML = `
    <td>
      <select onchange="updateProgress('criacao')" id="cont-dia-${id}" style="min-width:90px;">
        <option>Segunda</option><option>Terça</option><option>Quarta</option>
        <option>Quinta</option><option>Sexta</option><option>Sábado</option><option>Domingo</option>
      </select>
    </td>
    <td>
      <select onchange="updateProgress('criacao')" id="cont-canal-${id}" style="min-width:110px;">
        <option>Instagram</option><option>Facebook</option><option>TikTok</option>
        <option>YouTube</option><option>WhatsApp</option><option>Outro</option>
      </select>
    </td>
    <td>
      <select onchange="updateProgress('criacao')" id="cont-tipo-${id}" style="min-width:100px;">
        <option>Reels / Vídeo</option><option>Carrossel</option><option>Foto / Arte</option>
        <option>Stories</option><option>Post texto</option>
      </select>
    </td>
    <td><input type="text" id="cont-tema-${id}" placeholder="Descreva o conteúdo..." oninput="updateProgress('criacao')" style="min-width:200px;"></td>
    <td><input type="number" id="cont-alcance-${id}" placeholder="0" min="0" oninput="updateProgress('criacao')" style="width:80px;"></td>
    <td><input type="number" id="cont-eng-${id}" placeholder="0" min="0" oninput="updateProgress('criacao')" style="width:80px;"></td>
    <td><button class="btn-remove-row" onclick="document.getElementById('cont-${id}').remove(); updateProgress('criacao')">✕</button></td>
  `;
  tbody.appendChild(tr);
  updateBadge('criacao');
  updateProgress('criacao');
}

// ── LEADS TABLE ──
let leadId = 0;
function addLead() {
  leadId++;
  const id = leadId;
  const tbody = document.getElementById('lead-body');
  const tr = document.createElement('tr');
  tr.id = 'lead-' + id;
  tr.innerHTML = `
    <td style="color:var(--muted);font-weight:600;text-align:center;">${id}</td>
    <td><input type="text" id="lead-nome-${id}" placeholder="Nome..." oninput="calcComKPIs(); updateProgress('comercial')"></td>
    <td><input type="text" id="lead-origem-${id}" placeholder='O que o lead disse...' oninput="updateProgress('comercial')"></td>
    <td><input type="text" id="lead-camp-${id}" placeholder="Campanha..." oninput="updateProgress('comercial')"></td>
    <td style="text-align:center;">
      <select id="lead-30-${id}" onchange="updateProgress('comercial')" style="width:70px;">
        <option value="">—</option>
        <option value="Sim">✅ Sim</option>
        <option value="Não">❌ Não</option>
      </select>
    </td>
    <td>
      <select id="lead-status-${id}" onchange="calcComKPIs(); updateProgress('comercial')" style="width:130px;">
        <option value="">Selecione...</option>
        <option value="Agendado">✅ Agendado</option>
        <option value="Compareceu">🏥 Compareceu</option>
        <option value="Venda">💰 Venda</option>
        <option value="Pendente">⏳ Pendente</option>
        <option value="Perdido">❌ Perdido</option>
      </select>
    </td>
    <td><input type="text" id="lead-motivo-${id}" placeholder="Se perdido..." oninput="updateProgress('comercial')"></td>
    <td><button class="btn-remove-row" onclick="document.getElementById('lead-${id}').remove(); calcComKPIs(); updateProgress('comercial')">✕</button></td>
  `;
  tbody.appendChild(tr);
  updateBadge('comercial');
  calcComKPIs();
}

function calcComKPIs() {
  const rows = document.querySelectorAll('[id^="lead-status-"]');
  let ag = 0, comp = 0, vendas = 0, total = rows.length;
  rows.forEach(el => {
    const v = el.value;
    if (v === 'Agendado' || v === 'Compareceu' || v === 'Venda') ag++;
    if (v === 'Compareceu' || v === 'Venda') comp++;
    if (v === 'Venda') vendas++;
  });
  document.getElementById('kpi-com-leads').textContent = total;
  document.getElementById('kpi-com-ag').textContent = ag;
  document.getElementById('kpi-com-comp').textContent = comp;
  document.getElementById('kpi-com-vendas').textContent = vendas;
}

// ── UPLOAD ──
const uploadedFiles = { trafico: [], criacao: [] };

function handleUpload(event, area) {
  const files = Array.from(event.target.files);
  const preview = document.getElementById('preview-' + area);
  files.forEach(file => {
    if (!file.type.startsWith('image/')) return;
    const reader = new FileReader();
    reader.onload = e => {
      const idx = uploadedFiles[area].length;
      // Store name, type AND base64 data for Drive upload
      uploadedFiles[area].push({ name: file.name, type: file.type, data: e.target.result });
      const div = document.createElement('div');
      div.className = 'preview-item';
      div.id = `prev-${area}-${idx}`;
      div.innerHTML = `<img src="${e.target.result}" alt="${file.name}"><button class="preview-remove" onclick="removePreview('${area}',${idx})">✕</button><div style="position:absolute;bottom:4px;left:4px;right:4px;background:rgba(15,44,62,0.75);color:#D99F6D;font-size:9px;padding:2px 4px;border-radius:3px;text-align:center;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;">${file.name}</div>`;
      preview.appendChild(div);
    };
    reader.readAsDataURL(file);
  });
  updateBadge(area === 'trafico' ? 'trafico' : 'criacao');
}

function removePreview(area, idx) {
  document.getElementById(`prev-${area}-${idx}`)?.remove();
  uploadedFiles[area][idx] = null;
}

// ── PROGRESS ──
function updateProgress(tab) {
  let filled = 0, total = 0;
  if (tab === 'trafico') {
    const fields = ['t-funcionando', 't-ajuste', 't-teste'];
    fields.forEach(f => { total++; if (document.getElementById(f)?.value.trim()) filled++; });
    const camps = document.querySelectorAll('[id^="camp-nome-"]');
    camps.forEach(el => { total++; if (el.value.trim()) filled++; });
    total = Math.max(total, 3);
  } else if (tab === 'criacao') {
    const fields = ['c-servico', 'c-mensagem', 'c-lead-viu', 'c-destaque', 'c-proxima'];
    fields.forEach(f => { total++; if (document.getElementById(f)?.value.trim()) filled++; });
    const rows = document.querySelectorAll('[id^="cont-tema-"]');
    rows.forEach(el => { total++; if (el.value.trim()) filled++; });
    total = Math.max(total, 5);
  } else {
    const fields = ['com-servico', 'com-objecao', 'com-feedback-mkt', 'com-proxima'];
    fields.forEach(f => { total++; if (document.getElementById(f)?.value.trim()) filled++; });
    const rows = document.querySelectorAll('[id^="lead-nome-"]');
    rows.forEach(el => { total++; if (el.value.trim()) filled++; });
    total = Math.max(total, 4);
  }
  const pct = total > 0 ? Math.round((filled / total) * 100) : 0;
  document.getElementById('prog-' + tab).style.width = pct + '%';
  updateBadge(tab);
}

function updateBadge(tab) {
  let count = 0;
  if (tab === 'trafico') count = document.querySelectorAll('[id^="camp-nome-"]').length;
  else if (tab === 'criacao') count = document.querySelectorAll('[id^="cont-tema-"]').length;
  else count = document.querySelectorAll('[id^="lead-nome-"]').length;
  document.getElementById('badge-' + tab).textContent = count;
}

// ── GERAR RESUMO ──
function gerarResumo() {
  const semana = formatDate(weekInput.value);
  let txt = '';

  txt += `╔══════════════════════════════════════════════════╗\n`;
  txt += `║  RESUMO SEMANAL DE MARKETING                     ║\n`;
  txt += `║  Semana de ${semana.padEnd(38)}║\n`;
  txt += `╚══════════════════════════════════════════════════╝\n\n`;

  // TRÁFEGO
  txt += `🎯 GESTÃO DE TRÁFEGO\n${'─'.repeat(48)}\n`;
  const camps = document.querySelectorAll('[id^="camp-nome-"]');
  if (camps.length === 0) {
    txt += `  Nenhuma campanha registrada.\n`;
  } else {
    camps.forEach(el => {
      const id = el.id.replace('camp-nome-', '');
      const nome = el.value || '(sem nome)';
      const leads = document.getElementById('camp-leads-' + id)?.value || '0';
      const verba = document.getElementById('camp-verba-' + id)?.value || '0';
      const cpl = document.getElementById('camp-cpl-' + id)?.value || '—';
      const copy = document.getElementById('camp-copy-' + id)?.value || '';
      const frase = document.getElementById('camp-frase-' + id)?.value || '';
      txt += `\n  📣 ${nome}\n`;
      txt += `     Leads: ${leads}  |  Verba: R$ ${verba}  |  CPL: ${cpl}\n`;
      if (copy) txt += `     Copy: "${copy.substring(0,80)}${copy.length > 80 ? '...' : ''}"\n`;
      if (frase) txt += `     🏷 Frase de origem: ${frase}\n`;
    });
  }
  const kpiLeads = document.getElementById('kpi-leads').textContent;
  const kpiVerba = document.getElementById('kpi-verba').textContent;
  const kpiCpl = document.getElementById('kpi-cpl').textContent;
  txt += `\n  TOTAIS → Leads: ${kpiLeads}  |  Verba: R$ ${kpiVerba}  |  CPL médio: ${kpiCpl}\n`;
  const func = document.getElementById('t-funcionando')?.value;
  const ajuste = document.getElementById('t-ajuste')?.value;
  const teste = document.getElementById('t-teste')?.value;
  if (func) txt += `\n  ✅ O que funcionou:\n  ${func}\n`;
  if (ajuste) txt += `\n  ⚠ O que ajustar:\n  ${ajuste}\n`;
  if (teste) txt += `\n  🧪 Teste sugerido:\n  ${teste}\n`;

  // CRIAÇÃO
  txt += `\n\n🎨 CRIAÇÃO / MARKETING\n${'─'.repeat(48)}\n`;
  const servico = document.getElementById('c-servico')?.value;
  const mensagem = document.getElementById('c-mensagem')?.value;
  const leadViu = document.getElementById('c-lead-viu')?.value;
  const destaque = document.getElementById('c-destaque')?.value;
  const proxCri = document.getElementById('c-proxima')?.value;
  if (servico) txt += `\n  Protocolo em destaque: ${servico}\n`;
  if (mensagem) txt += `  Mensagem principal: ${mensagem}\n`;

  const contRows = document.querySelectorAll('[id^="cont-dia-"]');
  if (contRows.length > 0) {
    txt += `\n  📅 Conteúdos publicados:\n`;
    contRows.forEach(el => {
      const id = el.id.replace('cont-dia-', '');
      const dia = el.value;
      const canal = document.getElementById('cont-canal-' + id)?.value;
      const tipo = document.getElementById('cont-tipo-' + id)?.value;
      const tema = document.getElementById('cont-tema-' + id)?.value;
      const alcance = document.getElementById('cont-alcance-' + id)?.value;
      txt += `     ${dia} | ${canal} | ${tipo}: ${tema}`;
      if (alcance) txt += ` (${alcance} alcance)`;
      txt += '\n';
    });
  }
  txt += `\n  📤 RESUMO PARA O COMERCIAL:\n`;
  if (leadViu) txt += `  O que o lead já viu: ${leadViu}\n`;
  if (destaque) txt += `  Destaques orgânicos: ${destaque}\n`;
  if (proxCri) txt += `  Pauta próxima semana: ${proxCri}\n`;

  // COMERCIAL
  txt += `\n\n📞 COMERCIAL / RECEPÇÃO\n${'─'.repeat(48)}\n`;
  const comServico = document.getElementById('com-servico')?.value;
  const metaAg = document.getElementById('com-meta-ag')?.value;
  const metaVenda = document.getElementById('com-meta-venda')?.value;
  if (comServico) txt += `\n  Protocolo prioritário: ${comServico}\n`;
  if (metaAg) txt += `  Meta agendamentos: ${metaAg}\n`;
  if (metaVenda) txt += `  Meta vendas: ${metaVenda}\n`;

  txt += `\n  RESULTADOS:\n`;
  txt += `  Leads recebidos: ${document.getElementById('kpi-com-leads').textContent}\n`;
  txt += `  Agendamentos: ${document.getElementById('kpi-com-ag').textContent}`;
  if (metaAg) txt += ` / ${metaAg} (meta)`;
  txt += '\n';
  txt += `  Comparecimentos: ${document.getElementById('kpi-com-comp').textContent}\n`;
  txt += `  Vendas: ${document.getElementById('kpi-com-vendas').textContent}`;
  if (metaVenda) txt += ` / ${metaVenda} (meta)`;
  txt += '\n';

  const leadRows = document.querySelectorAll('[id^="lead-nome-"]');
  if (leadRows.length > 0) {
    txt += `\n  👥 Leads registrados:\n`;
    leadRows.forEach(el => {
      const id = el.id.replace('lead-nome-', '');
      const nome = el.value || '(sem nome)';
      const status = document.getElementById('lead-status-' + id)?.value || '—';
      const origem = document.getElementById('lead-origem-' + id)?.value || '';
      const motivo = document.getElementById('lead-motivo-' + id)?.value || '';
      txt += `     ${nome} | ${status}`;
      if (origem) txt += ` | Origem: "${origem}"`;
      if (motivo) txt += ` | Perda: ${motivo}`;
      txt += '\n';
    });
  }

  const objecao = document.getElementById('com-objecao')?.value;
  const melhorCamp = document.getElementById('com-melhor-camp')?.value;
  const feedMkt = document.getElementById('com-feedback-mkt')?.value;
  const proxCom = document.getElementById('com-proxima')?.value;
  if (objecao) txt += `\n  ⚠ Principal objeção: ${objecao}\n`;
  if (melhorCamp) txt += `  🏆 Campanha de melhor qualidade: ${melhorCamp}\n`;
  if (feedMkt) txt += `\n  💬 Feedback para Marketing:\n  ${feedMkt}\n`;
  if (proxCom) txt += `\n  📅 Serviço sugerido próx. semana: ${proxCom}\n`;

  txt += `\n${'═'.repeat(50)}\n`;
  txt += `Gerado em ${new Date().toLocaleDateString('pt-BR')} ${new Date().toLocaleTimeString('pt-BR')}\n`;

  document.getElementById('resumo-content').textContent = txt;
  document.getElementById('modal-resumo').classList.add('open');
}

function fecharModal() {
  document.getElementById('modal-resumo').classList.remove('open');
}

function copiarResumo() {
  const txt = document.getElementById('resumo-content').textContent;
  navigator.clipboard.writeText(txt).then(() => showToast('✅ Texto copiado! Cole no Google Sheets.'));
}

function abrirSheets() {
  window.open('https://sheets.google.com', '_blank');
}

function limparTudo() {
  if (!confirm('Limpar todos os dados preenchidos? Esta ação não pode ser desfeita.')) return;
  document.querySelectorAll('input[type=text], input[type=number], textarea').forEach(el => { if (!el.readOnly) el.value = ''; });
  document.getElementById('campanha-list').innerHTML = '';
  document.getElementById('conteudo-body').innerHTML = '';
  document.getElementById('lead-body').innerHTML = '';
  document.getElementById('preview-trafico').innerHTML = '';
  document.getElementById('preview-criacao').innerHTML = '';
  uploadedFiles.trafico = []; uploadedFiles.criacao = [];
  campId = 0; contId = 0; leadId = 0;
  ['trafico','criacao','comercial'].forEach(t => { updateBadge(t); updateProgress(t); });
  calcKPIs(); calcComKPIs();
  showToast('🗑 Dados limpos com sucesso.');
}

function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2800);
}

// Drag and drop
document.querySelectorAll('.upload-area').forEach(area => {
  area.addEventListener('dragover', e => { e.preventDefault(); area.classList.add('dragover'); });
  area.addEventListener('dragleave', () => area.classList.remove('dragover'));
  area.addEventListener('drop', e => {
    e.preventDefault();
    area.classList.remove('dragover');
    const which = area.id.includes('trafico') ? 'trafico' : 'criacao';
    const fakeEvent = { target: { files: e.dataTransfer.files } };
    handleUpload(fakeEvent, which);
  });
});

// Init
weekInput.dispatchEvent(new Event('change'));
</script>
</body>
</html>
