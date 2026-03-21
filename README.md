# juuungwon.github.io
juuungwon.github.io


<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Your Name — Personal Page</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --black: #3A3A3A;
      --accent: #4B70F5;
      --accent-light: #EEF1FF;
      --accent-mid: #7B97F8;
      --bg: #F7F8FC;
      --white: #FFFFFF;
      --gray-1: #F0F1F6;
      --gray-2: #C8CBD8;
      --gray-3: #8A8FA8;
      --gray-4: #5A5F75;
      --card-bg: #FFFFFF;
      --border: rgba(75,112,245,0.10);
      --shadow-sm: 0 2px 12px rgba(75,112,245,0.07);
      --shadow-md: 0 8px 32px rgba(75,112,245,0.12);
      --shadow-lg: 0 24px 64px rgba(75,112,245,0.16);
      --radius: 20px;
      --radius-sm: 12px;
      --nav-h: 68px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Noto Sans KR', 'Sora', sans-serif;
      background: var(--bg);
      color: var(--black);
      line-height: 1.7;
      -webkit-font-smoothing: antialiased;
    }

    /* ─── SCROLLBAR ─── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: transparent; }
    ::-webkit-scrollbar-thumb { background: var(--accent-mid); border-radius: 99px; }

    /* ─── NAV ─── */
    nav {
      position: fixed; top: 0; left: 0; right: 0;
      height: var(--nav-h);
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 clamp(24px, 5vw, 80px);
      background: rgba(247,248,252,0.82);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
      z-index: 100;
      transition: box-shadow .3s;
    }
    nav.scrolled { box-shadow: var(--shadow-sm); }

    .nav-logo {
      font-family: 'Sora', sans-serif;
      font-weight: 700;
      font-size: 1.15rem;
      color: var(--accent);
      letter-spacing: -0.02em;
      text-decoration: none;
    }

    .nav-links {
      display: flex; gap: 8px; list-style: none;
    }
    .nav-links a {
      font-size: 0.875rem;
      font-weight: 500;
      color: var(--gray-4);
      text-decoration: none;
      padding: 7px 14px;
      border-radius: 99px;
      transition: background .2s, color .2s;
    }
    .nav-links a:hover {
      background: var(--accent-light);
      color: var(--accent);
    }

    /* ─── MAIN WRAPPER ─── */
    main {
      max-width: 860px;
      margin: 0 auto;
      padding: calc(var(--nav-h) + 64px) clamp(20px, 4vw, 0px) 120px;
    }

    /* ─── HERO ─── */
    .hero {
      display: flex;
      align-items: center;
      gap: 48px;
      margin-bottom: 96px;
      animation: fadeUp .8s ease both;
    }

    .hero-avatar {
      flex-shrink: 0;
      width: 120px; height: 120px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--accent-light) 0%, var(--accent-mid) 100%);
      display: flex; align-items: center; justify-content: center;
      font-family: 'Sora', sans-serif;
      font-size: 2.5rem;
      font-weight: 700;
      color: var(--white);
      box-shadow: var(--shadow-md);
      overflow: hidden;
    }
    .hero-avatar img {
      width: 100%; height: 100%; object-fit: cover;
    }

    .hero-text h1 {
      font-family: 'Sora', sans-serif;
      font-size: clamp(2rem, 4vw, 2.75rem);
      font-weight: 700;
      letter-spacing: -0.03em;
      color: var(--black);
      line-height: 1.2;
      margin-bottom: 10px;
    }
    .hero-text h1 span { color: var(--accent); }

    .hero-text .role {
      font-size: 1.05rem;
      font-weight: 500;
      color: var(--gray-3);
      margin-bottom: 18px;
    }

    .hero-text p {
      font-size: 0.975rem;
      color: var(--gray-4);
      max-width: 480px;
      line-height: 1.8;
      margin-bottom: 24px;
    }

    .hero-links {
      display: flex; gap: 10px; flex-wrap: wrap;
    }
    .btn {
      display: inline-flex; align-items: center; gap: 7px;
      padding: 10px 20px;
      border-radius: 99px;
      font-size: 0.875rem;
      font-weight: 600;
      text-decoration: none;
      transition: transform .2s, box-shadow .2s;
      cursor: pointer; border: none;
    }
    .btn:hover { transform: translateY(-2px); }
    .btn-primary {
      background: var(--accent);
      color: #fff;
      box-shadow: 0 4px 16px rgba(75,112,245,0.35);
    }
    .btn-primary:hover { box-shadow: 0 8px 24px rgba(75,112,245,0.45); }
    .btn-ghost {
      background: var(--gray-1);
      color: var(--gray-4);
    }
    .btn-ghost:hover { background: var(--accent-light); color: var(--accent); }

    /* ─── SECTION ─── */
    section {
      margin-bottom: 80px;
      animation: fadeUp .7s ease both;
    }
    section:nth-child(2) { animation-delay: .05s; }
    section:nth-child(3) { animation-delay: .10s; }
    section:nth-child(4) { animation-delay: .15s; }
    section:nth-child(5) { animation-delay: .20s; }

    .section-label {
      display: inline-flex; align-items: center; gap: 8px;
      font-family: 'Sora', sans-serif;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 8px;
    }
    .section-label::before {
      content: '';
      width: 6px; height: 6px;
      background: var(--accent);
      border-radius: 50%;
    }

    .section-title {
      font-family: 'Sora', sans-serif;
      font-size: clamp(1.5rem, 3vw, 2rem);
      font-weight: 700;
      letter-spacing: -0.03em;
      color: var(--black);
      margin-bottom: 32px;
    }

    /* ─── CARDS ─── */
    .card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 28px 32px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-sm);
      transition: box-shadow .25s, transform .25s;
    }
    .card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-3px);
    }

    /* ─── RESEARCH INTERESTS ─── */
    .interests-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 16px;
    }
    .interest-card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 24px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-sm);
      transition: all .25s;
    }
    .interest-card:hover {
      border-color: var(--accent);
      box-shadow: var(--shadow-md);
      transform: translateY(-3px);
    }
    .interest-icon {
      width: 44px; height: 44px;
      background: var(--accent-light);
      border-radius: var(--radius-sm);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.35rem;
      margin-bottom: 14px;
    }
    .interest-card h3 {
      font-family: 'Sora', sans-serif;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--black);
      margin-bottom: 6px;
    }
    .interest-card p {
      font-size: 0.83rem;
      color: var(--gray-3);
      line-height: 1.6;
    }

    /* ─── TIMELINE (Education / Experience) ─── */
    .timeline { display: flex; flex-direction: column; gap: 0; }

    .timeline-item {
      display: flex;
      gap: 24px;
      padding-bottom: 36px;
      position: relative;
    }
    .timeline-item:last-child { padding-bottom: 0; }

    .timeline-left {
      display: flex; flex-direction: column; align-items: center;
      flex-shrink: 0; width: 48px;
    }
    .timeline-dot {
      width: 14px; height: 14px;
      background: var(--accent);
      border-radius: 50%;
      border: 3px solid var(--bg);
      box-shadow: 0 0 0 2px var(--accent);
      flex-shrink: 0; margin-top: 4px;
    }
    .timeline-line {
      width: 2px;
      flex: 1;
      background: linear-gradient(to bottom, var(--accent), var(--border));
      margin-top: 8px;
      min-height: 24px;
    }
    .timeline-item:last-child .timeline-line { display: none; }

    .timeline-body {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 22px 26px;
      border: 1px solid var(--border);
      flex: 1;
      transition: box-shadow .25s, transform .25s;
    }
    .timeline-body:hover { box-shadow: var(--shadow-md); transform: translateY(-2px); }

    .timeline-period {
      font-size: 0.78rem;
      font-weight: 600;
      color: var(--accent);
      letter-spacing: 0.04em;
      margin-bottom: 4px;
    }
    .timeline-body h3 {
      font-family: 'Sora', sans-serif;
      font-size: 1.02rem;
      font-weight: 700;
      color: var(--black);
      margin-bottom: 2px;
    }
    .timeline-body .sub {
      font-size: 0.88rem;
      color: var(--gray-3);
      margin-bottom: 8px;
      font-weight: 500;
    }
    .timeline-body p {
      font-size: 0.875rem;
      color: var(--gray-4);
      line-height: 1.7;
    }

    /* ─── PUBLICATIONS ─── */
    .pub-list { display: flex; flex-direction: column; gap: 16px; }

    .pub-card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 24px 28px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-sm);
      transition: all .25s;
      display: flex; gap: 20px; align-items: flex-start;
    }
    .pub-card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-2px);
      border-color: rgba(75,112,245,0.25);
    }

    .pub-year {
      flex-shrink: 0;
      font-family: 'Sora', sans-serif;
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--accent);
      background: var(--accent-light);
      padding: 4px 12px;
      border-radius: 99px;
      margin-top: 2px;
      white-space: nowrap;
    }

    .pub-content h3 {
      font-family: 'Sora', sans-serif;
      font-size: 0.97rem;
      font-weight: 600;
      color: var(--black);
      line-height: 1.5;
      margin-bottom: 5px;
    }
    .pub-venue {
      font-size: 0.83rem;
      color: var(--gray-3);
      font-weight: 500;
      margin-bottom: 10px;
    }
    .pub-tags { display: flex; gap: 6px; flex-wrap: wrap; }
    .tag {
      font-size: 0.75rem;
      font-weight: 600;
      color: var(--accent);
      background: var(--accent-light);
      padding: 3px 10px;
      border-radius: 99px;
    }
    .tag.gray {
      color: var(--gray-3);
      background: var(--gray-1);
    }

    /* ─── FOOTER ─── */
    footer {
      text-align: center;
      padding: 48px 24px;
      color: var(--gray-3);
      font-size: 0.85rem;
      border-top: 1px solid var(--border);
    }
    footer a { color: var(--accent); text-decoration: none; }

    /* ─── ANIMATIONS ─── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(28px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ─── RESPONSIVE ─── */
    @media (max-width: 640px) {
      .hero { flex-direction: column; gap: 28px; text-align: center; margin-bottom: 64px; }
      .hero-links { justify-content: center; }
      .hero-text p { margin: 0 auto 24px; }
      .nav-links { display: none; }
      .interests-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav id="nav">
    <a class="nav-logo" href="#">YN.</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#research">Research</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#publications">Publications</a></li>
    </ul>
  </nav>

  <main>

    <!-- HERO / ABOUT -->
    <div class="hero" id="about">
      <div class="hero-avatar">
        <!-- 프로필 사진이 있으면 아래 img 태그 사용 -->
        <!-- <img src="profile.jpg" alt="Profile" /> -->
        YN
      </div>
      <div class="hero-text">
        <p class="role">PhD Student · Computer Science</p>
        <h1>Your <span>Name</span></h1>
        <p>
          안녕하세요. 저는 ○○대학교에서 ○○을 연구하는 대학원생입니다.
          자연어처리와 머신러닝에 관심이 많으며, 인간과 AI의 상호작용을 탐구합니다.
        </p>
        <div class="hero-links">
          <a href="mailto:you@email.com" class="btn btn-primary">
            ✉ Email Me
          </a>
          <a href="https://github.com/yourid" target="_blank" class="btn btn-ghost">
            GitHub
          </a>
          <a href="cv.pdf" target="_blank" class="btn btn-ghost">
            CV / Resume
          </a>
          <a href="https://scholar.google.com" target="_blank" class="btn btn-ghost">
            Google Scholar
          </a>
        </div>
      </div>
    </div>

    <!-- RESEARCH INTERESTS -->
    <section id="research">
      <div class="section-label">Research Interests</div>
      <h2 class="section-title">무엇을 연구하나요</h2>
      <div class="interests-grid">
        <div class="interest-card">
          <div class="interest-icon">🧠</div>
          <h3>Natural Language Processing</h3>
          <p>대형 언어모델의 추론 능력 및 언어 이해 메커니즘 분석</p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">🤖</div>
          <h3>Human-AI Interaction</h3>
          <p>AI 시스템과 사용자 간의 신뢰 형성 및 협업 구조 연구</p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">📊</div>
          <h3>Machine Learning</h3>
          <p>적은 데이터로 일반화 성능을 높이는 학습 방법론 탐구</p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">🔍</div>
          <h3>Information Retrieval</h3>
          <p>신경망 기반 검색 시스템 및 문서 표현 학습 연구</p>
        </div>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education">
      <div class="section-label">Education</div>
      <h2 class="section-title">학력</h2>
      <div class="timeline">

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2023 — Present</div>
            <h3>Ph.D. in Computer Science</h3>
            <div class="sub">○○대학교 컴퓨터공학과</div>
            <p>지도교수: ○○○ 교수. 자연어처리 및 대규모 언어모델 연구.</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2021 — 2023</div>
            <h3>M.S. in Computer Science</h3>
            <div class="sub">○○대학교 컴퓨터공학과</div>
            <p>석사학위 논문: "○○○○을 위한 ○○○○ 연구"</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2017 — 2021</div>
            <h3>B.S. in Computer Science</h3>
            <div class="sub">○○대학교 소프트웨어학부</div>
            <p>학부 수석졸업. 우수논문상 수상.</p>
          </div>
        </div>

      </div>
    </section>

    <!-- EXPERIENCE -->
    <section id="experience">
      <div class="section-label">Experiences</div>
      <h2 class="section-title">경험</h2>
      <div class="timeline">

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2024 Summer</div>
            <h3>Research Intern</h3>
            <div class="sub">○○ AI Lab, ○○○</div>
            <p>대화형 AI 시스템의 안전성 평가 파이프라인 개발 및 연구 참여.</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2022 — 2023</div>
            <h3>Teaching Assistant</h3>
            <div class="sub">○○대학교 — 기계학습 개론</div>
            <p>학부생 대상 ML 기초 강의 보조 및 과제 채점, 튜터링 진행.</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-left">
            <div class="timeline-dot"></div>
            <div class="timeline-line"></div>
          </div>
          <div class="timeline-body">
            <div class="timeline-period">2021</div>
            <h3>Software Engineer Intern</h3>
            <div class="sub">○○ Tech</div>
            <p>백엔드 API 개발 및 데이터 파이프라인 최적화 작업 수행.</p>
          </div>
        </div>

      </div>
    </section>

    <!-- PUBLICATIONS -->
    <section id="publications">
      <div class="section-label">Publications</div>
      <h2 class="section-title">논문</h2>
      <div class="pub-list">

        <div class="pub-card">
          <span class="pub-year">2024</span>
          <div class="pub-content">
            <h3>Title of Your Most Recent Paper: A Study on Something Interesting</h3>
            <div class="pub-venue">Conference on Empirical Methods in Natural Language Processing (EMNLP)</div>
            <div class="pub-tags">
              <span class="tag">NLP</span>
              <span class="tag">LLM</span>
              <span class="tag gray">Oral</span>
            </div>
          </div>
        </div>

        <div class="pub-card">
          <span class="pub-year">2023</span>
          <div class="pub-content">
            <h3>Another Great Paper Title on Human-AI Collaboration</h3>
            <div class="pub-venue">Annual Conference of the Association for Computational Linguistics (ACL)</div>
            <div class="pub-tags">
              <span class="tag">Human-AI</span>
              <span class="tag">Dialogue</span>
            </div>
          </div>
        </div>

        <div class="pub-card">
          <span class="pub-year">2022</span>
          <div class="pub-content">
            <h3>Efficient Fine-tuning of Large Language Models for Domain Adaptation</h3>
            <div class="pub-venue">International Conference on Machine Learning (ICML)</div>
            <div class="pub-tags">
              <span class="tag">Fine-tuning</span>
              <span class="tag">Efficiency</span>
            </div>
          </div>
        </div>

      </div>
    </section>

  </main>

  <footer>
    <p>© 2025 Your Name · Built with ❤️ · <a href="https://github.com/yourid/yourid.github.io">GitHub</a></p>
  </footer>

  <script>
    // Nav scroll shadow
    const nav = document.getElementById('nav');
    window.addEventListener('scroll', () => {
      nav.classList.toggle('scrolled', window.scrollY > 10);
    });

    // Intersection Observer for scroll-in animations
    const sections = document.querySelectorAll('section');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.style.opacity = '1';
          e.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.08 });

    sections.forEach(s => {
      s.style.opacity = '0';
      s.style.transform = 'translateY(24px)';
      s.style.transition = 'opacity .7s ease, transform .7s ease';
      observer.observe(s);
    });
  </script>
</body>
</html>
