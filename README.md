# ramirivict398-bot.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Slyvia · AI IG 内容运营系统</title>
  <meta name="description" content="把品牌卖点转成用户语言，把 IG 内容做成渠道节奏，把项目经验沉淀成可复用系统。" />
  <style>
    :root {
      --bg: #0d0d0e;
      --bg-2: #121214;
      --panel: rgba(255,255,255,0.06);
      --panel-2: rgba(255,255,255,0.04);
      --line: rgba(255,255,255,0.12);
      --text: #f6f2ea;
      --muted: rgba(246,242,234,0.72);
      --muted-2: rgba(246,242,234,0.5);
      --gold: #d8b164;
      --gold-soft: rgba(216,177,100,0.16);
      --shadow: 0 28px 80px rgba(0,0,0,0.42);
      --max: 1240px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at 0% 0%, rgba(216,177,100,0.12), transparent 24%),
        radial-gradient(circle at 100% 12%, rgba(216,177,100,0.10), transparent 22%),
        linear-gradient(180deg, #101012 0%, #0b0b0c 45%, #090909 100%);
      line-height: 1.6;
      overflow-x: hidden;
    }

    a { color: inherit; text-decoration: none; }
    button { font: inherit; }

    .container {
      width: min(var(--max), calc(100% - 32px));
      margin: 0 auto;
    }

    .nav {
      position: sticky;
      top: 0;
      z-index: 40;
      border-bottom: 1px solid rgba(255,255,255,0.08);
      background: rgba(10,10,10,0.6);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
    }

    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
      padding: 16px 0;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .brand-mark {
      width: 40px;
      height: 40px;
      border-radius: 12px;
      display: grid;
      place-items: center;
      color: var(--gold);
      background: linear-gradient(135deg, rgba(216,177,100,0.24), rgba(255,255,255,0.08));
      border: 1px solid rgba(255,255,255,0.1);
      box-shadow: var(--shadow);
      font-weight: 800;
      letter-spacing: -0.02em;
    }

    .brand-copy strong {
      display: block;
      font-size: 14px;
      letter-spacing: 0.01em;
    }

    .brand-copy span {
      display: block;
      margin-top: 2px;
      font-size: 12px;
      color: var(--muted-2);
    }

    .nav-links {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .nav-links a {
      font-size: 13px;
      color: var(--muted);
      transition: color .2s ease;
    }

    .nav-links a:hover { color: var(--text); }

    .hero {
      padding: 84px 0 44px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      min-height: 34px;
      padding: 0 12px;
      border-radius: 999px;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: .13em;
      color: var(--gold);
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 24px;
      margin-top: 22px;
      align-items: stretch;
    }

    .hero-main,
    .hero-side,
    .glass-card,
    .phase-panel,
    .about-main {
      background: linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.03));
      border: 1px solid rgba(255,255,255,0.09);
      box-shadow: var(--shadow);
    }

    .hero-main {
      border-radius: 34px;
      padding: 40px;
      position: relative;
      overflow: hidden;
    }

    .hero-main::after {
      content: "";
      position: absolute;
      right: -60px;
      bottom: -80px;
      width: 320px;
      height: 320px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(216,177,100,0.18), transparent 70%);
      pointer-events: none;
    }

    h1 {
      margin: 22px 0 18px;
      font-size: clamp(40px, 6vw, 76px);
      line-height: 1.02;
      letter-spacing: -0.05em;
    }

    h1 .gold { color: var(--gold); }

    .lead {
      margin: 0;
      max-width: 760px;
      color: var(--muted);
      font-size: 18px;
      line-height: 1.9;
    }

    .hero-actions {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      margin-top: 30px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 48px;
      padding: 0 18px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.1);
      background: rgba(255,255,255,0.04);
      transition: .2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
      background: rgba(255,255,255,0.08);
    }

    .btn-primary {
      border-color: rgba(216,177,100,0.34);
      background: linear-gradient(135deg, rgba(216,177,100,0.24), rgba(216,177,100,0.1));
    }

    .hero-meta {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
      margin-top: 42px;
    }

    .metric {
      padding: 18px 16px;
      border-radius: 18px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
    }

    .metric strong {
      display: block;
      font-size: clamp(24px, 3vw, 36px);
      line-height: 1;
      letter-spacing: -0.05em;
      margin-bottom: 8px;
    }

    .metric span {
      font-size: 12px;
      letter-spacing: .08em;
      text-transform: uppercase;
      color: var(--muted-2);
    }

    .hero-side {
      border-radius: 28px;
      padding: 22px;
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .side-card {
      border-radius: 22px;
      padding: 22px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
    }

    .side-label {
      font-size: 11px;
      letter-spacing: .14em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 12px;
    }

    .side-title {
      margin: 0 0 10px;
      font-size: 22px;
      letter-spacing: -0.03em;
    }

    .side-text {
      margin: 0;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.8;
    }

    .system-map {
      display: grid;
      gap: 10px;
      margin-top: 12px;
    }

    .map-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      padding: 12px 14px;
      border-radius: 16px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
      font-size: 14px;
    }

    .map-row span:last-child {
      color: var(--muted-2);
      font-size: 12px;
      text-align: right;
    }

    section { padding: 28px 0 36px; }

    .section-head {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 18px;
      margin-bottom: 22px;
    }

    .section-head h2 {
      margin: 0;
      font-size: clamp(30px, 4vw, 48px);
      letter-spacing: -0.05em;
    }

    .section-head p {
      margin: 0;
      max-width: 680px;
      color: var(--muted);
      line-height: 1.85;
      font-size: 16px;
    }

    .problems-grid,
    .tools-grid,
    .arch-grid,
    .deliver-grid,
    .about-grid,
    .highlights-grid {
      display: grid;
      gap: 18px;
    }

    .problems-grid,
    .tools-grid,
    .arch-grid,
    .highlights-grid { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .deliver-grid { grid-template-columns: repeat(4, minmax(0, 1fr)); }
    .about-grid { grid-template-columns: 1.05fr 0.95fr; }

    .glass-card {
      border-radius: 26px;
      padding: 24px;
      height: 100%;
    }

    .card-no {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 42px;
      height: 42px;
      border-radius: 14px;
      margin-bottom: 16px;
      background: var(--gold-soft);
      border: 1px solid rgba(216,177,100,0.24);
      color: var(--gold);
      font-weight: 800;
    }

    .card-title {
      margin: 0 0 10px;
      font-size: 22px;
      letter-spacing: -0.03em;
    }

    .card-text {
      margin: 0;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.85;
    }

    .mini-tags,
    .step-tools,
    .tool-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 16px;
    }

    .tag,
    .tool-tag {
      display: inline-flex;
      align-items: center;
      min-height: 30px;
      padding: 0 11px;
      border-radius: 999px;
      font-size: 12px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.05);
      color: var(--text);
    }

    .workflow-shell {
      display: grid;
      grid-template-columns: 320px minmax(0, 1fr);
      gap: 18px;
      align-items: start;
    }

    .phase-list {
      display: grid;
      gap: 12px;
      position: sticky;
      top: 88px;
    }

    .phase-btn {
      width: 100%;
      text-align: left;
      padding: 18px;
      border-radius: 22px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
      color: var(--text);
      cursor: pointer;
      transition: .18s ease;
    }

    .phase-btn:hover,
    .phase-btn.active {
      transform: translateY(-2px);
      border-color: rgba(216,177,100,0.34);
      background: linear-gradient(135deg, rgba(216,177,100,0.18), rgba(255,255,255,0.06));
    }

    .phase-stage {
      display: block;
      margin-bottom: 8px;
      font-size: 11px;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: var(--gold);
    }

    .phase-name {
      display: block;
      margin-bottom: 8px;
      font-size: 18px;
      font-weight: 700;
      letter-spacing: -0.03em;
    }

    .phase-sub {
      display: block;
      font-size: 13px;
      line-height: 1.6;
      color: var(--muted-2);
    }

    .phase-panel {
      border-radius: 30px;
      padding: 28px;
      min-height: 760px;
    }

    .phase-top {
      display: flex;
      justify-content: space-between;
      align-items: start;
      gap: 18px;
      margin-bottom: 22px;
    }

    .phase-top h3 {
      margin: 8px 0 10px;
      font-size: 34px;
      letter-spacing: -0.04em;
    }

    .phase-top p {
      margin: 0;
      max-width: 760px;
      color: var(--muted);
      line-height: 1.85;
    }

    .phase-chip {
      min-width: 160px;
      padding: 14px 16px;
      border-radius: 18px;
      text-align: center;
      border: 1px solid rgba(216,177,100,0.24);
      background: rgba(216,177,100,0.12);
      color: var(--gold);
      font-size: 13px;
      line-height: 1.55;
    }

    .steps {
      display: grid;
      gap: 14px;
    }

    .step {
      display: grid;
      grid-template-columns: 88px minmax(0, 1fr);
      gap: 18px;
      align-items: start;
      padding: 18px;
      border-radius: 22px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
    }

    .step-label {
      display: grid;
      gap: 6px;
      align-content: start;
    }

    .step-label strong {
      font-size: 12px;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: var(--gold);
    }

    .step-label span {
      font-size: 34px;
      line-height: 1;
      letter-spacing: -0.05em;
      font-weight: 800;
    }

    .step-title {
      margin: 0 0 8px;
      font-size: 20px;
      letter-spacing: -0.03em;
    }

    .step-copy {
      margin: 0;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.85;
    }

    .step-note {
      margin-top: 10px;
      color: var(--muted-2);
      font-size: 13px;
      line-height: 1.75;
    }

    .tool-cat {
      color: var(--gold);
      font-size: 11px;
      letter-spacing: .13em;
      text-transform: uppercase;
      margin-bottom: 10px;
    }

    .tool-title {
      margin: 0 0 10px;
      font-size: 20px;
      letter-spacing: -0.03em;
    }

    .tool-desc {
      margin: 0;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.85;
    }

    .arch-layer {
      position: relative;
      overflow: hidden;
    }

    .arch-layer::after {
      content: "";
      position: absolute;
      right: -30px;
      bottom: -40px;
      width: 180px;
      height: 180px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(216,177,100,0.14), transparent 70%);
      pointer-events: none;
    }

    .arch-title {
      margin: 0 0 10px;
      font-size: 21px;
      letter-spacing: -0.03em;
    }

    .arch-list {
      margin: 0;
      padding-left: 18px;
      display: grid;
      gap: 8px;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.8;
    }

    .deliver-card strong {
      display: block;
      margin-bottom: 10px;
      font-size: clamp(28px, 4vw, 44px);
      line-height: 1;
      letter-spacing: -0.05em;
      color: var(--gold);
    }

    .deliver-card h4 {
      margin: 0 0 8px;
      font-size: 18px;
      letter-spacing: -0.03em;
    }

    .deliver-card p {
      margin: 0;
      color: var(--muted);
      font-size: 14px;
      line-height: 1.8;
    }

    .about-main {
      padding: 28px;
      border-radius: 30px;
    }

    .about-name {
      margin: 8px 0 14px;
      font-size: clamp(34px, 4vw, 54px);
      letter-spacing: -0.05em;
    }

    .about-intro {
      margin: 0;
      max-width: 760px;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.9;
    }

    .manifesto {
      margin-top: 26px;
      padding: 22px;
      border-radius: 24px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
    }

    .manifesto p {
      margin: 0;
      font-size: 20px;
      line-height: 1.9;
      letter-spacing: -0.02em;
    }

    .about-side {
      display: grid;
      gap: 18px;
    }

    .footer {
      padding: 38px 0 64px;
      text-align: center;
      font-size: 13px;
      color: var(--muted-2);
    }

    .code-block {
      margin-top: 16px;
      padding: 16px;
      border-radius: 18px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(0,0,0,0.32);
      overflow: auto;
      font-size: 13px;
      line-height: 1.75;
      color: #efe7d5;
      font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;
    }

    @media (max-width: 1080px) {
      .hero-grid,
      .workflow-shell,
      .about-grid { grid-template-columns: 1fr; }

      .phase-list { position: static; }

      .hero-meta,
      .deliver-grid,
      .problems-grid,
      .tools-grid,
      .arch-grid,
      .highlights-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    }

    @media (max-width: 720px) {
      .container { width: min(var(--max), calc(100% - 20px)); }
      .nav-inner { align-items: flex-start; }
      .nav-links { gap: 12px; }
      .hero { padding-top: 54px; }
      .hero-main, .hero-side, .phase-panel, .about-main, .glass-card { padding: 20px; border-radius: 22px; }
      .hero-meta,
      .deliver-grid,
      .problems-grid,
      .tools-grid,
      .arch-grid,
      .highlights-grid { grid-template-columns: 1fr; }
      .phase-top { flex-direction: column; }
      .step { grid-template-columns: 1fr; }
      .manifesto p { font-size: 18px; }
    }
  </style>
