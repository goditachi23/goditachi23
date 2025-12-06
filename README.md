<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Vedansh — Technical Repository README</title>
  <style>
    :root{
      --bg:#0b1020; --panel:#071023; --accent:#00e6a8; --accent2:#6b8cff; --muted:#9aa7c7; --glass: rgba(255,255,255,0.04);
      --mono: 'SFMono-Regular', Consolas, "Liberation Mono", Menlo, monospace;
    }
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;background: radial-gradient(1200px 600px at 10% 10%, rgba(107,140,255,0.06), transparent), radial-gradient(800px 400px at 90% 90%, rgba(0,230,168,0.03), transparent), var(--bg);color:#e6eef8;-webkit-font-smoothing:antialiased}
    .wrap{max-width:1100px;margin:36px auto;padding:36px;border-radius:14px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);box-shadow: 0 8px 40px rgba(2,6,23,0.6);position:relative;overflow:hidden}

    /* Header */
    .header{display:flex;align-items:center;gap:20px}
    .logo{width:90px;height:90px;border-radius:14px;background:linear-gradient(135deg,var(--accent),var(--accent2));display:flex;align-items:center;justify-content:center;box-shadow: 0 8px 30px rgba(107,140,255,0.12);transform:rotate(-12deg)}
    .logo svg{width:56px;height:56px;filter:drop-shadow(0 6px 20px rgba(107,140,255,0.15))}
    h1{margin:0;font-size:28px;letter-spacing: -0.4px}
    .sub{color:var(--muted);margin-top:6px}

    /* Neon badges */
    .badges{display:flex;gap:8px;margin-top:14px}
    .badge{padding:8px 12px;border-radius:999px;background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);font-family:var(--mono);font-size:12px;color:var(--accent2);box-shadow:0 6px 18px rgba(107,140,255,0.04)}

    /* Grid */
    .grid{display:grid;grid-template-columns:1fr 420px;gap:24px;margin-top:26px}

    /* Card */
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.015), transparent);border-radius:12px;padding:18px;border:1px solid rgba(255,255,255,0.03)}

    /* Terminal */
    .terminal{background:linear-gradient(180deg,#071025, #041122);padding:18px;border-radius:10px;color:#c9f7e6;font-family:var(--mono);font-size:13px;line-height:1.6;border:1px solid rgba(0,230,168,0.06);box-shadow: inset 0 2px 18px rgba(0,0,0,0.6)}
    .term-line{display:flex;gap:10px;align-items:center}
    .prompt{color:var(--accent);}
    .cursor{display:inline-block;width:8px;height:16px;background:var(--accent);margin-left:6px;animation:blink 1s steps(2) infinite}
    @keyframes blink{50%{opacity:0}}

    /* Tech list */
    .tech{display:flex;flex-wrap:wrap;gap:8px}
    .pill{background:var(--glass);padding:8px 10px;border-radius:999px;font-family:var(--mono);font-size:13px;border:1px solid rgba(255,255,255,0.02)}

    /* Animated pipeline */
    .pipeline{display:flex;align-items:center;gap:14px;justify-content:center;margin-top:18px}
    .stage{width:86px;height:86px;border-radius:12px;background:linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));display:flex;flex-direction:column;align-items:center;justify-content:center;border:1px solid rgba(255,255,255,0.03);position:relative}
    .stage h4{margin:0;font-size:12px}
    .connector{height:6px;width:80px;background:linear-gradient(90deg,var(--accent),var(--accent2));border-radius:4px;box-shadow:0 6px 14px rgba(107,140,255,0.08);position:relative;overflow:hidden}
    .pulse{position:absolute;left:-30%;top:-40%;width:60%;height:200%;background:radial-gradient(circle at 30% 30%, rgba(255,255,255,0.08), transparent);transform:rotate(15deg);animation:slide 3s linear infinite}
    @keyframes slide{0%{left:-50%}100%{left:150%}}

    /* Cards list */
    .projects{display:grid;gap:12px}
    .project{display:flex;justify-content:space-between;align-items:center;padding:12px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.012), transparent);border:1px solid rgba(255,255,255,0.02)}
    .proj-meta{display:flex;flex-direction:column}
    .proj-title{font-weight:600}
    .proj-desc{font-size:13px;color:var(--muted);margin-top:6px}

    /* Footer */
    footer{margin-top:20px;color:var(--muted);font-size:13px;text-align:center}

    /* Floating particles */
    .particles{position:absolute;inset:0;pointer-events:none}
    .particle{position:absolute;border-radius:999px;opacity:0.06}

    /* Responsive */
    @media (max-width:980px){.grid{grid-template-columns:1fr}.logo{width:76px;height:76px}}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="particles" aria-hidden>
      <div class="particle" style="width:420px;height:420px;left:-120px;top:-80px;background:linear-gradient(135deg,var(--accent2),transparent)"></div>
      <div class="particle" style="width:260px;height:260px;right:-60px;bottom:-100px;background:linear-gradient(45deg,var(--accent),transparent)"></div>
    </div>

    <header class="header">
      <div class="logo" title="Vedansh">
        <!-- compact V logo -->
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="g1" x1="0" x2="1">
              <stop offset="0" stop-color="#00E6A8"/>
              <stop offset="1" stop-color="#6B8CFF"/>
            </linearGradient>
          </defs>
          <path d="M20 18 L50 78 L80 18" stroke="url(#g1)" stroke-width="9" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
        </svg>
      </div>
      <div style="flex:1">
        <h1>Vedansh — Technical Repository</h1>
        <div class="sub">Polyglot code samples • JavaScript-focused • Moving into DevOps & CI/CD workflows</div>
        <div class="badges">
          <span class="badge">JavaScript</span>
          <span class="badge">HTML • CSS</span>
          <span class="badge">Android • Java</span>
          <span class="badge">DevOps • CI/CD (future)</span>
          <span class="badge">Open Source</span>
        </div>
      </div>
    </header>

    <div class="grid">
      <main>
        <section class="card">
          <h2 style="margin:0 0 6px 0">Repository Overview</h2>
          <p style="color:var(--muted);margin-top:6px">This repository collects practical, production-oriented code snippets and projects across front-end, mobile and backend stacks — with a strong emphasis on JavaScript. You'll find polished components, complete micro-projects, and soon: automated pipelines, IaC examples, and repeatable CI/CD templates for modern DevOps workflows.</p>

          <div style="margin-top:16px" class="terminal" aria-hidden>
            <div class="term-line"><span class="prompt">➜</span><code> git clone https://github.com/username/repo-name.git</code></div>
            <div class="term-line"><span class="prompt">➜</span><code> cd repo-name && ls -la</code></div>
            <div style="margin-top:8px;background:linear-gradient(90deg, rgba(0,230,168,0.02), transparent);padding:10px;border-radius:8px;display:flex;justify-content:space-between;align-items:center">
              <div style="font-size:13px;color:var(--muted)">Current focus</div>
              <div style="font-family:var(--mono);font-size:13px">JavaScript • React • Node • Android • Java → DevOps: CI/CD, Pipelines, Docker, Kubernetes</div>
            </div>
            <div style="margin-top:10px" class="term-line"><span class="prompt">➜</span><code> # run a demo</code><span class="cursor" aria-hidden></span></div>
          </div>

          <h3 style="margin-top:18px">What you'll find</h3>
          <ul style="color:var(--muted);line-height:1.8;margin-top:8px">
            <li>Reusable JavaScript modules, component libraries and worked examples.</li>
            <li>Production-ish Android samples (Java + Kotlin friendly structure).</li>
            <li>Full-stack demos: small APIs, serverless notes, and test harnesses.</li>
            <li>Coming soon: opinionated CI/CD templates, pipeline-as-code, Dockerfiles and Kubernetes manifests.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:18px">
          <h3 style="margin:0">Highlighted Projects</h3>
          <div class="projects" style="margin-top:12px">
            <div class="project">
              <div class="proj-meta">
                <div class="proj-title">micro-ui-kit</div>
                <div class="proj-desc">Tiny, themeable UI components built in vanilla JS + CSS with accessibility in mind.</div>
              </div>
              <div style="font-family:var(--mono);font-size:13px;color:var(--muted)">/ui</div>
            </div>

            <div class="project">
              <div class="proj-meta">
                <div class="proj-title">android-helpers</div>
                <div class="proj-desc">Template Android modules and sample integrations (Java). Clean folder structure and CI-ready builds.</div>
              </div>
              <div style="font-family:var(--mono);font-size:13px;color:var(--muted)">/android</div>
            </div>

            <div class="project">
              <div class="proj-meta">
                <div class="proj-title">api-stub</div>
                <div class="proj-desc">Express + Node microservice examples with tests and mock providers for local dev.</div>
              </div>
              <div style="font-family:var(--mono);font-size:13px;color:var(--muted)">/services</div>
            </div>

          </div>

          <p style="color:var(--muted);margin-top:12px">Each project contains a clear README, a working demo or emulator, and a unit-test example where applicable.</p>
        </section>

        <section class="card" style="margin-top:18px">
          <h3 style="margin:0">Contribution & Roadmap</h3>
          <p style="color:var(--muted);margin-top:8px">Contributions are welcome. Pull requests should include tests, a short changelog, and a demo branch when relevant. The immediate roadmap prioritizes:</p>
          <ol style="color:var(--muted);margin-top:8px">
            <li>CI/CD examples for GitHub Actions and GitLab CI with Docker build steps.</li>
            <li>Pipeline templates for building, testing, and deploying microservices.</li>
            <li>Infrastructure snippets: Terraform + Kubernetes manifests for small apps.</li>
            <li>Automated release workflows and semantic versioning helpers.</li>
          </ol>
        </section>

      </main>

      <aside>
        <div class="card">
          <h3 style="margin:0">Tech Snapshot</h3>
          <div style="margin-top:12px" class="tech">
            <span class="pill">JavaScript</span>
            <span class="pill">React</span>
            <span class="pill">Node.js</span>
            <span class="pill">HTML</span>
            <span class="pill">CSS</span>
            <span class="pill">Android</span>
            <span class="pill">Java</span>
            <span class="pill">Docker</span>
            <span class="pill">Kubernetes</span>
            <span class="pill">GitHub Actions</span>
            <span class="pill">Terraform</span>
          </div>

          <div style="margin-top:14px">
            <h4 style="margin:0">CI/CD pipeline (preview)</h4>
            <div class="pipeline" aria-hidden>
              <div class="stage"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M3 12h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/></svg><h4>Build</h4></div>
              <div class="connector"><div class="pulse"></div></div>
              <div class="stage"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M12 5v14" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/></svg><h4>Test</h4></div>
              <div class="connector"><div class="pulse"></div></div>
              <div class="stage"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M4 12h16" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/></svg><h4>Deploy</h4></div>
            </div>
          </div>

          <div style="margin-top:16px">
            <h4 style="margin:0">Quick commands</h4>
            <pre style="margin-top:8px;background:rgba(255,255,255,0.02);padding:10px;border-radius:8px;color:var(--muted);font-family:var(--mono);font-size:13px"># run tests
