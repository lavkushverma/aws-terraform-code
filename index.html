<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Terraform Doc Generator — AI Powered</title>
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=JetBrains+Mono:wght@400;600&family=Sora:wght@400;600;700;800&display=swap');

    :root {
      --bg:        #0a0f1e;
      --surface:   #111827;
      --surface2:  #1e293b;
      --border:    #1f2d42;
      --accent:    #7c3aed;
      --accent2:   #38bdf8;
      --text:      #e2e8f0;
      --muted:     #64748b;
      --green:     #22c55e;
      --red:       #ef4444;
      --yellow:    #eab308;
    }

    * { box-sizing: border-box; }
    body {
      font-family: 'Sora', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
    }

    /* ---- Background grid ---- */
    body::before {
      content: '';
      position: fixed; inset: 0; z-index: 0;
      background-image:
        linear-gradient(rgba(124,58,237,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(124,58,237,0.04) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
    }

    .wrap { position: relative; z-index: 1; max-width: 900px; margin: 0 auto; padding: 2.5rem 1.5rem; }

    /* ---- Header ---- */
    header { text-align: center; margin-bottom: 3rem; }
    .logo {
      display: inline-flex; align-items: center; gap: 12px;
      background: var(--surface); border: 1px solid var(--border);
      border-radius: 14px; padding: 10px 20px; margin-bottom: 1.5rem;
      box-shadow: 0 0 30px rgba(124,58,237,0.15);
    }
    .logo-icon {
      width: 36px; height: 36px; border-radius: 8px;
      background: linear-gradient(135deg, #7c3aed, #38bdf8);
      display: flex; align-items: center; justify-content: center;
      font-size: 18px;
    }
    .logo-text { font-size: 0.9rem; color: var(--muted); }
    .logo-text strong { color: var(--text); font-weight: 600; }

    h1 { font-size: 2.4rem; font-weight: 800; margin: 0 0 0.5rem;
         background: linear-gradient(135deg, #fff 30%, #7c3aed);
         -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    .subtitle { color: var(--muted); font-size: 1rem; }

    /* ---- Prompt Section ---- */
    .section-label {
      font-size: 0.72rem; font-weight: 700; letter-spacing: 0.12em;
      color: var(--accent2); text-transform: uppercase; margin-bottom: 0.6rem;
    }

    .prompt-box {
      background: var(--surface2); border: 1px solid var(--border);
      border-radius: 14px; overflow: hidden;
      box-shadow: 0 0 0 1px rgba(56,189,248,0.05);
      margin-bottom: 1.5rem;
    }
    .prompt-header {
      background: #1a2640; padding: 10px 16px;
      display: flex; align-items: center; justify-content: space-between;
      border-bottom: 1px solid var(--border);
    }
    .prompt-header span { font-family: 'Fira Code', monospace; font-size: 0.8rem; color: var(--accent2); }
    .copy-prompt-btn {
      font-size: 0.75rem; padding: 4px 12px; border-radius: 6px;
      background: var(--border); color: var(--text); border: none; cursor: pointer;
      transition: background 0.2s;
    }
    .copy-prompt-btn:hover { background: var(--accent); }
    .copy-prompt-btn.ok { background: #22c55e; color: #fff; }

    .prompt-body {
      font-family: 'JetBrains Mono', monospace; font-size: 0.8rem;
      color: #94a3b8; line-height: 1.75; padding: 1.2rem 1.4rem;
      white-space: pre-wrap; max-height: 340px; overflow-y: auto;
      scrollbar-width: thin; scrollbar-color: var(--border) transparent;
    }
    .hl-key  { color: #c084fc; }
    .hl-val  { color: #4ade80; }
    .hl-sec  { color: #f9a8d4; }
    .hl-com  { color: var(--muted); font-style: italic; }
    .hl-var  { color: #38bdf8; }

    /* ---- Generator Form ---- */
    .card {
      background: var(--surface); border: 1px solid var(--border);
      border-radius: 16px; padding: 2rem; margin-bottom: 1.5rem;
    }

    .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    @media (max-width: 600px) { .form-grid { grid-template-columns: 1fr; } }

    label { display: block; font-size: 0.78rem; color: var(--muted); margin-bottom: 5px; }
    input, select, textarea {
      width: 100%; background: var(--surface2); border: 1px solid var(--border);
      color: var(--text); border-radius: 8px; padding: 0.6rem 0.9rem;
      font-size: 0.88rem; font-family: inherit; outline: none;
      transition: border-color 0.2s;
    }
    input:focus, select:focus, textarea:focus { border-color: var(--accent); }
    textarea { resize: vertical; min-height: 90px; font-family: 'JetBrains Mono', monospace; font-size: 0.8rem; }

    .generate-btn {
      width: 100%; margin-top: 1.5rem;
      background: linear-gradient(135deg, #7c3aed, #5b21b6);
      color: #fff; border: none; border-radius: 10px;
      padding: 0.85rem 1.5rem; font-size: 1rem; font-weight: 700;
      cursor: pointer; transition: all 0.2s; letter-spacing: 0.01em;
      display: flex; align-items: center; justify-content: center; gap: 8px;
    }
    .generate-btn:hover:not(:disabled) { transform: translateY(-1px); box-shadow: 0 8px 24px rgba(124,58,237,0.35); }
    .generate-btn:disabled { opacity: 0.5; cursor: not-allowed; transform: none; }

    /* ---- Loader ---- */
    .loader {
      display: none; text-align: center; padding: 3rem;
      color: var(--muted); font-size: 0.9rem;
    }
    .loader.show { display: block; }
    .spinner {
      width: 36px; height: 36px; border-radius: 50%;
      border: 3px solid var(--border); border-top-color: var(--accent);
      animation: spin 0.7s linear infinite; margin: 0 auto 1rem;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    /* ---- Result ---- */
    #result-section { display: none; }
    #result-section.show { display: block; }

    .result-header {
      display: flex; align-items: center; justify-content: space-between;
      margin-bottom: 1rem;
    }
    .result-header h2 { font-size: 1.1rem; font-weight: 700; }

    .result-actions { display: flex; gap: 8px; }
    .action-btn {
      font-size: 0.78rem; padding: 6px 14px; border-radius: 7px;
      border: 1px solid var(--border); background: var(--surface2);
      color: var(--text); cursor: pointer; transition: all 0.2s;
    }
    .action-btn:hover { border-color: var(--accent); color: var(--accent); }
    .action-btn.primary { background: var(--accent); border-color: var(--accent); color: #fff; }
    .action-btn.primary:hover { background: #6d28d9; }

    .iframe-wrap {
      border: 1px solid var(--border); border-radius: 12px; overflow: hidden;
      background: #fff;
    }
    #preview-frame { width: 100%; height: 620px; border: none; display: block; }

    /* ---- Prompt Badge ---- */
    .badge {
      display: inline-flex; align-items: center; gap: 6px;
      background: rgba(124,58,237,0.1); border: 1px solid rgba(124,58,237,0.3);
      border-radius: 999px; padding: 4px 12px;
      font-size: 0.72rem; color: #a78bfa;
    }

    /* error */
    .error-box {
      background: rgba(239,68,68,0.08); border: 1px solid rgba(239,68,68,0.3);
      border-radius: 10px; padding: 1rem 1.2rem; color: #fca5a5;
      font-size: 0.85rem; display: none; margin-top: 1rem;
    }
    .error-box.show { display: block; }
  </style>
</head>
<body>
<div class="wrap">

  <!-- Header -->
  <header>
    <div class="logo">
      <div class="logo-icon">⚡</div>
      <div><div class="logo-text"><strong>Terraform Doc Generator</strong></div>
      <div class="logo-text">Powered by Claude AI</div></div>
    </div>
    <h1>Generate Terraform Docs</h1>
    <p class="subtitle">Describe any AWS resource — get a beautiful, syntax-highlighted doc page instantly.</p>
  </header>

  <!-- The Prompt — fully visible and copyable -->
  <div class="card">
    <div class="section-label">🧠 The Prompt Used for Every Generation</div>
    <p style="color:var(--muted);font-size:0.82rem;margin-bottom:1rem;">
      This is the exact system + user prompt injected into Claude when you click Generate. You can copy and reuse it anywhere.
    </p>
    <div class="prompt-box">
      <div class="prompt-header">
        <span>system_prompt.txt</span>
        <button class="copy-prompt-btn" onclick="copyPrompt()">📋 Copy Prompt</button>
      </div>
      <div class="prompt-body" id="prompt-display"></div>
    </div>
    <div class="badge">✦ This prompt is injected verbatim before your input</div>
  </div>

  <!-- Generator -->
  <div class="card">
    <div class="section-label">🚀 Generate a Doc Page</div>
    <div class="form-grid">
      <div>
        <label>AWS Resource / Service</label>
        <input id="resource" type="text" placeholder="e.g. S3 Bucket, RDS Instance, Lambda" value="S3 Bucket with versioning and encryption" />
      </div>
      <div>
        <label>Environment / Context</label>
        <select id="env">
          <option>Production</option>
          <option>Staging</option>
          <option>Development</option>
          <option>Multi-environment</option>
        </select>
      </div>
      <div>
        <label>Terraform Files to Include</label>
        <input id="files" type="text" placeholder="main.tf, variables.tf, outputs.tf" value="main.tf, variables.tf, outputs.tf, security.tf" />
      </div>
      <div>
        <label>Special Requirements (optional)</label>
        <input id="extras" type="text" placeholder="e.g. KMS encryption, lifecycle rules, IAM policy" value="KMS encryption, versioning, lifecycle policy, bucket policy" />
      </div>
    </div>
    <button class="generate-btn" id="gen-btn" onclick="generate()">
      <span>⚡</span> Generate Documentation Page
    </button>
    <div class="error-box" id="error-box"></div>
  </div>

  <!-- Loader -->
  <div class="loader" id="loader">
    <div class="spinner"></div>
    <p>Claude is writing Terraform code and building your doc page…</p>
    <p style="font-size:0.78rem;margin-top:0.4rem;color:#475569;">This takes ~15–25 seconds</p>
  </div>

  <!-- Result -->
  <div id="result-section">
    <div class="result-header">
      <h2>✅ Generated Page</h2>
      <div class="result-actions">
        <button class="action-btn" onclick="copyHTML()">📋 Copy HTML</button>
        <button class="action-btn primary" onclick="downloadHTML()">⬇ Download</button>
      </div>
    </div>
    <div class="iframe-wrap">
      <iframe id="preview-frame" sandbox="allow-scripts allow-same-origin"></iframe>
    </div>
  </div>

</div>

<script>
// =====================================================================
// THE PROMPT — this is what gets sent to Claude for every generation
// =====================================================================
const SYSTEM_PROMPT = `You are an expert Terraform and AWS documentation writer.

Your job is to generate a COMPLETE, SELF-CONTAINED HTML documentation page for a Terraform resource. The page must match this exact design style:

DESIGN RULES (non-negotiable):
- Dark background: #0f172a body, #1e293b code blocks, #334155 code headers
- Font: Inter (body) + Fira Code (monospace) from Google Fonts
- Tailwind CSS via CDN: https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4
- Purple accent color: #7c3aed for tabs, buttons, glow
- Syntax highlighting with <span> tags using these classes:
  .kw { color: #c084fc }      /* keywords: resource, variable, output, data */
  .type { color: #38bdf8 }    /* resource type strings */
  .str { color: #4ade80 }     /* string values */
  .attr { color: #f9a8d4 }    /* attribute names */
  .comment { color: #64748b; font-style: italic }
  .func { color: #fbbf24 }    /* functions like jsonencode */
  .bool { color: #fb923c }    /* true/false/numbers */
  .var { color: #67e8f9 }     /* variable references like var.xxx */
  .bracket { color: #94a3b8 } /* braces and brackets */

PAGE STRUCTURE (follow this exactly):
1. <header> — Logo icon + resource name title + link to Terraform registry docs
2. Hero section — H2 title with purple <span>, description paragraph
3. Architecture diagram — flex boxes showing the resource flow (e.g. App → Resource → AWS Service)
4. Tab navigation — one tab per .tf file requested, plus a "Complete" tab
5. Each tab — a .code-block with macOS-style dots header, copy button, and <pre> with syntax-highlighted HCL code
6. Usage steps — 3 cards: Initialize, Plan, Apply with code
7. Two info cards: Key Features (✓ list) and Prerequisites (• list)
8. <footer>

TERRAFORM CODE RULES:
- Write REAL, production-grade, working Terraform HCL code
- Include: provider config, required_version >= 1.0, data sources, main resource, security group if relevant, outputs
- Use variables for all configurable values
- Add meaningful comments in the code
- Follow AWS best practices (least privilege IAM, encryption at rest, tagging)
- Tags must always include: Name, Environment, ManagedBy = "terraform"

JAVASCRIPT (required):
- Tab switching: activate tab on click, show/hide .tab-content divs
- Copy button: copies the <pre> innerText to clipboard, shows "✅ Copied!" then reverts

OUTPUT: Return ONLY the complete HTML. No markdown, no explanation, no code fences. Start with <!DOCTYPE html> and end with </html>.`;

const USER_PROMPT_TEMPLATE = (resource, env, files, extras) =>
`Generate a documentation page for the following Terraform resource:

Resource: ${resource}
Environment: ${env}
Files to include as tabs: ${files}
Special requirements: ${extras || 'None'}

Follow all design rules and code rules from the system prompt exactly.`;

// =====================================================================
// Render prompt in the display box with highlights
// =====================================================================
function renderPromptDisplay() {
  const lines = SYSTEM_PROMPT.split('\n');
  const el = document.getElementById('prompt-display');
  el.innerHTML = lines.map(line => {
    if (line.startsWith('//') || line.startsWith('#')) return `<span class="hl-com">${esc(line)}</span>`;
    if (line.match(/^[A-Z][A-Z\s\/]+:/)) return `<span class="hl-sec">${esc(line)}</span>`;
    if (line.match(/^\./)) return `<span class="hl-val">${esc(line)}</span>`;
    if (line.match(/^- /)) return `<span style="color:#e2e8f0">${esc(line)}</span>`;
    return `<span>${esc(line)}</span>`;
  }).join('\n');
}
function esc(s) {
  return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
}

// =====================================================================
// Copy prompt
// =====================================================================
function copyPrompt() {
  navigator.clipboard.writeText(SYSTEM_PROMPT).then(() => {
    const btn = document.querySelector('.copy-prompt-btn');
    btn.textContent = '✅ Copied!'; btn.classList.add('ok');
    setTimeout(() => { btn.textContent = '📋 Copy Prompt'; btn.classList.remove('ok'); }, 2000);
  });
}

// =====================================================================
// Generate
// =====================================================================
let generatedHTML = '';

async function generate() {
  const resource = document.getElementById('resource').value.trim();
  const env = document.getElementById('env').value;
  const files = document.getElementById('files').value.trim();
  const extras = document.getElementById('extras').value.trim();

  if (!resource) { showError('Please enter an AWS resource name.'); return; }

  const btn = document.getElementById('gen-btn');
  btn.disabled = true;
  document.getElementById('loader').classList.add('show');
  document.getElementById('result-section').classList.remove('show');
  document.getElementById('error-box').classList.remove('show');

  try {
    const response = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 8000,
        system: SYSTEM_PROMPT,
        messages: [{
          role: 'user',
          content: USER_PROMPT_TEMPLATE(resource, env, files, extras)
        }]
      })
    });

    const data = await response.json();

    if (!response.ok) {
      throw new Error(data?.error?.message || `API error ${response.status}`);
    }

    const text = data.content?.map(b => b.text || '').join('') || '';
    // Strip any accidental markdown fences
    generatedHTML = text.replace(/^```html?\n?/i, '').replace(/```\s*$/,'').trim();

    // Render in iframe
    const frame = document.getElementById('preview-frame');
    frame.srcdoc = generatedHTML;
    document.getElementById('result-section').classList.add('show');
    document.getElementById('result-section').scrollIntoView({ behavior: 'smooth', block: 'start' });

  } catch(err) {
    showError('Error: ' + err.message);
  } finally {
    btn.disabled = false;
    document.getElementById('loader').classList.remove('show');
  }
}

function showError(msg) {
  const box = document.getElementById('error-box');
  box.textContent = msg; box.classList.add('show');
}

function copyHTML() {
  if (!generatedHTML) return;
  navigator.clipboard.writeText(generatedHTML).then(() => {
    const btn = event.target;
    btn.textContent = '✅ Copied!';
    setTimeout(() => btn.textContent = '📋 Copy HTML', 2000);
  });
}

function downloadHTML() {
  if (!generatedHTML) return;
  const blob = new Blob([generatedHTML], { type: 'text/html' });
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  const name = document.getElementById('resource').value.toLowerCase().replace(/\s+/g,'-').replace(/[^a-z0-9-]/g,'');
  a.download = `terraform-${name || 'doc'}.html`;
  a.click();
}

// Init
renderPromptDisplay();
</script>
</body>
</html>