</head>
<body>
  <header class="nav">
    <div class="container nav-inner">
      <a href="#top" class="brand">
        <div class="brand-mark">S</div>
        <div class="brand-copy">
          <strong>Slyvia · AI IG 内容运营系统</strong>
          <span>Brand Content × Instagram Workflow × AI System</span>
        </div>
      </a>
      <nav class="nav-links">
        <a href="#problems">问题</a>
        <a href="#workflow">工作流</a>
        <a href="#tools">工具库</a>
        <a href="#architecture">系统架构</a>
        <a href="#results">项目亮点</a>
        <a href="#about">关于</a>
      </nav>
    </div>
  </header>

  <main id="top">
    <section class="hero">
      <div class="container hero-grid">
        <div class="hero-main">
          <div class="eyebrow">AI Instagram Content Operating System</div>
          <h1>把品牌卖点<br><span class="gold">转成用户语言</span><br>把 IG 内容做成系统</h1>
          <p class="lead">
            这不是一个只会写文案的 AI 工具，而是一套真正从 Instagram 账号运营岗位出发设计的 AI 内容运营系统。
            它覆盖摸盘、选题、文案、审查、素材生成、飞书协同、审核状态监控、数据归档与复盘，
            让 IG 账号内容从“人肉串联”升级成“可复用、可协同、可沉淀”的工作方式。
          </p>
          <div class="hero-actions">
            <a class="btn btn-primary" href="#workflow">查看完整工作流</a>
            <a class="btn" href="#architecture">查看系统架构</a>
          </div>
          <div class="hero-meta">
            <div class="metric"><strong>20+</strong><span>Prompt 模板</span></div>
            <div class="metric"><strong>18+</strong><span>AI 介入节点</span></div>
            <div class="metric"><strong>4</strong><span>核心工作流</span></div>
            <div class="metric"><strong>100+</strong><span>内容资产沉淀</span></div>
          </div>
        </div>

        <aside class="hero-side">
          <div class="side-card">
            <div class="side-label">项目定位</div>
            <h3 class="side-title">IG 账号运营助手系统，不只是生成工具</h3>
            <p class="side-text">
              用 AI 做的不是“更快写完”，而是“更稳做对”。
              它同时服务内容判断、卖点转译、语感校准、素材协同、团队分发和后续复盘。
            </p>
          </div>
          <div class="side-card">
            <div class="side-label">系统能力图</div>
            <div class="system-map">
              <div class="map-row"><span>摸盘期</span><span>标签热度 / 竞品 Reels / 评论语料</span></div>
              <div class="map-row"><span>内容链路</span><span>选题 / 文案 / 审查 / 素材包</span></div>
              <div class="map-row"><span>互动链路</span><span>评论回复 / Story 衍生 / Creator 共创</span></div>
              <div class="map-row"><span>系统维护层</span><span>周复盘 / 月分析 / 库更新 / 人设守门</span></div>
              <div class="map-row"><span>协同方式</span><span>飞书群 / 多维表格 / Obsidian / Wiki</span></div>
              <div class="map-row"><span>素材工具</span><span>Dreamina / Nano Banana / img2prompt / CapCut</span></div>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <section id="problems">
      <div class="container">
        <div class="section-head">
          <div>
            <div class="eyebrow">Three real problems</div>
            <h2>IG 账号运营真正卡住的，不只是写文案</h2>
          </div>
          <p>
            真正的低效来自三个地方：不知道方向值不值得做、内容写出来却没有传播力、协同与归档全靠人脑记。
            所以这套系统要解决的，不是单点提效，而是把内容从前端判断到后端复盘全部接起来。
          </p>
        </div>

        <div class="problems-grid">
          <article class="glass-card">
            <div class="card-no">01</div>
            <h3 class="card-title">方向值不值得做</h3>
            <p class="card-text">
              话题有没有热度？竞品在打什么表达？用户在评论区真正会被什么内容触发？如果没有摸盘，内容一开始就可能做偏。
            </p>
            <div class="mini-tags">
              <span class="tag">Instagram Search</span>
              <span class="tag">Meta Ad Library</span>
              <span class="tag">Claude Chrome</span>
            </div>
          </article>

          <article class="glass-card">
            <div class="card-no">02</div>
            <h3 class="card-title">内容写了却不成势</h3>
            <p class="card-text">
              文案像说明书、首图不够抓人、Carousel 节奏太平、Reels 开头没有钩子，最后发出去没人收藏，也没人愿意互动。
            </p>
            <div class="mini-tags">
              <span class="tag">卖点转译</span>
              <span class="tag">Dreamina</span>
              <span class="tag">Nano Banana</span>
            </div>
          </article>

          <article class="glass-card">
            <div class="card-no">03</div>
            <h3 class="card-title">链路不闭环</h3>
            <p class="card-text">
              选题、写稿、素材、评论区话术、飞书分发、审核状态和数据归档分散在不同地方，团队每天都在重复找版本、找素材、找结论。
            </p>
            <div class="mini-tags">
              <span class="tag">飞书群</span>
              <span class="tag">多维表格</span>
              <span class="tag">Obsidian</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="workflow">
      <div class="container">
        <div class="section-head">
          <div>
            <div class="eyebrow">Workflow</div>
            <h2>完整工作流</h2>
          </div>
          <p>
            点击任意阶段，查看每个 AI 节点的具体执行逻辑。
            这套工作流只围绕 IG 账号运营展开，从摸盘、内容产出、互动运营到系统维护，尽量贴近真实品牌内容岗的推进方式。
          </p>
        </div>

        <div class="workflow-shell">
          <div class="phase-list" id="phaseList"></div>
          <div class="phase-panel" id="phasePanel"></div>
        </div>
      </div>
    </section>

    <section id="tools">
      <div class="container">
        <div class="section-head">
          <div>
            <div class="eyebrow">Tool Library</div>
            <h2>工具库</h2>
          </div>
          <p>
            不是简单叠加工具，而是让每个工具在链路里承担明确角色：Claude 负责理解与生成，Instagram Search 与 Meta Ad Library 负责给判断依据，
            img2prompt、即梦 Dreamina、Nano Banana、CapCut AI 负责把内容感受转成素材，飞书负责协同，Obsidian 和 Wiki 负责沉淀。
          </p>
        </div>

        <div class="tools-grid">
          <article class="glass-card">
            <div class="tool-cat">摸盘</div>
            <h3 class="tool-title">Instagram Search + Meta Ad Library + Claude Chrome</h3>
            <p class="tool-desc">用于标签热度检索、竞品账号观察、Reels 结构抓取和评论区语料挖掘，让冷启动不靠感觉，而靠可观察的数据与真实表达。</p>
            <div class="tool-tags"><span class="tool-tag">Instagram Search</span><span class="tool-tag">Meta Ad Library</span><span class="tool-tag">Claude Chrome</span></div>
          </article>

          <article class="glass-card">
            <div class="tool-cat">内容</div>
            <h3 class="tool-title">Claude + Slyvia Skill + 产品知识库</h3>
            <p class="tool-desc">负责内容方向规划、爆款拆解、文案初稿、营销感降调、Creator brief、评论回复与周复盘，让内容既有速度，也有品牌语感。</p>
            <div class="tool-tags"><span class="tool-tag">Claude</span><span class="tool-tag">Slyvia Skill</span><span class="tool-tag">产品知识库</span></div>
          </article>

          <article class="glass-card">
            <div class="tool-cat">素材</div>
            <h3 class="tool-title">img2prompt + 即梦 Dreamina + Nano Banana + CapCut AI</h3>
            <p class="tool-desc">负责首图参考、Carousel 配图、Story 视觉延展、Reels 首帧、贴纸化素材与局部改图，解决内容“能写但不好看”的问题。</p>
            <div class="tool-tags"><span class="tool-tag">img2prompt</span><span class="tool-tag">即梦 Dreamina</span><span class="tool-tag">Nano Banana</span><span class="tool-tag">CapCut AI</span></div>
          </article>

          <article class="glass-card">
            <div class="tool-cat">协同</div>
            <h3 class="tool-title">feishu-group + 飞书多维表格</h3>
            <p class="tool-desc">负责把文案、素材建议、审核状态和复盘结论推送给团队，并在表格里做账号、维度、时间和数据的结构化归档。</p>
            <div class="tool-tags"><span class="tool-tag">飞书群</span><span class="tool-tag">飞书 Base</span><span class="tool-tag">状态归档</span></div>
          </article>

          <article class="glass-card">
            <div class="tool-cat">沉淀</div>
            <h3 class="tool-title">Obsidian + lark-wiki + lark-minutes</h3>
            <p class="tool-desc">负责存高互动结构、Creator 协作经验、会议纪要、活动模板、周复盘和知识库，让每次优化都能沉淀回系统，不只停留在脑子里。</p>
            <div class="tool-tags"><span class="tool-tag">Obsidian</span><span class="tool-tag">lark-wiki</span><span class="tool-tag">lark-minutes</span></div>
          </article>

          <article class="glass-card">
            <div class="tool-cat">监控</div>
            <h3 class="tool-title">loop 监控 + 数据回写</h3>
            <p class="tool-desc">负责审核状态追踪、内容表现抓取和归档回写，让每条发出去的内容都能留下原始记录，为下次复盘提供真正可用的数据底稿。</p>
            <div class="tool-tags"><span class="tool-tag">loop 监控</span><span class="tool-tag">数据归档</span><span class="tool-tag">周复盘</span></div>
          </article>
        </div>
      </div>
    </section>

    <section id="architecture">
      <div class="container">
        <div class="section-head">
          <div>
            <div class="eyebrow">System Architecture</div>
            <h2>系统架构</h2>
          </div>
          <p>
            这套网站展示的不只是方法论，也是一个可落地的轻量 IG 内容运营中台：前端有品牌与内容 sense，
            中台有 AI 任务拆分，后端有飞书协同、数据库存储、审核状态监控和知识库归档机制。这里不做定时发布，而是输出可直接取用的发布素材包与归档结果。
          </p>
        </div>

        <div class="arch-grid">
          <article class="glass-card arch-layer">
            <h3 class="arch-title">应用层</h3>
            <ul class="arch-list">
              <li>单页介绍站 / 作品集展示</li>
              <li>项目说明、工作流展示与案例承载</li>
              <li>可扩展为 SOP 展示页或 Demo 页</li>
            </ul>
          </article>

          <article class="glass-card arch-layer">
            <h3 class="arch-title">AI 调用层</h3>
            <ul class="arch-list">
              <li>Claude：洞察、生成、审查、复盘</li>
              <li>Slyvia Skill：风格手册、任务模板、品牌语感</li>
              <li>Dreamina / Nano Banana / img2prompt：素材生成与改图</li>
            </ul>
          </article>

          <article class="glass-card arch-layer">
            <h3 class="arch-title">内容输入层</h3>
            <ul class="arch-list">
              <li>Instagram Search、Meta Ad Library、竞品 Reels</li>
              <li>评论区语料、Creator 内容、历史高互动样本</li>
              <li>产品知识库、活动模板、IP 人设规范</li>
            </ul>
          </article>

          <article class="glass-card arch-layer">
            <h3 class="arch-title">交付协同层</h3>
            <ul class="arch-list">
              <li>飞书群：文案、素材包与评论话术推送</li>
              <li>飞书多维表格：状态、版本、数据归档</li>
              <li>飞书文档 / Wiki：brief、周报、知识沉淀</li>
            </ul>
          </article>

          <article class="glass-card arch-layer">
            <h3 class="arch-title">数据存储层</h3>
            <ul class="arch-list">
              <li>PostgreSQL：brief / version / metrics / logs</li>
              <li>对象存储：首图、Carousel、Story、素材参考</li>
              <li>Obsidian：高胜率结构、案例、规则沉淀</li>
            </ul>
          </article>

          <article class="glass-card arch-layer">
            <h3 class="arch-title">监控归档层</h3>
            <ul class="arch-list">
              <li>审核状态监控与结果回写</li>
              <li>内容数据回流与周/月复盘生成</li>
              <li>禁词库、知识库与 Skill 规则迭代</li>
            </ul>
          </article>
        </div>

        <div class="code-block">slyvia-ig-content-system/
