---
hide:
  - navigation
  - toc
---

<style>
      :root {
        --ink: #26242b;
        --muted: #77737d;
        --line: #e9e4df;
        --paper: #fbfaf8;
        --warm: #f4efe9;
        --lilac: #e9dcff;
        --purple: #8357d8;
        --purple-deep: #5e35ad;
        --green: #dcebdc;
        --yellow: #f7e6ad;
        --blue: #dce9f4;
        --shadow: 0 22px 60px rgba(65, 42, 94, 0.09);
      }

      * { box-sizing: border-box; }
      html { scroll-behavior: smooth; }
      body {
        margin: 0;
        color: var(--ink);
        background: var(--paper);
        font-family: "Noto Sans SC", system-ui, sans-serif;
        line-height: 1.65;
      }
      a { color: inherit; text-decoration: none; }
      .wrap { width: min(1120px, calc(100% - 44px)); margin: 0 auto; }
      .mono { font-family: "DM Mono", monospace; letter-spacing: .02em; }
      .eyebrow { color: var(--purple-deep); font-size: 12px; font-weight: 700; letter-spacing: .12em; text-transform: uppercase; }

      header {
        position: sticky;
        top: 0;
        z-index: 10;
        background: rgba(251, 250, 248, .84);
        border-bottom: 1px solid rgba(233, 228, 223, .86);
        backdrop-filter: blur(14px);
      }
      .nav { height: 74px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
      .brand { display: inline-flex; align-items: center; gap: 10px; font-weight: 800; letter-spacing: -.02em; }
      .mark { width: 34px; height: 34px; display: grid; place-items: center; border-radius: 11px; background: var(--purple); color: white; box-shadow: 0 7px 18px rgba(131, 87, 216, .24); font-family: "DM Mono", monospace; font-size: 16px; }
      .brand small { display: block; color: var(--muted); font-size: 10px; font-weight: 500; letter-spacing: .1em; }
      .links { display: flex; align-items: center; gap: 26px; color: var(--muted); font-size: 13px; font-weight: 600; }
      .links a { transition: color .2s ease; }
      .links a:hover { color: var(--purple-deep); }
      .nav-cta { padding: 10px 16px; border-radius: 99px; background: var(--ink); color: white; font-size: 13px; font-weight: 700; transition: transform .2s, background .2s; }
      .nav-cta:hover { transform: translateY(-2px); background: var(--purple-deep); }

      .hero { padding: 78px 0 65px; position: relative; overflow: hidden; }
      .hero::before { content: ""; position: absolute; width: 560px; height: 560px; border-radius: 50%; background: radial-gradient(circle, rgba(233, 220, 255, .84), rgba(233, 220, 255, 0) 68%); top: -260px; right: -140px; pointer-events: none; }
      .hero-grid { display: grid; grid-template-columns: 1.06fr .94fr; gap: 68px; align-items: center; position: relative; }
      h1 { max-width: 650px; margin: 18px 0 20px; font-size: clamp(44px, 6.2vw, 78px); line-height: 1.12; letter-spacing: -.06em; font-weight: 800; }
      h1 em { color: var(--purple-deep); font-style: normal; }
      .lead { max-width: 550px; color: var(--muted); font-size: 17px; line-height: 1.85; }
      .hero-actions { display: flex; align-items: center; gap: 13px; flex-wrap: wrap; margin-top: 30px; }
      .button { display: inline-flex; align-items: center; justify-content: center; gap: 9px; padding: 13px 19px; border-radius: 12px; border: 1px solid var(--ink); font-size: 13px; font-weight: 700; transition: transform .2s, box-shadow .2s, background .2s; }
      .button:hover { transform: translateY(-3px); box-shadow: 0 10px 22px rgba(38, 36, 43, .12); }
      .button.primary { background: var(--ink); color: white; }
      .button.ghost { border-color: var(--line); background: white; }
      .button.ghost:hover { border-color: var(--purple); color: var(--purple-deep); }
      .hero-note { margin-top: 22px; color: var(--muted); font-size: 12px; }
      .hero-note span { color: var(--purple-deep); font-weight: 700; }

      .hero-card { position: relative; padding: 27px; border: 1px solid var(--line); border-radius: 28px; background: rgba(255,255,255,.79); box-shadow: var(--shadow); transform: rotate(1.2deg); }
      .hero-card::after { content: "✦"; position: absolute; right: 22px; top: -26px; color: var(--purple); font-size: 30px; }
      .card-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 25px; }
      .avatar { width: 62px; height: 62px; display: grid; place-items: center; border-radius: 19px; background: linear-gradient(135deg, #f0d7fb, #8c62d9); color: white; font-size: 27px; font-weight: 800; box-shadow: inset 0 -9px 20px rgba(79, 31, 138, .2); }
      .status { padding: 6px 10px; border-radius: 99px; background: var(--green); color: #3b7048; font-size: 11px; font-weight: 700; }
      .hero-card h3 { margin: 0 0 5px; font-size: 22px; letter-spacing: -.04em; }
      .hero-card p { margin: 0; color: var(--muted); font-size: 13px; }
      .progress { padding: 18px; border-radius: 17px; background: var(--warm); }
      .progress-head { display: flex; justify-content: space-between; margin-bottom: 13px; font-size: 12px; font-weight: 700; }
      .progress-head span { color: var(--purple-deep); }
      .bar { height: 8px; overflow: hidden; border-radius: 99px; background: #e0d9d1; }
      .bar i { display: block; width: 38%; height: 100%; border-radius: inherit; background: var(--purple); }
      .mini-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 9px; margin-top: 15px; }
      .mini { padding: 14px 10px; border-radius: 15px; text-align: center; background: white; border: 1px solid var(--line); }
      .mini strong { display: block; font-size: 20px; letter-spacing: -.04em; }
      .mini span { color: var(--muted); font-size: 10px; }

      .ticker { padding: 16px 0; border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); color: var(--muted); font-size: 12px; }
      .ticker-inner { display: flex; gap: 30px; align-items: center; flex-wrap: wrap; }
      .ticker strong { color: var(--ink); }
      .dot { width: 5px; height: 5px; background: var(--purple); border-radius: 50%; }

      section { padding: 100px 0; }
      .section-head { display: flex; justify-content: space-between; align-items: end; gap: 30px; margin-bottom: 33px; }
      h2 { margin: 8px 0 0; font-size: clamp(28px, 4vw, 42px); line-height: 1.2; letter-spacing: -.055em; }
      .section-intro { max-width: 365px; margin: 0; color: var(--muted); font-size: 14px; }

      .path-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
      .path-card { min-height: 250px; padding: 25px; display: flex; flex-direction: column; justify-content: space-between; border: 1px solid var(--line); border-radius: 22px; background: white; transition: transform .2s, box-shadow .2s; }
      .path-card:hover { transform: translateY(-5px); box-shadow: var(--shadow); }
      .path-card:nth-child(2) { background: var(--lilac); border-color: transparent; }
      .path-card:nth-child(3) { background: var(--green); border-color: transparent; }
      .path-icon { width: 39px; height: 39px; display: grid; place-items: center; border-radius: 12px; background: rgba(255,255,255,.65); font-size: 18px; }
      .path-card h3 { margin: 27px 0 7px; font-size: 20px; letter-spacing: -.04em; }
      .path-card p { color: var(--muted); margin: 0; font-size: 13px; line-height: 1.7; }
      .path-foot { display: flex; justify-content: space-between; align-items: center; margin-top: 25px; color: var(--muted); font-size: 11px; }
      .path-foot a { color: var(--purple-deep); font-weight: 700; }

      .resource-section { background: var(--warm); }
      .filters { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 25px; }
      .filter { padding: 8px 13px; border: 1px solid #ded5cd; border-radius: 99px; background: rgba(255,255,255,.58); color: var(--muted); cursor: pointer; font: inherit; font-size: 12px; }
      .filter.active, .filter:hover { border-color: var(--purple); background: var(--purple); color: white; }
      .resource-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
      .resource { padding: 21px; border: 1px solid rgba(222, 213, 205, .84); border-radius: 18px; background: rgba(255,255,255,.77); transition: transform .2s; }
      .resource:hover { transform: translateY(-4px); }
      .resource.hidden { display: none; }
      .resource-label { display: inline-block; padding: 5px 8px; border-radius: 6px; background: var(--blue); color: #486a86; font-size: 10px; font-weight: 700; }
      .resource:nth-child(2) .resource-label { background: var(--yellow); color: #876b1b; }
      .resource:nth-child(3) .resource-label { background: var(--lilac); color: var(--purple-deep); }
      .resource h3 { margin: 17px 0 7px; font-size: 17px; letter-spacing: -.035em; }
      .resource p { min-height: 46px; margin: 0; color: var(--muted); font-size: 12px; line-height: 1.7; }
      .resource-foot { display: flex; justify-content: space-between; align-items: center; margin-top: 22px; padding-top: 13px; border-top: 1px solid var(--line); color: var(--muted); font-size: 11px; }
      .resource-foot a { color: var(--purple-deep); font-weight: 700; }

      .project-grid { display: grid; grid-template-columns: 1.15fr .85fr; gap: 14px; }
      .project { min-height: 220px; padding: 28px; border: 1px solid var(--line); border-radius: 22px; background: white; }
      .project.featured { background: var(--ink); color: white; border-color: var(--ink); }
      .project.featured p, .project.featured .project-meta { color: #b6b2bc; }
      .project h3 { margin: 25px 0 7px; font-size: 24px; letter-spacing: -.05em; }
      .project p { max-width: 450px; margin: 0; color: var(--muted); font-size: 13px; line-height: 1.8; }
      .project-meta { display: flex; gap: 8px; color: var(--muted); font-size: 11px; }
      .project-meta span { padding: 4px 8px; border: 1px solid currentColor; border-radius: 99px; }
      .project-link { display: inline-flex; margin-top: 25px; color: var(--purple); font-size: 12px; font-weight: 700; }

      .log-section { border-top: 1px solid var(--line); }
      .log-list { border-top: 1px solid var(--line); }
      .log { display: grid; grid-template-columns: 130px 1fr auto; gap: 20px; align-items: center; padding: 19px 0; border-bottom: 1px solid var(--line); }
      .log time { color: var(--muted); font: 12px "DM Mono", monospace; }
      .log h3 { margin: 0; font-size: 15px; letter-spacing: -.025em; }
      .log p { margin: 3px 0 0; color: var(--muted); font-size: 12px; }
      .log > a { color: var(--purple-deep); font-size: 12px; font-weight: 700; }

      footer { padding: 35px 0 45px; border-top: 1px solid var(--line); }
      .footer-row { display: flex; justify-content: space-between; align-items: center; gap: 20px; }
      .footer-row p { margin: 0; color: var(--muted); font-size: 12px; }
      .socials { display: flex; gap: 18px; color: var(--muted); font-size: 12px; font-weight: 700; }
      .socials a:hover { color: var(--purple-deep); }

      .reveal { opacity: 0; transform: translateY(18px); transition: opacity .65s ease, transform .65s ease; }
      .reveal.show { opacity: 1; transform: none; }
      @media (max-width: 800px) {
        .wrap { width: min(100% - 30px, 620px); }
        .links { display: none; }
        .hero { padding-top: 53px; }
        .hero-grid, .project-grid { grid-template-columns: 1fr; gap: 40px; }
        .hero-card { max-width: 520px; margin: 0 auto; }
        section { padding: 70px 0; }
        .section-head { display: block; }
        .section-intro { margin-top: 16px; }
        .path-grid, .resource-grid { grid-template-columns: 1fr; }
        .path-card { min-height: 210px; }
        .log { grid-template-columns: 1fr auto; gap: 7px 15px; }
        .log time { grid-column: 1 / -1; }
        .log > a { grid-column: 2; grid-row: 2 / span 2; }
        .footer-row { align-items: flex-start; flex-direction: column; }
      }
    
/* MkDocs shell overrides: this page is the homepage, not a docs article. */
.md-header, .md-sidebar, .md-footer, .md-tabs, .md-search { display: none !important; }
.md-main { background: var(--paper); }
.md-main__inner { margin: 0 !important; }
.md-content { max-width: none !important; }
.md-content__inner { margin: 0 !important; padding: 0 !important; }
</style>

    <header>
      <div class="wrap nav">
        <a class="brand" href="#top" aria-label="回到首页"><span class="mark">LQ</span><span>LQGbw<small>AI · LEARN · BUILD</small></span></a>
        <nav class="links" aria-label="主导航">
          <a href="#path">学习路线</a><a href="#resources">资源库</a><a href="#projects">项目</a><a href="#log">成长记录</a>
        </nav>
        <a class="nav-cta" href="#resources">探索资源 ↗</a>
      </div>
    </header>

    <main id="top">
      <section class="hero">
        <div class="wrap hero-grid">
          <div class="reveal">
            <div class="eyebrow mono">PERSONAL LAB / 001</div>
            <h1>边学边做，<br /><em>把 AI 变成</em>真实能力。</h1>
            <p class="lead">我是 LQGbw，正在记录从了解 AI 工具，到做出真正有用的小项目的过程。这里有学习路线、实践项目、可复用资源，也有一路上的真实思考。</p>
            <div class="hero-actions"><a class="button primary" href="#path">查看学习路线 <span>↓</span></a><a class="button ghost" href="#projects">看我的项目 ↗</a></div>
            <p class="hero-note"><span>现在进行中：</span>搭建我的第一套 AI 工作流 · 每周更新</p>
          </div>
          <div class="hero-card reveal">
            <div class="card-top"><div class="avatar">✦</div><span class="status">● 持续更新中</span></div>
            <h3>我的 AI 成长地图</h3>
            <p>从会用工具，到能做出作品。</p>
            <div class="progress" style="margin-top: 23px"><div class="progress-head"><span>当前学习进度</span><span>38%</span></div><div class="bar"><i></i></div></div>
            <div class="mini-grid"><div class="mini"><strong>03</strong><span>学习路线</span></div><div class="mini"><strong>08</strong><span>实践项目</span></div><div class="mini"><strong>21</strong><span>资源整理</span></div></div>
          </div>
        </div>
      </section>

      <div class="ticker"><div class="wrap ticker-inner"><strong class="mono">THIS WEEK</strong><span class="dot"></span><span>整理 AI 工具入门路线</span><span class="dot"></span><span>发布第一个可复用 Skill</span><span class="dot"></span><span>记录一次真实实践</span></div></div>

      <section id="path"><div class="wrap"><div class="section-head reveal"><div><div class="eyebrow mono">01 / LEARNING PATH</div><h2>从好奇开始，<br />做出自己的路线。</h2></div><p class="section-intro">不追求一次学完所有东西。每条路线都对应一个真实目标，用作品检验学习。</p></div>
        <div class="path-grid"><article class="path-card reveal"><div><div class="path-icon">◎</div><h3>AI 工具入门</h3><p>认识主流 AI 工具，找到适合自己的工作方式，完成第一个可复用工作流。</p></div><div class="path-foot"><span>4 个章节 · 入门</span><a href="#resources">开始学习 →</a></div></article><article class="path-card reveal"><div><div class="path-icon">⌁</div><h3>Prompt 与工作流</h3><p>从“问得更好”到“做成流程”，把零散的提示词变成稳定的生产力。</p></div><div class="path-foot"><span>6 个章节 · 实践</span><a href="#resources">开始学习 →</a></div></article><article class="path-card reveal"><div><div class="path-icon">✳</div><h3>Skill / 自动化</h3><p>学习如何封装自己的方法，让 AI 在重复任务中真正帮你省时间。</p></div><div class="path-foot"><span>进行中 · 持续更新</span><a href="#resources">查看进度 →</a></div></article></div>
      </div></section>

      <section class="resource-section" id="resources"><div class="wrap"><div class="section-head reveal"><div><div class="eyebrow mono">02 / RESOURCE LIBRARY</div><h2>拿来就用的<br />AI 资源库。</h2></div><p class="section-intro">把我用过、做过、验证过的东西留下来。每份资源都附有使用场景和实践说明。</p></div>
        <div class="filters reveal" role="tablist" aria-label="资源筛选"><button class="filter active" data-filter="all">全部</button><button class="filter" data-filter="skill">Skill</button><button class="filter" data-filter="prompt">Prompt</button><button class="filter" data-filter="tool">工具</button></div>
        <div class="resource-grid"><article class="resource reveal" data-type="skill"><span class="resource-label">SKILL</span><h3>AI 周报整理助手</h3><p>把一周的碎片信息整理成清晰的周报结构，适合个人复盘和团队同步。</p><div class="resource-foot"><span>v0.1 · 刚刚更新</span><a href="#">查看 GitHub ↗</a></div></article><article class="resource reveal" data-type="prompt"><span class="resource-label">PROMPT</span><h3>工具测评提示词模板</h3><p>从功能、体验、适用人群和真实场景四个角度，快速写出一篇有用的工具测评。</p><div class="resource-foot"><span>可复制 · 免费</span><a href="#">查看模板 ↗</a></div></article><article class="resource reveal" data-type="tool"><span class="resource-label">TOOLKIT</span><h3>AI 工具选择清单</h3><p>按写作、研究、设计、自动化和开发分类，记录我实际用过的工具。</p><div class="resource-foot"><span>21 个工具 · 持续补充</span><a href="#">打开清单 ↗</a></div></article></div>
      </div></section>

      <section id="projects"><div class="wrap"><div class="section-head reveal"><div><div class="eyebrow mono">03 / BUILD IN PUBLIC</div><h2>学习的结果，<br />应该留下作品。</h2></div><p class="section-intro">这里记录正在做的实验，不追求完美发布，只追求每一次都比上一次更进一步。</p></div>
        <div class="project-grid"><article class="project featured reveal"><div class="project-meta"><span>进行中</span><span>AI WORKFLOW</span></div><h3>我的第一个 AI 工具实验室</h3><p>一个用来记录 AI 工具、工作流和个人实践的空间。它会慢慢变成我的公开学习档案。</p><a class="project-link" href="#">查看项目详情 ↗</a></article><article class="project reveal"><div class="project-meta"><span>计划中</span></div><h3>小红书内容工作流</h3><p>探索如何用 AI 辅助选题、研究、写作和复盘，同时保留自己的判断和表达。</p><a class="project-link" href="#">关注更新 ↗</a></article></div>
      </div></section>

      <section class="log-section" id="log"><div class="wrap"><div class="section-head reveal"><div><div class="eyebrow mono">04 / FIELD NOTES</div><h2>成长不是口号，<br />是留下记录。</h2></div><p class="section-intro">一些正在发生的小事。以后回头看，这就是我走过的路。</p></div>
        <div class="log-list"><article class="log reveal"><time>2026.08.21</time><div><h3>开始搭建自己的 AI 主页</h3><p>先把学习路线、资源库和项目展示放在一起。</p></div><a href="#">阅读 →</a></article><article class="log reveal"><time>2026.08.18</time><div><h3>为什么想做一个成长型 AI 博主</h3><p>不是假装专家，而是把真实的学习过程分享出来。</p></div><a href="#">阅读 →</a></article><article class="log reveal"><time>2026.08.12</time><div><h3>我开始整理自己的工具箱</h3><p>工具很多，但真正留下来的应该是方法。</p></div><a href="#">阅读 →</a></article></div>
      </div></section>
    </main>

    <footer><div class="wrap footer-row"><p>© 2026 LQGbw · 边学边做 AI</p><div class="socials"><a href="https://github.com/LQGbw" target="_blank" rel="noreferrer">GitHub ↗</a><a href="#">小红书 ↗</a><a href="https://github.com/LQGbw" target="_blank" rel="noreferrer">联系我 ↗</a></div></div></footer>
    <script>
      const revealObserver = new IntersectionObserver((entries) => entries.forEach((entry) => { if (entry.isIntersecting) entry.target.classList.add('show'); }), { threshold: .12 });
      document.querySelectorAll('.reveal').forEach((el) => revealObserver.observe(el));
      document.querySelectorAll('.filter').forEach((button) => button.addEventListener('click', () => {
        document.querySelectorAll('.filter').forEach((item) => item.classList.remove('active'));
        button.classList.add('active');
        const type = button.dataset.filter;
        document.querySelectorAll('.resource').forEach((card) => card.classList.toggle('hidden', type !== 'all' && card.dataset.type !== type));
      }));
    </script>
  
