<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mahesh Raghava - Full Stack Developer & AI Enthusiast</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=Space+Mono:wght@400;700&display=swap');

        *{margin:0;padding:0;box-sizing:border-box}
        :root{
          --c0:#0a0a0f;--c1:#0f0f1a;--c2:#1a1a2e;
          --cyan:#00e5ff;--cyan2:#00b8d4;--cyan3:#0097a7;
          --blue:#2979ff;--blue2:#1565c0;
          --glow:0 0 20px rgba(0,229,255,0.3);
          --glow2:0 0 40px rgba(0,229,255,0.15);
          --border:rgba(0,229,255,0.15);
          --border2:rgba(0,229,255,0.3);
        }

        body{
          background:var(--c0);color:#e0e0e0;
          font-family:'Space Mono',monospace;
          overflow-x:hidden;
          line-height:1.7;
        }

        .container{max-width:900px;margin:0 auto;padding:0 24px}

        /* ---- HERO ---- */
        .hero{
          position:relative;
          padding:80px 0 60px;
          text-align:center;
          overflow:hidden;
        }
        .hero::before{
          content:'';
          position:absolute;inset:0;
          background:radial-gradient(ellipse 70% 50% at 50% 0%, rgba(0,229,255,0.08) 0%, transparent 70%);
          pointer-events:none;
        }
        .grid-bg{
          position:absolute;inset:0;
          background-image:
            linear-gradient(rgba(0,229,255,0.04) 1px, transparent 1px),
            linear-gradient(90deg, rgba(0,229,255,0.04) 1px, transparent 1px);
          background-size:40px 40px;
          pointer-events:none;
        }
        .hero-tag{
          display:inline-block;
          font-size:11px;letter-spacing:3px;text-transform:uppercase;
          color:var(--cyan);border:1px solid var(--border2);
          padding:6px 16px;border-radius:2px;
          margin-bottom:24px;
          animation:fadeUp .6s ease both;
        }
        .hero h1{
          font-family:'Syne',sans-serif;
          font-size:clamp(2.4rem,6vw,4rem);
          font-weight:800;letter-spacing:-1px;
          line-height:1.05;
          color:#fff;
          animation:fadeUp .6s .1s ease both;
        }
        .hero h1 span{
          background:linear-gradient(90deg,var(--cyan),var(--blue));
          -webkit-background-clip:text;-webkit-text-fill-color:transparent;
        }
        .hero-sub{
          font-size:13px;letter-spacing:2px;text-transform:uppercase;
          color:rgba(255,255,255,0.4);margin-top:12px;
          animation:fadeUp .6s .2s ease both;
        }
        .hero-links{
          display:flex;gap:12px;justify-content:center;margin-top:32px;
          animation:fadeUp .6s .3s ease both;flex-wrap:wrap;
        }
        .link-pill{
          display:inline-flex;align-items:center;gap:8px;
          font-family:'Space Mono',monospace;font-size:12px;
          color:var(--cyan);border:1px solid var(--border2);
          padding:8px 18px;border-radius:2px;text-decoration:none;
          transition:all .2s;background:rgba(0,229,255,0.04);
        }
        .link-pill:hover{background:rgba(0,229,255,0.1);box-shadow:var(--glow);color:#fff}
        .link-pill .dot{width:6px;height:6px;border-radius:50%;background:var(--cyan);display:inline-block}

        /* ---- DIVIDER ---- */
        .divider{
          display:flex;align-items:center;gap:16px;
          margin:48px 0 32px;
        }
        .divider-line{flex:1;height:1px;background:var(--border)}
        .divider-label{
          font-size:10px;letter-spacing:3px;text-transform:uppercase;
          color:var(--cyan);white-space:nowrap;
        }

        /* ---- ABOUT ---- */
        .about-grid{
          display:grid;grid-template-columns:1fr 1fr;gap:2px;
          border:1px solid var(--border);
        }
        .about-cell{
          padding:16px 20px;border:1px solid var(--border);
          font-size:13px;color:rgba(255,255,255,0.65);
          position:relative;
          transition:background .2s;
        }
        .about-cell:hover{background:rgba(0,229,255,0.04)}
        .about-cell .prefix{color:var(--cyan);margin-right:8px}
        .about-cell strong{color:#fff;font-weight:700}

        /* ---- TECH ARSENAL ---- */
        .section{padding:0 0 48px}

        .tech-group{margin-bottom:28px}
        .tech-group-label{
          font-size:10px;letter-spacing:3px;text-transform:uppercase;
          color:rgba(255,255,255,0.3);margin-bottom:12px;
        }
        .tech-row{display:flex;flex-wrap:wrap;gap:8px}
        .tech-badge{
          font-family:'Space Mono',monospace;
          font-size:11px;letter-spacing:1px;
          color:rgba(255,255,255,0.7);
          border:1px solid var(--border);
          padding:6px 14px;border-radius:1px;
          background:var(--c1);
          transition:all .2s;cursor:default;
          position:relative;overflow:hidden;
        }
        .tech-badge::before{
          content:'';position:absolute;top:0;left:-100%;
          width:100%;height:100%;
          background:linear-gradient(90deg,transparent,rgba(0,229,255,0.08),transparent);
          transition:left .4s;
        }
        .tech-badge:hover::before{left:100%}
        .tech-badge:hover{border-color:var(--cyan);color:var(--cyan);background:rgba(0,229,255,0.05)}

        /* ---- PROJECTS ---- */
        .projects-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
        .project-card{
          border:1px solid var(--border);background:var(--c1);
          padding:24px;position:relative;overflow:hidden;
          transition:all .25s;
        }
        .project-card::after{
          content:'';position:absolute;top:0;left:0;right:0;
          height:2px;
          background:linear-gradient(90deg,var(--cyan),var(--blue));
          transform:scaleX(0);transform-origin:left;
          transition:transform .3s;
        }
        .project-card:hover{border-color:var(--border2);background:rgba(0,229,255,0.03)}
        .project-card:hover::after{transform:scaleX(1)}
        .project-num{
          font-size:10px;letter-spacing:2px;text-transform:uppercase;
          color:rgba(255,255,255,0.2);margin-bottom:12px;
        }
        .project-title{
          font-family:'Syne',sans-serif;font-size:1.2rem;font-weight:800;
          color:#fff;margin-bottom:8px;
        }
        .project-desc{font-size:12px;color:rgba(255,255,255,0.5);line-height:1.7;margin-bottom:16px}
        .project-tags{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:16px}
        .project-tag{
          font-size:10px;letter-spacing:1px;
          color:var(--cyan3);border:1px solid rgba(0,151,167,0.3);
          padding:3px 10px;border-radius:1px;
        }
        .project-link{
          font-size:11px;letter-spacing:2px;text-transform:uppercase;
          color:var(--cyan);text-decoration:none;
          display:inline-flex;align-items:center;gap:6px;
          transition:gap .2s;
        }
        .project-link:hover{gap:10px}
        .project-link::after{content:'→'}

        /* ---- SKILLS ---- */
        .skills-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
        .skill-block{
          border:1px solid var(--border);
          padding:20px;background:var(--c1);
        }
        .skill-block-title{
          font-family:'Syne',sans-serif;font-size:.85rem;font-weight:700;
          color:var(--cyan);margin-bottom:12px;letter-spacing:1px;
          text-transform:uppercase;
        }
        .skill-item{
          font-size:12px;color:rgba(255,255,255,0.55);
          padding:5px 0;border-bottom:1px solid rgba(255,255,255,0.04);
          display:flex;align-items:center;gap:8px;
        }
        .skill-item:last-child{border-bottom:none}
        .skill-item::before{content:'▸';color:var(--cyan);font-size:10px;flex-shrink:0}

        /* ---- BUILDING ---- */
        .building-list{display:grid;grid-template-columns:1fr 1fr;gap:2px}
        .building-item{
          border:1px solid var(--border);padding:18px 20px;
          background:var(--c1);transition:background .2s;
        }
        .building-item:hover{background:rgba(0,229,255,0.04)}
        .building-item-title{
          font-family:'Syne',sans-serif;font-size:.85rem;font-weight:700;
          color:#fff;margin-bottom:6px;
        }
        .building-item-desc{font-size:12px;color:rgba(255,255,255,0.45);line-height:1.6}

        /* ---- CONTACT ---- */
        .contact-box{
          border:1px solid var(--border2);
          padding:40px;text-align:center;
          background:var(--c1);
          position:relative;overflow:hidden;
        }
        .contact-box::before{
          content:'';position:absolute;inset:0;
          background:radial-gradient(ellipse 60% 40% at 50% 100%, rgba(0,229,255,0.06) 0%, transparent 70%);
        }
        .contact-box h3{
          font-family:'Syne',sans-serif;font-size:1.6rem;font-weight:800;
          color:#fff;margin-bottom:8px;position:relative;
        }
        .contact-box p{font-size:13px;color:rgba(255,255,255,0.45);margin-bottom:28px;position:relative}
        .contact-links{
          display:flex;gap:12px;justify-content:center;flex-wrap:wrap;position:relative;
        }
        .contact-link{
          font-family:'Space Mono',monospace;font-size:12px;
          color:rgba(255,255,255,0.6);text-decoration:none;
          border:1px solid var(--border);padding:10px 20px;
          transition:all .2s;background:var(--c2);
        }
        .contact-link:hover{color:var(--cyan);border-color:var(--border2);box-shadow:var(--glow)}

        /* ---- FOOTER ---- */
        .footer{
          border-top:1px solid var(--border);
          padding:24px;text-align:center;
          font-size:11px;letter-spacing:2px;text-transform:uppercase;
          color:rgba(255,255,255,0.2);margin-top:48px;
        }
        .footer span{color:var(--cyan)}

        /* ---- ANIMATIONS ---- */
        @keyframes fadeUp{
          from{opacity:0;transform:translateY(20px)}
          to{opacity:1;transform:translateY(0)}
        }
        .reveal{opacity:0;transform:translateY(16px);transition:opacity .5s, transform .5s}
        .reveal.in{opacity:1;transform:translateY(0)}

        @media(max-width:600px){
          .about-grid,.projects-grid,.skills-grid,.building-list{grid-template-columns:1fr}
          .hero h1{font-size:2rem}
        }
    </style>
</head>
<body>

<div class="hero">
  <div class="grid-bg"></div>
  <div class="container">
    <div class="hero-tag">Full Stack Developer · AI Enthusiast</div>
    <h1>K <span>Mahesh</span><br>Raghava</h1>
    <p class="hero-sub">Building scalable · Thinking intelligently · Shipping fast</p>
    <div class="hero-links">
      <a href="mailto:maheshraghavak@gmail.com" class="link-pill"><span class="dot"></span>maheshraghavak@gmail.com</a>
      <a href="https://in.linkedin.com/in/mahesh-raghava-361a51305" class="link-pill"><span class="dot"></span>LinkedIn</a>
      <a href="https://github.com/MaheshRaghava" class="link-pill"><span class="dot"></span>GitHub</a>
    </div>
  </div>
</div>

<div class="container">

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// about</div><div class="divider-line"></div></div>

  <div class="about-grid reveal">
    <div class="about-cell"><span class="prefix">01</span>Currently building <strong>AI-powered web platforms</strong> with Firebase &amp; Cloud</div>
    <div class="about-cell"><span class="prefix">02</span>Learning <strong>Advanced ML/AI</strong>, scalable architecture, LLM integration</div>
    <div class="about-cell"><span class="prefix">03</span>Expertise in <strong>C · Java · Python · Full-Stack</strong> development</div>
    <div class="about-cell"><span class="prefix">04</span>Passionate about <strong>turning ideas</strong> into innovative, scalable solutions</div>
    <div class="about-cell"><span class="prefix">05</span>Ask me about <strong>Node.js · Firebase · MongoDB · Gemini APIs</strong></div>
    <div class="about-cell"><span class="prefix">06</span>I build <strong>clones of popular apps</strong> to master architectural patterns</div>
  </div>

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// tech arsenal</div><div class="divider-line"></div></div>

  <div class="section reveal">
    <div class="tech-group">
      <div class="tech-group-label">Languages &amp; Fundamentals</div>
      <div class="tech-row">
        <span class="tech-badge">C</span>
        <span class="tech-badge">Java</span>
        <span class="tech-badge">Python</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Web Technologies</div>
      <div class="tech-row">
        <span class="tech-badge">HTML</span>
        <span class="tech-badge">CSS</span>
        <span class="tech-badge">JavaScript</span>
        <span class="tech-badge">Node.js</span>
        <span class="tech-badge">Express.js</span>
        <span class="tech-badge">React.js</span>
        <span class="tech-badge">Socket.io</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Databases &amp; Backend Services</div>
      <div class="tech-row">
        <span class="tech-badge">MongoDB</span>
        <span class="tech-badge">Firebase</span>
        <span class="tech-badge">Google Cloud</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Tools &amp; Platforms</div>
      <div class="tech-row">
        <span class="tech-badge">Git</span>
        <span class="tech-badge">VS Code</span>
        <span class="tech-badge">npm</span>
        <span class="tech-badge">Postman</span>
        <span class="tech-badge">Bash</span>
        <span class="tech-badge">Docker</span>
      </div>
    </div>
  </div>

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// featured projects</div><div class="divider-line"></div></div>

  <div class="projects-grid section reveal">
    <div class="project-card">
      <div class="project-num">Project 01</div>
      <div class="project-title">CodeSenseiAI</div>
      <p class="project-desc">GitHub App that analyzes PRs for security vulnerabilities, bugs, and code quality issues using Google Gemini 2.5 Flash. AI-Powered Code Review Bot.</p>
      <div class="project-tags">
        <span class="project-tag">JavaScript</span>
        <span class="project-tag">Google Gemini</span>
        <span class="project-tag">GitHub API</span>
        <span class="project-tag">Express.js</span>
        <span class="project-tag">Node.js</span>
      </div>
      <a href="https://codesenseiai-gold.vercel.app/" class="project-link">Live Demo</a>
    </div>
    <div class="project-card">
      <div class="project-num">Project 02</div>
      <div class="project-title">CodeRoom</div>
      <p class="project-desc">Multi-user real-time collaborative editor with Monaco, live cursors, integrated chat, and sandboxed code execution environment.</p>
      <div class="project-tags">
        <span class="project-tag">Node.js</span>
        <span class="project-tag">Socket.io</span>
        <span class="project-tag">React</span>
        <span class="project-tag">MongoDB</span>
      </div>
      <a href="https://coderoom-client.onrender.com" class="project-link">Live Demo</a>
    </div>
  </div>

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// skills &amp; expertise</div><div class="divider-line"></div></div>

  <div class="skills-grid section reveal">
    <div class="skill-block">
      <div class="skill-block-title">Backend &amp; API</div>
      <div class="skill-item">RESTful API Design &amp; GraphQL</div>
      <div class="skill-item">Authentication &amp; Authorization (JWT, OAuth)</div>
      <div class="skill-item">Database Design &amp; Optimization</div>
      <div class="skill-item">Scalable Architecture Patterns</div>
    </div>
    <div class="skill-block">
      <div class="skill-block-title">AI &amp; Machine Learning</div>
      <div class="skill-item">LLM Integration &amp; Prompt Engineering</div>
      <div class="skill-item">Google Gemini API</div>
      <div class="skill-item">Data Processing &amp; Analysis</div>
      <div class="skill-item">ML Model Integration</div>
    </div>
    <div class="skill-block">
      <div class="skill-block-title">Frontend Technologies</div>
      <div class="skill-item">React.js &amp; Modern JavaScript</div>
      <div class="skill-item">Responsive UI/UX Design</div>
      <div class="skill-item">State Management</div>
      <div class="skill-item">Performance Optimization</div>
    </div>
    <div class="skill-block">
      <div class="skill-block-title">DevOps &amp; Deployment</div>
      <div class="skill-item">Docker &amp; Containerization</div>
      <div class="skill-item">Cloud Deployment (Firebase, GCP)</div>
      <div class="skill-item">CI/CD Pipelines</div>
      <div class="skill-item">Server Configuration</div>
    </div>
  </div>

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// what i'm building</div><div class="divider-line"></div></div>

  <div class="building-list section reveal">
    <div class="building-item">
      <div class="building-item-title">Firebase + AI Integration</div>
      <div class="building-item-desc">Scalable backends with intelligent features powered by the latest LLM APIs</div>
    </div>
    <div class="building-item">
      <div class="building-item-title">AI-Driven Tools</div>
      <div class="building-item-desc">Automating development workflows with LLMs to supercharge productivity</div>
    </div>
    <div class="building-item">
      <div class="building-item-title">Real-Time Applications</div>
      <div class="building-item-desc">WebSocket-based collaborative platforms for seamless multi-user experiences</div>
    </div>
    <div class="building-item">
      <div class="building-item-title">Full-Stack Solutions</div>
      <div class="building-item-desc">End-to-end user experiences from database to polished UI</div>
    </div>
  </div>

  <div class="divider reveal"><div class="divider-line"></div><div class="divider-label">// let's collaborate</div><div class="divider-line"></div></div>

  <div class="contact-box reveal">
    <h3>Get In Touch</h3>
    <p>Always excited to collaborate on innovative projects, discuss AI/ML applications,<br>share knowledge, and build something amazing together.</p>
    <div class="contact-links">
      <a href="mailto:maheshraghavak@gmail.com" class="contact-link">maheshraghavak@gmail.com</a>
      <a href="https://in.linkedin.com/in/mahesh-raghava-361a51305" class="contact-link">@mahesh-raghava</a>
      <a href="https://github.com/MaheshRaghava" class="contact-link">@MaheshRaghava</a>
    </div>
  </div>

</div>

<div class="footer">
  <span>K Mahesh Raghava</span> · Full Stack Developer · AI Enthusiast · Last Updated 2026
</div>

<script>
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if(e.isIntersecting){e.target.classList.add('in');observer.unobserve(e.target)}
  });
},{threshold:.1});
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>

</body>
</html>