├─ app/
│  ├─ api/
│  ├─ services/
│  │  ├─ anthropic_client.py
│  │  ├─ feishu_client.py
│  │  ├─ review_service.py
│  │  ├─ asset_pack_service.py
│  │  └─ archive_service.py
│  ├─ jobs/
│  │  ├─ insight_scan.py
│  │  ├─ generate_brief.py
│  │  ├─ build_asset_pack.py
│  │  ├─ sync_review_status.py
│  │  └─ weekly_review.py
│  └─ db/
├─ prompts/
│  ├─ system/
│  ├─ workflows/
│  └─ validators/
└─ skill/
   ├─ SKILL.md
   └─ slyvia-skill.config.yaml</div>
      </div>
    </section>

    <section id="results">
      <div class="container">
        <div class="section-head">
          <div>
            <div class="eyebrow">Project Highlights</div>
            <h2>项目亮点</h2>
          </div>
          <p>
            这套系统的价值不只是“快”，而是让内容判断、内容产出、素材配合和团队协同同时更稳。
            每做完一个项目，系统都不会归零，而是继续沉淀成下一轮可复用资产。
          </p>
        </div>

        <div class="deliver-grid">
          <article class="glass-card deliver-card">
            <strong>20+</strong>
            <h4>Prompt 模板</h4>
            <p>覆盖摸盘、brief、文案、审查、素材提示词、评论话术、Creator brief、周报月报等内容任务。</p>
          </article>

          <article class="glass-card deliver-card">
            <strong>18+</strong>
            <h4>AI 介入节点</h4>
            <p>从话题检索、竞品抓取、语料挖掘到素材包、飞书协同、状态监控与复盘，形成完整链路。</p>
          </article>

          <article class="glass-card deliver-card">
            <strong>4</strong>
            <h4>核心工作流</h4>
            <p>覆盖摸盘期、IG 内容链路、IG 互动链路与系统维护层，全部围绕 Instagram 账号运营展开。</p>
          </article>

          <article class="glass-card deliver-card">
            <strong>100+</strong>
            <h4>内容资产沉淀</h4>
            <p>每条内容从 brief、初稿、审核稿、素材建议到数据快照都可追溯，并可被后续项目直接复用。</p>
          </article>
        </div>

        <div class="highlights-grid" style="margin-top:18px;">
          <article class="glass-card">
            <div class="card-no">A</div>
            <h3 class="card-title">更强的内容 sense</h3>
            <p class="card-text">
              系统最核心的价值不是写得多，而是能把偏理性的品牌信息，稳定翻译成更适合 IG 传播的表达、结构和场景。
            </p>
          </article>

          <article class="glass-card">
            <div class="card-no">B</div>
            <h3 class="card-title">更稳的素材配合</h3>
            <p class="card-text">
              不是文案写完再临时找图，而是让 img2prompt、Dreamina、Nano Banana 和 CapCut AI 参与到内容结构里，让首图、Carousel、Story 和 Reels 首帧从一开始就对齐。
            </p>
          </article>

          <article class="glass-card">
            <div class="card-no">C</div>
            <h3 class="card-title">更可复用的团队资产</h3>
            <p class="card-text">
              评论钩子、Creator brief、禁词规则、高互动结构、视觉策略、知识库与 Skill 规则都会沉淀下来，项目做完系统不会归零。
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container about-grid">
        <div class="about-main">
          <div class="eyebrow">About this project</div>
          <h2 class="about-name">Slyvia · AI IG 内容运营系统</h2>
          <p class="about-intro">
            我做的不是一个“帮我写几条文案”的工具，而是一套真正从 Instagram 内容运营岗位出发设计的 AI 工作流。
            它同时服务三个目标：让品牌卖点更容易被用户感知，让内容节奏更容易被团队执行，让项目经验更容易沉淀成下一轮可复用资产。
          </p>
          <div class="manifesto">
            <p>
              内容不是素材堆砌。<br>
              内容是品牌语言、用户情绪、渠道任务和复盘机制的组合。<br>
              把重复执行交给 AI，把真正重要的判断留给运营。
            </p>
          </div>
        </div>

        <div class="about-side">
          <article class="glass-card">
            <div class="side-label">身份 01</div>
            <h3 class="side-title">IG 内容运营负责人</h3>
            <p class="side-text">能从品牌卖点出发判断什么值得做内容，也知道怎么把内容推向用户愿意停留、收藏和评论的方向。</p>
          </article>
          <article class="glass-card">
            <div class="side-label">身份 02</div>
            <h3 class="side-title">AI 内容系统设计者</h3>
            <p class="side-text">将摸盘、文案、素材、审查、协同、监控和复盘做成标准模块，让系统越来越会“自己跑”。</p>
          </article>
          <article class="glass-card">
            <div class="side-label">身份 03</div>
            <h3 class="side-title">品牌内容 sense</h3>
            <p class="side-text">比起单纯提效，更在意内容是否像品牌、像用户会接受的语言、像真正能带来长期价值的表达。</p>
          </article>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container">Slyvia · AI IG 内容运营系统 Demo</div>
  </footer>

  <script>
    const phases = [
      {
        stage: '阶段 0 · 摸盘期',
        name: '接到新项目',
        sub: '先把方向判断做清楚，再决定内容该往哪里打。',
        intro: '这一层解决的不是“写什么”，而是“值不值得做”。先通过话题热度、竞品 Reels 结构和评论区语料把赛道摸清，再决定内容调性、账号表达方向和首批选题。',
        chip: '热度判断 / 竞品拆解 / 评论语料',
        steps: [
          {
            label: '侦察',
            title: '话题热度检索',
            text: '打开 Instagram Search、Explore 页和 Meta Ad Library，在 Chrome 侧边栏调出 Claude，实时分析标签热度、竞品动作和表达密度，判断这个方向值不值得做。',
            tools: ['Instagram Search', 'Meta Ad Library', 'Claude Chrome插件'],
            note: '💡 不靠感觉判断方向，AI 先帮你看清这个话题是不是值得花内容成本。'
          },
          {
            label: '情报',
            title: '竞品账号 / Reels 结构抓取',
            text: '让 Claude 批量抓取同类品牌和 Creator 的高互动 Reels / Carousel，分析首帧逻辑、标题结构、镜头节奏和评论触发方式，整理出共同爆款基因。',
            tools: ['Claude Chrome', 'img2prompt'],
            note: '💡 高互动不是偶然，AI 帮你把“看起来好像很会做”拆成真正可复用的结构。'
          },
          {
            label: '洞察',
            title: '评论区语料挖掘',
            text: '让 Claude 爬取高互动帖子评论区，提炼用户真实痛点、高频词汇、审美偏好和情绪触发点，直接转化成内容方向。',
            tools: ['Claude Chrome侧边栏', '评论语料表'],
            note: '💡 用户替你说出了最值得做的内容角度，AI 负责把它们收拢成方向。'
          },
          {
            label: '决策',
            title: '冷启动方向定稿',
            text: '把以上数据综合输入 Claude，生成「Reels 增长型 vs Feed 收藏型」策略建议，确定内容调性、账号表达方向和首批 10 个选题。',
            tools: ['Claude', 'Slyvia Skill'],
            note: '💡 摸盘结束，不只是得到灵感，而是输出一版可执行的 IG 内容战略。'
          }
        ]
      },
      {
        stage: '工作流 1 · IG 内容链路',
        name: '账号内容生产链路',
        sub: '从方向规划到素材包交付，把内容和视觉都做成闭环。',
        intro: '这一层更像真实的 IG 账号运营节奏：先做周内容结构，再复盘高互动样本，接着生成初稿、做营销感校准、联动素材工具，最后把内容包推给团队取用与归档。',
        chip: '内容规划 / 文案 / 素材 / 归档',
        steps: [
          {
            label: '策略',
            title: '内容方向规划',
            text: '每周一次，Claude 根据账号数据、节日节点、品牌新品和竞品动态，输出「一周内容结构规划」，确定本周 Feed、Carousel、Reels、Story 的维度分布。',
            tools: ['Claude', '内容规划 Skill'],
            note: '💡 不是把所有内容都做成同一种感觉，而是先安排清楚这一周的表达节奏。'
          },
          {
            label: '数据',
            title: '高互动内容复盘',
            text: '每周从真实数据里挑出表现好的帖子，让 Claude 拆解首帧公式、标题句式、镜头停留点、评论触发点和保存理由，提炼可复用模板放进 Obsidian 知识库。',
            tools: ['Claude', 'Obsidian存档'],
            note: '💡 高互动不是“某条碰巧”，而是系统会反复出现的结构。'
          },
          {
            label: '创作',
            title: '文案初稿生成',
            text: '从产品知识库、品牌语言和真实使用场景里取材，调用 Slyvia Skill，Claude 按「像真人在说话」的风格手册生成 IG 图文、Carousel 文案和 Reels 口播初稿。',
            tools: ['Claude', 'Slyvia Skill', '产品知识库'],
            note: '💡 先有真实素材，AI 才能写出不像模板机的内容。知识库是根基。'
          },
          {
            label: '审查',
            title: '营销感降调 + 禁词过滤',
            text: '初稿写完，Claude 对照平台禁区词库和「营销感降调」标准，逐条过滤硬广词汇、卖点词堆砌和不自然 CTA，用感受词库替换。',
            tools: ['Claude', '禁词库', '感受词库'],
            note: '💡 通过率高、保存率高的内容通常都更“软”，更像真实的人在说话。'
          },
          {
            label: '配图',
            title: '首图 / Carousel 配图生成',
            text: '文案确定后，参考竞品高互动首图和 Carousel 构图逻辑（img2prompt 反推），用即梦 Dreamina 生成首图氛围图，用 Nano Banana 做局部改图、风格统一和素材延展。',
            tools: ['img2prompt', '即梦 Dreamina', 'Nano Banana'],
            note: '💡 首图决定用户停不停，第二张之后才决定他会不会继续滑。'
          },
          {
            label: '延展',
            title: 'Reels / Story 素材延展',
            text: '针对同一主题继续生成 Reels 首帧参考、Story 贴纸化元素、问答贴图和字幕视觉草案，必要时用 CapCut AI 做短视频素材整合。',
            tools: ['Nano Banana', '即梦 Dreamina', 'CapCut AI'],
            note: '💡 不让内容只停在一条帖子上，而是把一个主题延展成一整组 IG 可用素材。'
          },
          {
            label: '分发',
            title: '飞书推送 · 团队直取',
            text: '内容通过审查后，把文案、首图建议、Carousel 顺序、Reels 参考和 Story 素材说明通过 feishu-group Skill 推送到飞书群，团队成员直接取用。',
            tools: ['feishu-group', '飞书多维表格'],
            note: '💡 我不负责重复发版本，我负责让团队拿到一套可以直接执行的内容包。'
          },
          {
            label: '归档',
            title: '审核状态 + 数据归档',
            text: '内容交付后，loop 监控审核状态与执行反馈，通过后数据自动写入飞书多维表格，按账号、维度、形式、时间归档，为下次复盘提供原始数据。',
            tools: ['loop监控', 'lark-base'],
            note: '💡 所有发出去的内容都要留档，复盘才有料。'
          }
        ]
      },
      {
        stage: '工作流 2 · IG 互动链路',
        name: '评论 / Story / Creator 互动链路',
        sub: '不是发完就结束，而是把互动也变成内容资产。',
        intro: '这一层不是私域，而是 IG 账号运营里最容易被忽略的互动层：评论区、Story 互动、Creator brief 和 UGC 二创。系统负责把互动从“临场发挥”变成“提前设计”。',
        chip: '评论 / Story / Creator / UGC',
        steps: [
          {
            label: '节奏',
            title: '周内容节奏配比',
            text: 'Claude 根据账号目标自动安排本周 Feed、Carousel、Reels、Story、互动贴和 Giveaway 的配比，避免整周都在讲同一件事，造成审美疲劳。',
            tools: ['Claude', '节奏规划 Skill'],
            note: '💡 IG 不是只看单条，而是看整个账号这一周有没有呼吸感。'
          },
          {
            label: '社区',
            title: '评论区回复建议',
            text: '内容上线后，Claude 根据评论区高频问题和互动氛围，提前生成首轮回复、追问句和收藏引导话术，让评论区本身也成为内容延伸。',
            tools: ['Claude', '评论话术库'],
            note: '💡 评论区不是客服区，它也是内容的一部分。'
          },
          {
            label: '二创',
            title: 'UGC / 用户反馈转二创',
            text: '把高质量评论、用户晒单和真实反馈提炼成二创角度，必要时用 Dreamina 和 Nano Banana 统一视觉风格，生成可用于 Story 或 Carousel 的二次素材。',
            tools: ['Claude', '即梦 Dreamina', 'Nano Banana'],
            note: '💡 最打动人的内容，很多时候来自用户已经替你说过的话。'
          },
          {
            label: '共创',
            title: 'Creator Brief 设计',
            text: '针对合作达人或 Creator，Claude 自动生成包含卖点重点、镜头建议、情绪方向、禁止表达和输出清单的 brief，减少来回口头解释成本。',
            tools: ['Claude', 'Creator Brief库'],
            note: '💡 共创不是把素材丢给达人，而是提前把能拍成什么说清楚。'
          },
          {
            label: 'Story',
            title: 'Story 互动素材设计',
            text: '围绕同一主题同步设计 Story 问答、投票、进度条、贴纸文案和引导语，用 Nano Banana / Dreamina 衍生轻量视觉元素，保持账号一周内表达的一致性。',
            tools: ['Claude', 'Nano Banana', '即梦 Dreamina'],
            note: '💡 Story 不是边角料，它是把 Feed 热度接住的地方。'
          },
          {
            label: '活动',
            title: 'Giveaway / 互动活动策划',
            text: '从品牌节点和账号目标出发，Claude 设计 Giveaway 文案、参与机制、评论触发问题和 Creator 联动建议，让活动既涨互动，也不显得太硬。',
            tools: ['Claude', '活动模板库'],
            note: '💡 好的互动活动不是送得多，而是让参与理由本身就像内容。'
          },
          {
            label: '同步',
            title: '飞书群一键同步',
            text: '评论话术、Story 素材说明、Creator brief 和活动脚本通过 feishu-group 推送到飞书群，团队不需要来回找版本，直接照着执行。',
            tools: ['feishu-group', '飞书文档'],
            note: '💡 互动运营不是临场救火，提前同步之后，整个团队都能接得更顺。'
          }
        ]
      },
      {
        stage: '系统维护层',
        name: '让系统越跑越准',
        sub: '周复盘、月分析、库更新与人设守门。',
        intro: '真正的系统不是能跑一轮，而是能持续校准。维护层负责整理每周规则变化、每月数据判断、知识库迭代和账号人设校验，让内容不只越来越快，也越来越准。',
        chip: '复盘 / 分析 / 迭代 / 校验',
        steps: [
          {
            label: '周维护',
            title: '周数据复盘 + 禁词整理',
            text: '每周五，Claude 汇总本周帖子数据，对比各维度表现，输出「下周方向调整建议」。同步整理本周新出现的平台敏感表达，更新禁词库。',
            tools: ['Claude', 'lark-minutes', '禁词库'],
            note: '💡 平台表达习惯一直在变，规则不更新，就等于让账号用旧地图继续走。'
          },
          {
            label: '月维护',
            title: 'IG 内容表现分析',
            text: '每月拉取账号内容数据，Claude 分析各类 Feed、Carousel、Reels、Story 的保存率、评论率、分享率和主页访问表现，输出「下月方向 + 形式调整」。',
            tools: ['Claude', '账号数据看板'],
            note: '💡 数据不是为了证明过去，而是为了决定下个月该把力气花在哪里。'
          },
          {
            label: '库维护',
            title: '知识库更新 + Skill 迭代',
            text: '把跑通的高互动结构、新的 Creator 合作经验、优化后的评论话术和素材策略，定期同步到 Obsidian 知识库，同时更新 Slyvia Skill 的语感规则和产品知识库。',
            tools: ['Obsidian', 'skill-creator', 'Slyvia Skill'],
            note: '💡 每一次优化都要沉淀回系统，否则经验只在脑子里，无法复用。'
          },
          {
            label: 'IP守门',
            title: '账号人设定期校验',
            text: '每隔一段时间，让 Claude 对照账号历史内容和人设定义，检查是否有漂移——有没有开始像别人？有没有丢失自己的风格锚点？',
            tools: ['Claude', 'IP人设规范'],
            note: '💡 账号做久了最容易犯的错不是内容变差，而是慢慢失去自己原本的声音。'
          }
        ]
      }
    ];

    const phaseList = document.getElementById('phaseList');
    const phasePanel = document.getElementById('phasePanel');
    let activeIndex = 0;

    function renderPhaseButtons() {
      phaseList.innerHTML = phases.map((phase, index) => `
        <button class="phase-btn ${index === activeIndex ? 'active' : ''}" data-index="${index}">
          <span class="phase-stage">${phase.stage}</span>
          <span class="phase-name">${phase.name}</span>
          <span class="phase-sub">${phase.sub}</span>
        </button>
      `).join('');

      [...phaseList.querySelectorAll('.phase-btn')].forEach(btn => {
        btn.addEventListener('click', () => {
          activeIndex = Number(btn.dataset.index);
          renderPhaseButtons();
          renderPhasePanel();
        });
      });
    }

    function renderPhasePanel() {
      const phase = phases[activeIndex];
      phasePanel.innerHTML = `
        <div class="phase-top">
          <div>
            <div class="eyebrow">${phase.stage}</div>
            <h3>${phase.name}</h3>
            <p>${phase.intro}</p>
          </div>
          <div class="phase-chip">核心逻辑<br><strong>${phase.chip}</strong></div>
        </div>
        <div class="steps">
          ${phase.steps.map((step, i) => `
            <article class="step">
              <div class="step-label">
                <strong>${step.label}</strong>
                <span>${String(i + 1).padStart(2, '0')}</span>
              </div>
              <div>
                <h4 class="step-title">${step.title}</h4>
                <p class="step-copy">${step.text}</p>
                <div class="step-tools">
                  ${(step.tools || []).map(tool => `<span class="tool-tag">${tool}</span>`).join('')}
                </div>
                <div class="step-note">${step.note}</div>
              </div>
            </article>
          `).join('')}
        </div>
      `;
    }

    renderPhaseButtons();
    renderPhasePanel();
  </script>
</body>
</html>
