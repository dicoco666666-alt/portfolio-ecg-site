# portfolio-ecg-site
簡約黑白個人作品集網站，含心電圖圖片上傳與分析 demo
<!DOCTYPE html>
<html lang="zh-Hant">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Leo Portfolio</title>
    <meta
      name="description"
      content="個人作品集網站，簡約黑白風格，包含作品展示、聯絡表單與心電圖圖片分析功能。"
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header class="site-header">
      <div class="container nav-wrap">
        <a href="#top" class="brand">LEO</a>
        <button class="nav-toggle" aria-label="開啟選單">
          <span></span>
          <span></span>
          <span></span>
        </button>
        <nav class="nav">
          <a href="#about">關於我</a>
          <a href="#work">作品</a>
          <a href="#ecg">ECG 分析</a>
          <a href="#contact">聯絡</a>
        </nav>
      </div>
    </header>

    <main id="top">
      <section class="hero">
        <div class="container hero-wrap">
          <div class="hero-copy">
            <p class="eyebrow">Product Designer / Front-end Developer</p>
            <h1>我設計簡約、打造有感的數位體驗。</h1>
            <p class="lead">
              我專注於使用者介面設計、互動視覺與前端實作，將想法轉成簡潔、實用且有辨識度的產品。
            </p>
            <div class="cta-group">
              <a class="btn btn-primary" href="#work">查看作品</a>
              <a class="btn btn-secondary" href="#contact">聯絡我</a>
            </div>
            <div class="mini-stats">
              <div>
                <strong>5+</strong>
                <span>年經驗</span>
              </div>
              <div>
                <strong>28</strong>
                <span>完成專案</span>
              </div>
              <div>
                <strong>12</strong>
                <span>合作夥伴</span>
              </div>
            </div>
          </div>

          <div class="hero-card">
            <div class="profile-card">
              <div class="avatar">L</div>
              <div>
                <h3>Leo Wang</h3>
                <p>UI/UX Designer & Front-end Developer</p>
              </div>
            </div>

            <div class="project-preview">
              <div class="project-tag">最新專案</div>
              <h4>SmartCare Dashboard</h4>
              <div class="bars">
                <span style="height: 40%"></span>
                <span style="height: 58%"></span>
                <span style="height: 76%"></span>
                <span style="height: 66%"></span>
                <span style="height: 88%"></span>
                <span style="height: 72%"></span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="about" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">About</p>
            <h2>讓設計與技術保持一致</h2>
          </div>

          <div class="about-grid">
            <div class="about-card">
              <h3>設計能力</h3>
              <p>
                從品牌識別、頁面架構到互動細節，我重視視覺層次與資訊清晰度，打造符合目標受眾的使用體驗。
              </p>
            </div>
            <div class="about-card">
              <h3>前端實作</h3>
              <p>
                使用 HTML、CSS、JavaScript 與現代前端工具，將設計轉為高質量產品界面，並兼顧響應式與交互。
              </p>
            </div>
            <div class="about-card">
              <h3>協作方式</h3>
              <p>
                我善於與設計師、工程師與客戶溝通，釐清需求後快速迭代，讓專案價值最大化。
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="work" class="section muted">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Work</p>
            <h2>代表作品</h2>
          </div>

          <div class="work-grid">
            <article class="work-card">
              <div class="thumb dark"></div>
              <div class="card-body">
                <span class="tag">品牌網站</span>
                <h3>Nord Studio</h3>
                <p>為設計工作室打造的品牌網站，聚焦簡約美學與清晰的內容層級。</p>
              </div>
            </article>

            <article class="work-card">
              <div class="thumb light"></div>
              <div class="card-body">
                <span class="tag">SaaS</span>
                <h3>PulseBoard</h3>
                <p>數據儀表板系統，幫助管理者快速檢視 KPI 與業務狀態。</p>
              </div>
            </article>

            <article class="work-card">
              <div class="thumb dark-2"></div>
              <div class="card-body">
                <span class="tag">行動應用</span>
                <h3>Wellness App</h3>
                <p>健康追蹤 app，聚焦目標管理、睡眠紀錄與每日復盤。</p>
              </div>
            </article>
          </div>
        </div>
      </section>

      <section id="ecg" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">ECG Analyzer</p>
            <h2>心電圖圖片分析</h2>
          </div>

          <div class="ecg-panel">
            <div class="upload-box" id="dropZone">
              <input type="file" id="ecgImage" accept="image/*" hidden />
              <div class="upload-content">
                <div class="upload-icon">↑</div>
                <p>點擊或拖曳上傳心電圖圖片</p>
                <button type="button" class="btn btn-primary" id="triggerUpload">
                  選擇圖片
                </button>
              </div>
            </div>

            <div class="preview-box">
              <img
                id="imagePreview"
                src=""
                alt="心電圖預覽"
                style="display: none"
              />
              <div class="placeholder" id="previewPlaceholder">尚未上傳圖片</div>
            </div>
          </div>

          <div class="analysis-actions">
            <button type="button" class="btn btn-primary" id="analyzeBtn">
              分析心電圖
            </button>
          </div>

          <div class="result-card" id="analysisResult">
            <h3>分析結果</h3>
            <p>請先上傳心電圖圖片，然後點擊「分析心電圖」。</p>
          </div>
        </div>
      </section>

      <section id="contact" class="section contact-section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Contact</p>
            <h2>聯絡我</h2>
          </div>

          <form class="contact-form" id="contactForm">
            <div class="field-row">
              <label>
                姓名
                <input type="text" name="name" placeholder="請輸入您的姓名" required />
              </label>
              <label>
                電子郵件
                <input type="email" name="email" placeholder="請輸入電子郵件" required />
              </label>
            </div>

            <label>
              主旨
              <input type="text" name="subject" placeholder="例如：合作邀約、網站製作" required />
            </label>

            <label>
              訊息
              <textarea
                name="message"
                rows="6"
                placeholder="請簡單描述需求與期望..."
                required
              ></textarea>
            </label>

            <button type="submit" class="btn btn-primary">送出訊息</button>
          </form>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <div class="container footer-wrap">
        <p>© 2026 Leo Wang</p>
        <div class="socials">
          <a href="#">Behance</a>
          <a href="#">Dribbble</a>
          <a href="#">GitHub</a>
        </div>
      </div>
    </footer>

    <script src="script.js"></script>
  </body>
</html>