npm ci
npm test

# build docker image
docker build -t vedansh/project-name:latest .

# demo pipeline
./scripts/ci/run-local.sh</pre>
          </div>

        </div>

        <div class="card" style="margin-top:14px">
          <h4 style="margin:0">Contact</h4>
          <div style="color:var(--muted);margin-top:8px;font-size:13px">GitHub: <a href="https://github.com/your-username" style="color:var(--accent);text-decoration:none">@your-username</a></div>
          <div style="color:var(--muted);margin-top:6px;font-size:13px">Email: <span style="color:var(--accent2)">hello@your-domain.com</span></div>
        </div>

      </aside>
    </div>

    <footer>
      <div style="opacity:0.9">Built with curiosity. Shipping small, reliable systems. Ready for DevOps & automation.</div>
    </footer>
  </div>

  <script>
    // small interactive flourish — copy repo button + animated timeline entry
    (function(){
      // add a copy command helper (no external access needed)
      const copyText = (t)=>navigator.clipboard?.writeText(t).catch(()=>{});

      // keyboard shortcut: press C to copy clone command when focus is on page
      window.addEventListener('keydown', (e)=>{
        if(e.key.toLowerCase()==='c' && (e.ctrlKey||e.metaKey)===false){
          copyText('git clone https://github.com/your-username/repo-name.git');
          const n = document.createElement('div');
          n.textContent = 'Clone command copied';
          n.style.position='fixed';n.style.left='50%';n.style.top='18px';n.style.transform='translateX(-50%)';n.style.padding='8px 12px';n.style.borderRadius='8px';n.style.background='linear-gradient(90deg, rgba(0,230,168,0.1), rgba(107,140,255,0.08))';n.style.color='#dfffea';n.style.zIndex=9999;document.body.appendChild(n);
          setTimeout(()=>n.remove(),1200);
        }
      });
    })();
  </script>
</body>
</html>

