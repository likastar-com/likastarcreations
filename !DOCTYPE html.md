<!DOCTYPE html>  
  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>French Charm Finds — Content Studio</title>  
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">  
<style>  
  :root {  
    --cream: #f5f0e8;  
    --parchment: #ede7d9;  
    --warm-white: #faf7f2;  
    --ink: #1e1610;  
    --brown: #5a3e28;  
    --gold: #8B6914;  
    --taupe: #9a8878;  
    --border: #d4c9b5;  
    --pillar-1: #7a5c3a;  
    --pillar-2: #3a5c4a;  
    --pillar-3: #3a3a5c;  
    --pillar-4: #5c3a3a;  
  }  
  
- { box-sizing: border-box; margin: 0; padding: 0; }  
  
body {  
background: var(–cream);  
font-family: ‘Jost’, sans-serif;  
color: var(–ink);  
min-height: 100vh;  
position: relative;  
overflow-x: hidden;  
}  
  
/* Grain texture overlay */  
body::before {  
content: ‘’;  
position: fixed;  
inset: 0;  
background-image: url(“data:image/svg+xml,%3Csvg viewBox=‘0 0 256 256’ xmlns=‘http://www.w3.org/2000/svg’%3E%3Cfilter id=‘noise’%3E%3CfeTurbulence type=‘fractalNoise’ baseFrequency=‘0.9’ numOctaves=‘4’ stitchTiles=‘stitch’/%3E%3C/filter%3E%3Crect width=‘100%25’ height=‘100%25’ filter=‘url(%23noise)’ opacity=‘0.04’/%3E%3C/svg%3E”);  
pointer-events: none;  
z-index: 0;  
opacity: 0.4;  
}  
  
.container {  
max-width: 720px;  
margin: 0 auto;  
padding: 0 1.5rem 4rem;  
position: relative;  
z-index: 1;  
}  
  
/* Header */  
header {  
padding: 2.5rem 0 2rem;  
border-bottom: 1px solid var(–border);  
margin-bottom: 2rem;  
position: relative;  
}  
  
.header-eyebrow {  
font-family: ‘Jost’, sans-serif;  
font-weight: 200;  
font-size: 10px;  
letter-spacing: 0.35em;  
text-transform: uppercase;  
color: var(–gold);  
margin-bottom: 0.5rem;  
}  
  
.header-title {  
font-family: ‘Cormorant Garamond’, serif;  
font-weight: 300;  
font-size: clamp(1.6rem, 4vw, 2.2rem);  
color: var(–ink);  
letter-spacing: 0.02em;  
line-height: 1.2;  
}  
  
.header-title em {  
font-style: italic;  
color: var(–brown);  
}  
  
.header-sub {  
font-size: 11px;  
font-weight: 300;  
color: var(–taupe);  
letter-spacing: 0.1em;  
margin-top: 0.4rem;  
}  
  
/* Decorative line */  
.deco-line {  
display: flex;  
align-items: center;  
gap: 1rem;  
margin: 1.5rem 0;  
}  
.deco-line::before, .deco-line::after {  
content: ‘’;  
flex: 1;  
height: 1px;  
background: var(–border);  
}  
.deco-line span {  
font-size: 10px;  
color: var(–taupe);  
letter-spacing: 0.2em;  
text-transform: uppercase;  
font-weight: 300;  
}  
  
/* Section labels */  
.section-label {  
font-size: 9px;  
font-weight: 400;  
letter-spacing: 0.25em;  
text-transform: uppercase;  
color: var(–gold);  
margin-bottom: 0.7rem;  
display: block;  
}  
  
/* Mode tabs */  
.mode-tabs {  
display: flex;  
gap: 0;  
border: 1px solid var(–border);  
border-radius: 2px;  
overflow: hidden;  
margin-bottom: 2rem;  
background: var(–warm-white);  
}  
  
.mode-tab {  
flex: 1;  
padding: 10px 6px;  
border: none;  
background: transparent;  
font-family: ‘Jost’, sans-serif;  
font-size: 10px;  
font-weight: 300;  
letter-spacing: 0.12em;  
text-transform: uppercase;  
color: var(–taupe);  
cursor: pointer;  
transition: all 0.25s;  
border-right: 1px solid var(–border);  
position: relative;  
}  
  
.mode-tab:last-child { border-right: none; }  
  
.mode-tab.active {  
background: var(–ink);  
color: var(–cream);  
}  
  
.mode-tab:hover:not(.active) {  
background: var(–parchment);  
color: var(–brown);  
}  
  
/* Pillar grid */  
.pillars {  
display: grid;  
grid-template-columns: repeat(2, 1fr);  
gap: 8px;  
margin-bottom: 1.75rem;  
}  
  
.pillar-btn {  
padding: 10px 14px;  
border: 1px solid var(–border);  
border-radius: 2px;  
background: transparent;  
font-family: ‘Jost’, sans-serif;  
font-size: 11px;  
font-weight: 300;  
letter-spacing: 0.05em;  
color: var(–taupe);  
cursor: pointer;  
transition: all 0.2s;  
text-align: left;  
display: flex;  
align-items: center;  
gap: 8px;  
}  
  
.pillar-btn span.emoji { font-size: 14px; }  
  
.pillar-btn.active-1 { border-color: var(–pillar-1); background: rgba(122,92,58,0.06); color: var(–pillar-1); }  
.pillar-btn.active-2 { border-color: var(–pillar-2); background: rgba(58,92,74,0.06); color: var(–pillar-2); }  
.pillar-btn.active-3 { border-color: var(–pillar-3); background: rgba(58,58,92,0.06); color: var(–pillar-3); }  
.pillar-btn.active-4 { border-color: var(–pillar-4); background: rgba(92,58,58,0.06); color: var(–pillar-4); }  
  
.pillar-btn:hover:not([class*=“active”]) {  
background: var(–parchment);  
color: var(–brown);  
border-color: var(–brown);  
}  
  
/* Inputs */  
.input-group { margin-bottom: 1.5rem; }  
  
textarea, input[type=“text”], input[type=“number”] {  
width: 100%;  
padding: 12px 14px;  
border: 1px solid var(–border);  
border-radius: 2px;  
background: var(–warm-white);  
color: var(–ink);  
font-family: ‘Cormorant Garamond’, serif;  
font-size: 15px;  
font-weight: 300;  
line-height: 1.7;  
resize: vertical;  
transition: border-color 0.2s;  
-webkit-appearance: none;  
}  
  
textarea:focus, input:focus {  
outline: none;  
border-color: var(–brown);  
}  
  
textarea::placeholder, input::placeholder {  
color: var(–taupe);  
font-style: italic;  
font-size: 14px;  
}  
  
/* Image upload */  
.upload-area {  
border: 1px dashed var(–border);  
border-radius: 2px;  
padding: 14px 18px;  
display: flex;  
align-items: center;  
gap: 12px;  
cursor: pointer;  
transition: all 0.2s;  
background: var(–warm-white);  
}  
  
.upload-area:hover { border-color: var(–brown); background: var(–parchment); }  
  
.upload-icon {  
width: 32px;  
height: 32px;  
border: 1px solid var(–border);  
border-radius: 2px;  
display: flex;  
align-items: center;  
justify-content: center;  
color: var(–taupe);  
font-size: 14px;  
flex-shrink: 0;  
}  
  
.upload-text { font-size: 12px; color: var(–taupe); font-weight: 300; letter-spacing: 0.05em; }  
.upload-text strong { color: var(–brown); font-weight: 400; }  
.upload-preview { display: flex; align-items: center; gap: 8px; }  
.upload-preview img { width: 36px; height: 36px; object-fit: cover; border-radius: 2px; border: 1px solid var(–border); }  
  
input[type=“file”] { display: none; }  
  
/* Performance log */  
.perf-panel {  
border: 1px solid var(–border);  
border-radius: 2px;  
overflow: hidden;  
margin-bottom: 1.75rem;  
}  
  
.perf-header {  
display: flex;  
justify-content: space-between;  
align-items: center;  
padding: 10px 14px;  
background: var(–parchment);  
border-bottom: 1px solid var(–border);  
}  
  
.perf-toggle {  
background: none;  
border: none;  
font-family: ‘Jost’, sans-serif;  
font-size: 10px;  
font-weight: 300;  
letter-spacing: 0.1em;  
color: var(–taupe);  
cursor: pointer;  
text-transform: uppercase;  
}  
  
.perf-body { padding: 12px 14px; background: var(–warm-white); }  
  
.perf-entry {  
display: flex;  
justify-content: space-between;  
align-items: center;  
padding: 6px 0;  
border-bottom: 1px solid var(–parchment);  
font-size: 12px;  
}  
  
.perf-entry:last-child { border-bottom: none; }  
.perf-entry .hook-text { font-family: ‘Cormorant Garamond’, serif; font-style: italic; color: var(–brown); font-size: 13px; flex: 1; }  
.perf-entry .views { color: var(–gold); font-weight: 500; font-size: 12px; margin-left: 12px; white-space: nowrap; }  
  
.perf-add {  
display: flex;  
gap: 8px;  
margin-top: 10px;  
}  
  
.perf-add input { font-family: ‘Jost’, sans-serif; font-size: 12px; padding: 8px 10px; }  
.perf-add input:first-child { flex: 2; }  
.perf-add input:last-of-type { flex: 1; }  
  
.btn-add {  
padding: 8px 14px;  
border: 1px solid var(–brown);  
background: transparent;  
color: var(–brown);  
font-family: ‘Jost’, sans-serif;  
font-size: 10px;  
letter-spacing: 0.1em;  
text-transform: uppercase;  
cursor: pointer;  
border-radius: 2px;  
transition: all 0.2s;  
white-space: nowrap;  
}  
  
.btn-add:hover { background: var(–brown); color: var(–cream); }  
  
/* Generate button */  
.btn-generate {  
width: 100%;  
padding: 15px;  
background: var(–ink);  
color: var(–cream);  
border: none;  
border-radius: 2px;  
font-family: ‘Jost’, sans-serif;  
font-size: 11px;  
font-weight: 300;  
letter-spacing: 0.2em;  
text-transform: uppercase;  
cursor: pointer;  
transition: all 0.25s;  
position: relative;  
overflow: hidden;  
}  
  
.btn-generate::after {  
content: ‘’;  
position: absolute;  
inset: 0;  
background: linear-gradient(135deg, transparent 0%, rgba(255,255,255,0.04) 50%, transparent 100%);  
transform: translateX(-100%);  
transition: transform 0.4s;  
}  
  
.btn-generate:hover::after { transform: translateX(100%); }  
.btn-generate:hover { background: var(–brown); }  
.btn-generate:disabled { background: var(–taupe); cursor: not-allowed; }  
  
/* Spinner */  
.spinner-wrap { display: flex; justify-content: center; padding: 2rem; }  
  
.spinner {  
width: 24px;  
height: 24px;  
border: 1.5px solid var(–border);  
border-top-color: var(–brown);  
border-radius: 50%;  
animation: spin 0.7s linear infinite;  
}  
  
@keyframes spin { to { transform: rotate(360deg); } }  
  
/* Output */  
.output-wrap {  
margin-top: 1.5rem;  
animation: fadeUp 0.4s ease;  
}  
  
@keyframes fadeUp {  
from { opacity: 0; transform: translateY(10px); }  
to { opacity: 1; transform: translateY(0); }  
}  
  
.output-header {  
display: flex;  
justify-content: space-between;  
align-items: center;  
margin-bottom: 0.75rem;  
}  
  
.btn-copy {  
padding: 5px 12px;  
border: 1px solid var(–border);  
background: transparent;  
color: var(–taupe);  
font-family: ‘Jost’, sans-serif;  
font-size: 10px;  
letter-spacing: 0.1em;  
text-transform: uppercase;  
cursor: pointer;  
border-radius: 2px;  
transition: all 0.2s;  
}  
  
.btn-copy:hover { border-color: var(–brown); color: var(–brown); }  
.btn-copy.copied { border-color: var(–pillar-2); color: var(–pillar-2); }  
  
.output-box {  
background: var(–warm-white);  
border: 1px solid var(–border);  
border-radius: 2px;  
padding: 1.5rem 1.75rem;  
}  
  
.output-line {  
font-family: ‘Cormorant Garamond’, serif;  
font-size: 15px;  
font-weight: 300;  
line-height: 1.85;  
color: var(–ink);  
margin-bottom: 0.3rem;  
}  
  
.output-line.heading {  
font-family: ‘Jost’, sans-serif;  
font-size: 10px;  
font-weight: 400;  
letter-spacing: 0.2em;  
text-transform: uppercase;  
color: var(–gold);  
margin-top: 1rem;  
margin-bottom: 0.3rem;  
}  
  
.output-line.heading:first-child { margin-top: 0; }  
  
/* Error */  
.error-msg {  
font-size: 12px;  
color: var(–pillar-4);  
font-style: italic;  
margin-bottom: 1rem;  
padding: 10px 14px;  
border: 1px solid rgba(92,58,58,0.2);  
border-radius: 2px;  
background: rgba(92,58,58,0.04);  
}  
  
/* Footer */  
.footer-note {  
text-align: center;  
font-size: 10px;  
color: var(–taupe);  
letter-spacing: 0.12em;  
font-style: italic;  
margin-top: 2.5rem;  
font-family: ‘Cormorant Garamond’, serif;  
font-weight: 300;  
}  
  
/* Hidden section */  
.section { margin-bottom: 1.5rem; }  
.hidden { display: none; }  
  
@media (max-width: 480px) {  
.pillars { grid-template-columns: 1fr 1fr; }  
.mode-tabs { flex-wrap: wrap; }  
.mode-tab { flex: 0 0 50%; border-bottom: 1px solid var(–border); }  
.mode-tab:nth-child(4), .mode-tab:nth-child(5) { border-bottom: none; }  
}  
</style>  
  
</head>  
<body>  
  
<div class="container">  
  
  <header>  
    <p class="header-eyebrow">Content Studio</p>  
    <h1 class="header-title">@french_charm_<em>finds</em></h1>  
    <p class="header-sub">Paris insider · 20 years · still discovering</p>  
  </header>  
  
  <!-- Mode tabs -->  
  
<span class="section-label">Format</span>  
  
  <div class="mode-tabs">  
    <button class="mode-tab active" onclick="setMode('reels', this)">Reel Ideas</button>  
    <button class="mode-tab" onclick="setMode('captions', this)">Captions</button>  
    <button class="mode-tab" onclick="setMode('hooks', this)">Hooks</button>  
    <button class="mode-tab" onclick="setMode('seo', this)">SEO</button>  
    <button class="mode-tab" onclick="setMode('strategy', this)">Strategy</button>  
  </div>  
  
  <!-- Content pillars -->  
  
  <div class="section" id="pillar-section">  
    <span class="section-label">Content Pillar</span>  
    <div class="pillars">  
      <button class="pillar-btn" id="p-historical" onclick="togglePillar('historical', 1)">  
        <span class="emoji">🏛️</span> Historical Paris  
      </button>  
      <button class="pillar-btn" id="p-discovery" onclick="togglePillar('discovery', 2)">  
        <span class="emoji">🔍</span> Insider Discovery  
      </button>  
      <button class="pillar-btn" id="p-atmospheric" onclick="togglePillar('atmospheric', 3)">  
        <span class="emoji">🌙</span> Atmospheric Moment  
      </button>  
      <button class="pillar-btn" id="p-reportage" onclick="togglePillar('reportage', 4)">  
        <span class="emoji">🛍️</span> Place Reportage  
      </button>  
    </div>  
  </div>  
  
  <!-- Brief -->  
  
  <div class="section input-group">  
    <span class="section-label" id="brief-label">Your Brief</span>  
    <textarea id="brief" rows="3" placeholder="e.g. a quiet café on Rue Montorgueil, Tuesday morning, autumn light…"></textarea>  
  </div>  
  
  <!-- Inspiration upload -->  
  
  <div class="section" id="upload-section">  
    <span class="section-label">Inspiration Screenshot <span style="font-weight:200;text-transform:none;letter-spacing:0">(optional)</span></span>  
    <div class="upload-area" onclick="document.getElementById('fileInput').click()">  
      <div class="upload-icon">⊕</div>  
      <div id="upload-content">  
        <div class="upload-text"><strong>Upload image</strong> — hook style & tone reference</div>  
        <div class="upload-text" style="font-size:10px;margin-top:2px">The AI will borrow its energy, not its content</div>  
      </div>  
    </div>  
    <input type="file" id="fileInput" accept="image/*" onchange="handleImage(this)">  
    <div id="upload-preview" style="display:none;margin-top:8px;display:none">  
      <div class="upload-preview">  
        <img id="preview-img" src="" alt="">  
        <span style="font-size:12px;color:var(--taupe)" id="preview-name"></span>  
        <button onclick="removeImage()" style="background:none;border:none;color:var(--taupe);font-size:11px;cursor:pointer;margin-left:auto;font-family:'Jost',sans-serif">remove</button>  
      </div>  
    </div>  
  </div>  
  
  <!-- Performance log (strategy mode only) -->  
  
  <div class="section hidden" id="perf-section">  
    <div class="perf-panel">  
      <div class="perf-header">  
        <span class="section-label" style="margin:0">Performance Log</span>  
        <button class="perf-toggle" onclick="togglePerfLog()">show entries</button>  
      </div>  
      <div class="perf-body hidden" id="perf-body">  
        <div id="perf-entries">  
          <div class="perf-entry">  
            <span class="hook-text">"Parisian children have come here since 1847."</span>  
            <span class="views">3,914 views</span>  
          </div>  
          <div class="perf-entry">  
            <span class="hook-text">"This part of Paris didn't exist 50 years ago."</span>  
            <span class="views">202 views</span>  
          </div>  
          <div class="perf-entry">  
            <span class="hook-text">"Thursday is a Friday apéro rehearsal."</span>  
            <span class="views">79 views (2h)</span>  
          </div>  
        </div>  
        <div class="perf-add">  
          <input type="text" id="new-hook" placeholder="Hook text…">  
          <input type="text" id="new-views" placeholder="Views">  
          <button class="btn-add" onclick="addEntry()">Add</button>  
        </div>  
      </div>  
    </div>  
  </div>  
  
  <!-- Error -->  
  
  <div id="error-msg" class="error-msg hidden"></div>  
  
  <!-- Generate -->  
  
  <button class="btn-generate" id="btn-gen" onclick="generate()">  
    Generate Reel Ideas  
  </button>  
  
  <!-- Spinner -->  
  
  <div class="spinner-wrap hidden" id="spinner">  
    <div class="spinner"></div>  
  </div>  
  
  <!-- Output -->  
  
  <div id="output-wrap" class="output-wrap hidden">  
    <div class="output-header">  
      <span class="section-label" style="margin:0">Output</span>  
      <button class="btn-copy" id="copy-btn" onclick="copyOutput()">Copy</button>  
    </div>  
    <div class="output-box" id="output-box"></div>  
  </div>  
  
  <p class="footer-note">2–3 reels a week · insider perspective always · one strong image beats three average ones</p>  
  
</div>  
  
<script>  
const SYSTEM = `You are the dedicated content strategist and writer for @french_charm_finds, a French lifestyle Instagram account run by Inna, a 20-year Paris insider. You create refined, cinematic, emotionally resonant content — written from an insider's perspective, never a tourist's.  
  
TONE: Elegant. Observant. Calm. Lightly poetic. Visually aware. Concise.  
NEVER use: generic marketing language, loud influencer energy, clickbait, artificial phrasing, philosophical overwriting, the words "magical", "hidden gem", or "journey".  
  
CONTENT PILLARS:  
- 🏛️ Historical Paris — facts that reframe familiar places (BEST PERFORMING: "Parisian children have come here since 1847" = 3.9K views)  
- 🔍 Insider Discovery — "I thought I knew Paris" revelations  
- 🌙 Atmospheric Moments — time of day, season, mood    
- 🛍️ Place Reportage — shops, expos, addresses worth knowing  
  
HOOK PRINCIPLES:  
- Best hooks are time-anchored (a date, a historical fact) OR create personal discovery tension  
- Pure aesthetics underperform — always add a curiosity gap  
- Lead with emotion or curiosity, never with description  
- Witty one-liners also perform well: "Thursday is a Friday apéro rehearsal" got 16.1% like rate and 5.4% repost rate  
  
OUTPUT FORMATS:  
REEL IDEAS: 3 ideas. Each: Hook (1 sharp sentence) · Visual direction (1–2 sentences) · Text overlay per clip · Closing line. Reels = 10–20 seconds.  
CAPTIONS: 2 options. Option A: poetic. Option B: observational. 2–3 short sentences. No hashtags.  
SEO COMMENT: 15–20 Paris lifestyle keywords, copy-paste ready, plus 5 hashtags.  
HOOKS ONLY: 5 hooks ranked from most emotional to most curiosity-driven.  
STRATEGY: Analyse data, give direction on what's working, what to avoid, which pillar to prioritise, one specific reel idea.  
  
Always make creative assumptions. Only ask for clarification if genuinely too vague.  
The account posts 2–3 reels/week. Instagram is a creative outlet, not a revenue source.`;  
  
let currentMode = 'reels';  
let activePillar = null;  
let imageData = null;  
let imageType = null;  
let outputText = '';  
let perfLogVisible = false;  
  
const MODES = {  
  reels: 'Reel Ideas',  
  captions: 'Captions',  
  hooks: 'Hooks Only',  
  seo: 'SEO Comment',  
  strategy: 'Strategy Advice'  
};  
  
const PILLARS = {  
  historical: { label: '🏛️ Historical Paris', num: 1 },  
  discovery: { label: '🔍 Insider Discovery', num: 2 },  
  atmospheric: { label: '🌙 Atmospheric Moment', num: 3 },  
  reportage: { label: '🛍️ Place Reportage', num: 4 },  
};  
  
function setMode(mode, el) {  
  currentMode = mode;  
  document.querySelectorAll('.mode-tab').forEach(t => t.classList.remove('active'));  
  el.classList.add('active');  
  document.getElementById('btn-gen').textContent = 'Generate ' + MODES[mode];  
  document.getElementById('output-wrap').classList.add('hidden');  
  document.getElementById('error-msg').classList.add('hidden');  
  
  const isStrategy = mode === 'strategy';  
  document.getElementById('pillar-section').classList.toggle('hidden', isStrategy);  
  document.getElementById('upload-section').classList.toggle('hidden', isStrategy);  
  document.getElementById('perf-section').classList.toggle('hidden', !isStrategy);  
  
  const briefLabel = document.getElementById('brief-label');  
  const briefTA = document.getElementById('brief');  
  if (isStrategy) {  
    briefLabel.textContent = 'Additional Context (optional)';  
    briefTA.placeholder = 'Any specific questions or focus areas for strategy review…';  
  } else {  
    briefLabel.textContent = 'Your Brief';  
    briefTA.placeholder = 'e.g. a quiet café on Rue Montorgueil, Tuesday morning, autumn light…';  
  }  
}  
  
function togglePillar(id, num) {  
  const btn = document.getElementById('p-' + id);  
  if (activePillar === id) {  
    activePillar = null;  
    btn.className = 'pillar-btn';  
  } else {  
    if (activePillar) {  
      document.getElementById('p-' + activePillar).className = 'pillar-btn';  
    }  
    activePillar = id;  
    btn.className = 'pillar-btn active-' + num;  
  }  
}  
  
function handleImage(input) {  
  const file = input.files[0];  
  if (!file) return;  
  const reader = new FileReader();  
  reader.onload = (e) => {  
    imageData = e.target.result.split(',')[1];  
    imageType = file.type;  
    document.getElementById('preview-img').src = e.target.result;  
    document.getElementById('preview-name').textContent = file.name;  
    document.getElementById('upload-preview').style.display = 'flex';  
    document.querySelector('.upload-area').style.borderColor = 'var(--brown)';  
  };  
  reader.readAsDataURL(file);  
}  
  
function removeImage() {  
  imageData = null;  
  imageType = null;  
  document.getElementById('fileInput').value = '';  
  document.getElementById('upload-preview').style.display = 'none';  
  document.querySelector('.upload-area').style.borderColor = '';  
}  
  
function togglePerfLog() {  
  perfLogVisible = !perfLogVisible;  
  document.getElementById('perf-body').classList.toggle('hidden', !perfLogVisible);  
  document.querySelector('.perf-toggle').textContent = perfLogVisible ? 'hide' : 'show entries';  
}  
  
function addEntry() {  
  const hook = document.getElementById('new-hook').value.trim();  
  const views = document.getElementById('new-views').value.trim();  
  if (!hook || !views) return;  
  const div = document.createElement('div');  
  div.className = 'perf-entry';  
  div.innerHTML = `<span class="hook-text">"${hook}"</span><span class="views">${parseInt(views).toLocaleString()} views</span>`;  
  document.getElementById('perf-entries').appendChild(div);  
  document.getElementById('new-hook').value = '';  
  document.getElementById('new-views').value = '';  
}  
  
function getPerformanceData() {  
  const entries = document.querySelectorAll('.perf-entry');  
  return Array.from(entries).map(e => {  
    const hook = e.querySelector('.hook-text')?.textContent || '';  
    const views = e.querySelector('.views')?.textContent || '';  
    return `${hook} → ${views}`;  
  }).join('\n');  
}  
  
function buildPrompt() {  
  const brief = document.getElementById('brief').value.trim();  
  const pillarInfo = activePillar ? PILLARS[activePillar] : null;  
  
  if (currentMode === 'strategy') {  
    const data = getPerformanceData();  
    return `Analyse my recent reel performance and give me concrete strategy advice for @french_charm_finds.\n\nPerformance data:\n${data || 'No data yet.'}\n\nContext: ${brief || 'General strategy review for 2–3 reels per week.'}\n\nGive me: 1) What content pattern is working, 2) What to avoid, 3) Which content pillar to prioritise next, 4) One specific reel idea to try this week.`;  
  }  
  
  let prompt = `Generate ${currentMode === 'reels' ? 'REEL IDEAS' : currentMode === 'captions' ? 'CAPTIONS' : currentMode === 'hooks' ? 'HOOKS ONLY' : 'SEO COMMENT BLOCK'} for @french_charm_finds.`;  
  if (pillarInfo) prompt += `\n\nContent pillar: ${pillarInfo.label}`;  
  if (brief) prompt += `\n\nBrief: ${brief}`;  
  if (imageData) prompt += `\n\nI've uploaded an inspiration screenshot. Analyse its hook style and caption tone, then apply that energy — not the content — to my brief.`;  
  if (!brief && !activePillar) prompt += `\n\nMake creative assumptions based on the account's style and best-performing content.`;  
  return prompt;  
}  
  
async function generate() {  
  const brief = document.getElementById('brief').value.trim();  
  if (!brief && currentMode !== 'strategy' && !activePillar) {  
    showError('Add a brief or select a content pillar to continue.');  
    return;  
  }  
  
  hideError();  
  setLoading(true);  
  document.getElementById('output-wrap').classList.add('hidden');  
  
  try {  
    const userContent = [];  
    if (imageData) {  
      userContent.push({ type: 'image', source: { type: 'base64', media_type: imageType, data: imageData } });  
    }  
    userContent.push({ type: 'text', text: buildPrompt() });  
  
    const res = await fetch('https://api.anthropic.com/v1/messages', {  
      method: 'POST',  
      headers: { 'Content-Type': 'application/json' },  
      body: JSON.stringify({  
        model: 'claude-sonnet-4-20250514',  
        max_tokens: 1000,  
        system: SYSTEM,  
        messages: [{ role: 'user', content: userContent }]  
      })  
    });  
  
    const data = await res.json();  
    outputText = data.content?.map(b => b.text || '').join('\n') || 'No response received.';  
    renderOutput(outputText);  
  } catch (e) {  
    showError('Something went wrong. Please try again.');  
  }  
  setLoading(false);  
}  
  
function renderOutput(text) {  
  const box = document.getElementById('output-box');  
  box.innerHTML = '';  
  const lines = text.split('\n');  
  lines.forEach(line => {  
    const div = document.createElement('div');  
    const cleaned = line.replace(/\*\*/g, '').replace(/^#{1,3}\s*/, '');  
    const isHeading = /^(OPTION|HOOK|REEL|IDEA|SEO|STRATEGY|\d+\.|—)/.test(cleaned) || cleaned.endsWith(':') || /^[A-Z][A-Z\s]{4,}$/.test(cleaned.trim());  
    div.className = 'output-line' + (isHeading ? ' heading' : '');  
    div.textContent = cleaned || '\u00A0';  
    box.appendChild(div);  
  });  
  document.getElementById('output-wrap').classList.remove('hidden');  
}  
  
function copyOutput() {  
  navigator.clipboard.writeText(outputText).then(() => {  
    const btn = document.getElementById('copy-btn');  
    btn.textContent = 'Copied ✓';  
    btn.classList.add('copied');  
    setTimeout(() => { btn.textContent = 'Copy'; btn.classList.remove('copied'); }, 2000);  
  });  
}  
  
function setLoading(state) {  
  document.getElementById('spinner').classList.toggle('hidden', !state);  
  document.getElementById('btn-gen').disabled = state;  
  document.getElementById('btn-gen').textContent = state ? 'Generating…' : 'Generate ' + MODES[currentMode];  
}  
  
function showError(msg) {  
  const el = document.getElementById('error-msg');  
  el.textContent = msg;  
  el.classList.remove('hidden');  
}  
  
function hideError() {  
  document.getElementById('error-msg').classList.add('hidden');  
}  
</script>  
  
</body>  
</html>  
