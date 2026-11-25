<!DOCTYPE html>
<html lang="vi" data-theme="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nguyễn Tuấn Thanh | 11T2 — Nhiếp ảnh &amp; STEM</title>
  <meta name="description" content="Trang giới thiệu bản thân của Nguyễn Tuấn Thanh - Học sinh lớp 11T2, Trường THPT Chuyên Bến Tre tại Vĩnh Long. Đam mê Nhiếp ảnh và STEM." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --bg-primary: #0b0f17;
      --bg-secondary: #131a26;
      --bg-card: rgba(20, 28, 43, 0.85);
      --header-bg: rgba(11, 15, 23, 0.85);
      --text-primary: #f1f5f9;
      --text-secondary: #94a3b8;
      --accent-stem: #38bdf8;
      --accent-photo: #f59e0b;
      --border-color: rgba(148, 163, 184, 0.16);
      --grid-color: rgba(56, 189, 248, 0.05);
      --shadow: 0 12px 32px rgba(0, 0, 0, 0.35);
    }

    [data-theme="light"] {
      --bg-primary: #f8fafc;
      --bg-secondary: #ffffff;
      --bg-card: rgba(255, 255, 255, 0.95);
      --header-bg: rgba(248, 250, 252, 0.88);
      --text-primary: #0f172a;
      --text-secondary: #475569;
      --accent-stem: #0284c7;
      --accent-photo: #d97706;
      --border-color: rgba(15, 23, 42, 0.12);
      --grid-color: rgba(2, 132, 199, 0.06);
      --shadow: 0 10px 25px rgba(15, 23, 42, 0.08);
    }

    /* Đã sửa lỗi: đổi "- {" thành "* {" */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 84px;
      font-family: 'Inter', system-ui, -apple-system, sans-serif;
    }

    body {
      background-color: var(--bg-primary);
      color: var(--text-primary);
      line-height: 1.65;
      background-image:
        linear-gradient(to right, var(--grid-color) 1px, transparent 1px),
        linear-gradient(to bottom, var(--grid-color) 1px, transparent 1px);
      background-size: 36px 36px;
      transition: background-color 0.25s ease, color 0.25s ease;
    }

    .mono {
      font-family: 'JetBrains Mono', monospace;
    }

    .container {
      max-width: 1080px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Header & Mobile Menu */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      background: var(--header-bg);
      border-bottom: 1px solid var(--border-color);
    }

    .nav-wrapper {
      display: flex;
      justify-content: space-between;
      align-items: center;
      min-height: 68px;
      gap: 12px;
    }

    .logo {
      font-weight: 800;
      font-size: 1.15rem;
      letter-spacing: -0.02em;
      text-decoration: none;
      color: var(--text-primary);
      display: inline-flex;
      align-items: center;
      gap: 8px;
      white-space: nowrap;
    }

    .logo-badge {
      font-size: 0.72rem;
      padding: 2px 8px;
      border-radius: 6px;
      background: rgba(56, 189, 248, 0.14);
      color: var(--accent-stem);
      border: 1px solid rgba(56, 189, 248, 0.3);
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 18px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 20px;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-secondary);
      font-size: 0.92rem;
      font-weight: 500;
      transition: color 0.2s ease;
      white-space: nowrap;
    }

    .nav-links a:hover {
      color: var(--accent-stem);
    }

    .btn-icon {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      color: var(--text-primary);
      padding: 7px 12px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 0.85rem;
      font-weight: 600;
      transition: transform 0.2s ease, border-color 0.2s ease;
      white-space: nowrap;
    }

    .btn-icon:hover {
      border-color: var(--accent-stem);
      transform: translateY(-1px);
    }

    .menu-toggle {
      display: none;
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      color: var(--text-primary);
      padding: 7px 11px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
      line-height: 1;
    }

    .mobile-menu {
      display: none;
      flex-direction: column;
      padding: 12px 20px 18px;
      border-top: 1px solid var(--border-color);
      background: var(--header-bg);
      gap: 10px;
    }

    .mobile-menu.open {
      display: flex;
    }

    .mobile-menu a {
      text-decoration: none;
      color: var(--text-primary);
      padding: 8px 4px;
      font-weight: 500;
      border-bottom: 1px solid var(--border-color);
    }

    .mobile-menu a:last-child {
      border-bottom: none;
    }

    /* Hero Section */
    .hero {
      padding: 68px 0 52px;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 40px;
      align-items: center;
    }

    .status-pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      font-size: 0.8rem;
      padding: 6px 14px;
      border-radius: 999px;
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      color: var(--accent-stem);
      margin-bottom: 18px;
    }

    .dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--accent-photo);
      box-shadow: 0 0 8px var(--accent-photo);
      flex-shrink: 0;
    }

    h1 {
      font-size: clamp(2rem, 4.2vw, 3rem);
      font-weight: 800;
      line-height: 1.15;
      letter-spacing: -0.03em;
      margin-bottom: 16px;
    }

    .highlight-stem {
      color: var(--accent-stem);
    }

    .highlight-photo {
      color: var(--accent-photo);
    }

    .hero-desc {
      color: var(--text-secondary);
      font-size: 1.03rem;
      margin-bottom: 28px;
      max-width: 560px;
    }

    .cta-group {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 12px 20px;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.94rem;
      text-decoration: none;
      cursor: pointer;
      transition: all 0.2s ease;
      border: 1px solid transparent;
    }

    .btn-primary {
      background: var(--accent-stem);
      color: #08101c;
    }

    .btn-primary:hover {
      filter: brightness(1.08);
      transform: translateY(-2px);
    }

    .btn-outline {
      background: var(--bg-card);
      color: var(--text-primary);
      border-color: var(--border-color);
    }

    .btn-outline:hover {
      border-color: var(--accent-photo);
      transform: translateY(-2px);
    }

    /* Camera Viewfinder Card */
    .viewfinder {
      position: relative;
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: 18px;
      padding: 16px;
      box-shadow: var(--shadow);
    }

    .vf-header, .vf-footer {
      display: flex;
      justify-content: space-between;
      font-size: 0.75rem;
      color: var(--text-secondary);
      padding: 4px 6px;
    }

    .vf-rec {
      color: #ef4444;
      font-weight: 600;
    }

    .avatar-box {
      position: relative;
      width: 100%;
      aspect-ratio: 4 / 4.2;
      border-radius: 12px;
      overflow: hidden;
      margin: 8px 0;
      background: linear-gradient(135deg, #1e293b, #0f172a);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .avatar-box img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .avatar-placeholder {
      text-align: center;
      padding: 20px;
      color: #e2e8f0;
    }

    .crosshair {
      position: absolute;
      inset: 14px;
      border: 1px dashed rgba(245, 158, 11, 0.5);
      border-radius: 8px;
      pointer-events: none;
    }

    /* Sections */
    section {
      padding: 52px 0;
    }

    .section-header {
      margin-bottom: 28px;
    }

    .section-tag {
      font-size: 0.8rem;
      letter-spacing: 0.08em;
      color: var(--accent-stem);
      font-weight: 600;
      display: block;
      margin-bottom: 6px;
    }

    .section-title {
      font-size: 1.7rem;
      font-weight: 800;
      letter-spacing: -0.02em;
    }

    /* Info Strip */
    .info-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 16px;
    }

    .info-card {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      padding: 20px;
      border-radius: 14px;
      transition: transform 0.2s ease, border-color 0.2s ease;
    }

    .info-card:hover {
      transform: translateY(-3px);
      border-color: var(--accent-stem);
    }

    .info-label {
      font-size: 0.82rem;
      color: var(--text-secondary);
      margin-bottom: 4px;
    }

    .info-value {
      font-weight: 700;
      font-size: 1.05rem;
    }

    /* Skills Bento Grid */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .skill-panel {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: 16px;
      padding: 26px;
      box-shadow: var(--shadow);
    }

    .skill-panel.stem {
      border-top: 3px solid var(--accent-stem);
    }

    .skill-panel.photo {
      border-top: 3px solid var(--accent-photo);
    }

    .panel-title {
      font-size: 1.22rem;
      font-weight: 700;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .panel-desc {
      color: var(--text-secondary);
      font-size: 0.94rem;
    }

    .skill-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 16px;
    }

    .skill-list li {
      padding: 12px 14px;
      border-radius: 10px;
      background: rgba(148, 163, 184, 0.07);
      border: 1px solid var(--border-color);
      font-size: 0.93rem;
      color: var(--text-secondary);
    }

    .skill-list strong {
      display: block;
      color: var(--text-primary);
      margin-bottom: 2px;
    }

    /* Gallery */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
      gap: 20px;
    }

    .photo-card {
      position: relative;
      border-radius: 14px;
      overflow: hidden;
      background: var(--bg-secondary);
      border: 1px solid var(--border-color);
      aspect-ratio: 16 / 11;
    }

    .photo-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform 0.4s ease;
    }

    .photo-card:hover img {
      transform: scale(1.05);
    }

    .photo-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(9, 13, 22, 0.92), rgba(9, 13, 22, 0.15) 60%, transparent);
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: 18px;
      color: #f8fafc;
    }

    .photo-meta {
      font-size: 0.74rem;
      color: #fbbf24;
      margin-bottom: 3px;
    }

    .photo-caption {
      font-weight: 600;
      font-size: 0.98rem;
    }

    /* Contact Box */
    .contact-box {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: 18px;
      padding: 36px 28px;
      text-align: center;
      box-shadow: var(--shadow);
    }

    .contact-box p {
      color: var(--text-secondary);
      max-width: 540px;
      margin: 10px auto 24px;
    }

    .contact-actions {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 14px;
    }

    .copy-feedback {
      font-size: 0.85rem;
      color: var(--accent-stem);
      margin-top: 14px;
      min-height: 20px;
    }

    footer {
      border-top: 1px solid var(--border-color);
      padding: 28px 0;
      text-align: center;
      color: var(--text-secondary);
      font-size: 0.88rem;
    }

    @media (max-width: 820px) {
      .hero {
        grid-template-columns: 1fr;
        padding-top: 40px;
      }
      .nav-links {
        display: none;
      }
      .menu-toggle {
        display: inline-flex;
        align-items: center;
        justify-content: center;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="container nav-wrapper">
      <a href="#" class="logo">
        <span>NTT</span>
        <span class="logo-badge mono">11T2 // STEM &amp; PHOTO</span>
      </a>

      <div class="nav-right">
        <nav class="nav-links" aria-label="Điều hướng chính">
          <a href="#gioi-thieu">Giới thiệu</a>
          <a href="#ky-nang">Kỹ năng</a>
          <a href="#bo-suu-tap">Góc Nhiếp ảnh</a>
          <a href="#lien-he">Liên hệ</a>
        </nav>
        <button type="button" class="btn-icon" id="themeToggle" aria-label="Đổi giao diện Sáng hoặc Tối">☀️ Sáng</button>
        <button type="button" class="menu-toggle" id="menuToggle" aria-label="Mở menu điều hướng" aria-expanded="false">☰</button>
      </div>
    </div>

    <!-- Mobile Navigation Drawer -->
    <nav class="mobile-menu" id="mobileMenu" aria-label="Điều hướng điện thoại">
      <a href="#gioi-thieu">Giới thiệu</a>
      <a href="#ky-nang">Kỹ năng STEM &amp; Nhiếp ảnh</a>
      <a href="#bo-suu-tap">Góc Nhiếp ảnh</a>
      <a href="#lien-he">Liên hệ</a>
    </nav>
  </header>

  <main class="container">
    <!-- Hero Section -->
    <section class="hero">
      <div>
        <div class="status-pill mono">
          <span class="dot"></span>
          <span>Lớp 11T2 • THPT Chuyên Bến Tre (Vĩnh Long)</span>
        </div>
        <h1>
          Xin chào, mình là <br />
          <span class="highlight-stem">Nguyễn Tuấn Thanh</span>
        </h1>
        <p class="hero-desc">
          Mình là học sinh lớp <strong>11T2</strong> tại trường <strong>THPT Chuyên Bến Tre (tỉnh Vĩnh Long)</strong>. Mình yêu thích kết hợp tư duy logic của <span class="highlight-stem"><strong>STEM</strong></span> với góc nhìn sáng tạo qua ống kính <span class="highlight-photo"><strong>Nhiếp ảnh</strong></span>.
        </p>
        <div class="cta-group">
          <a href="#ky-nang" class="btn btn-primary">Khám phá kỹ năng</a>
          <a href="#bo-suu-tap" class="btn btn-outline">Xem góc nhiếp ảnh</a>
        </div>
      </div>

      <!-- Viewfinder Portrait Frame -->
      <div class="viewfinder">
        <div class="vf-header mono">
          <span class="vf-rec">● REC</span>
          <span>[ AF-C • RAW ]</span>
          <span>100%</span>
        </div>
        <div class="avatar-box">
          <img
            id="avatarImg"
            src="images/anh-ca-nhan.jpg"
            alt="Chân dung Nguyễn Tuấn Thanh"
          />
          <div class="avatar-placeholder" id="avatarPlaceholder">
            <p class="mono" style="font-size: 2rem; margin-bottom: 8px;">📷</p>
            <strong>Ảnh chân dung của bạn</strong>
            <p style="font-size: 0.84rem; margin-top: 6px; color: #cbd5e1;">
              Tải ảnh lên <code class="mono">images/anh-ca-nhan.jpg</code> trên GitHub để hiển thị tại đây.
            </p>
          </div>
          <div class="crosshair"></div>
        </div>
        <div class="vf-footer mono">
          <span>ISO 100</span>
          <span>f/1.8</span>
          <span>1/500s</span>
        </div>
      </div>
    </section>

    <!-- About & Academic Info -->
    <section id="gioi-thieu">
      <div class="section-header">
        <span class="section-tag mono">// 01. HỒ SƠ CÁ NHÂN</span>
        <h2 class="section-title">Thông tin cơ bản</h2>
      </div>
      <div class="info-grid">
        <div class="info-card">
          <div class="info-label">Họ và tên</div>
          <div class="info-value">Nguyễn Tuấn Thanh</div>
        </div>
        <div class="info-card">
          <div class="info-label">Lớp</div>
          <div class="info-value">11T2</div>
        </div>
        <div class="info-card">
          <div class="info-label">Trường học</div>
          <div class="info-value">THPT Chuyên Bến Tre</div>
        </div>
        <div class="info-card">
          <div class="info-label">Địa phương</div>
          <div class="info-value">Tỉnh Vĩnh Long</div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="ky-nang">
      <div class="section-header">
        <span class="section-tag mono">// 02. NĂNG LỰC &amp; ĐAM MÊ</span>
        <h2 class="section-title">Kỹ năng STEM &amp; Nhiếp ảnh</h2>
      </div>
      <div class="skills-grid">
        <!-- STEM Card -->
        <div class="skill-panel stem">
          <div class="panel-title">
            <span>⚙️</span>
            <span>Kỹ năng STEM &amp; Kỹ thuật</span>
          </div>
          <p class="panel-desc">
            Vận dụng kiến thức Khoa học, Công nghệ, Kỹ thuật và Toán học để xây dựng ý tưởng và giải quyết vấn đề thực tế.
          </p>
          <ul class="skill-list">
            <li>
              <strong>Tư duy Logic &amp; Giải quyết vấn đề</strong>
              Phân tích bài toán, thử nghiệm giả thuyết và tối ưu quy trình làm việc.
            </li>
            <li>
              <strong>Điện tử &amp; Lập trình cơ bản</strong>
              Làm quen với mạch điện, cảm biến, vi điều khiển và tư duy lập trình.
            </li>
            <li>
              <strong>Thiết kế &amp; Thực nghiệm mô hình</strong>
              Lên bản vẽ ý tưởng, lắp ráp và kiểm thử các sản phẩm STEM học đường.
            </li>
          </ul>
        </div>

        <!-- Photography Card -->
        <div class="skill-panel photo">
          <div class="panel-title">
            <span>📸</span>
            <span>Kỹ năng Nhiếp ảnh</span>
          </div>
          <p class="panel-desc">
            Ghi lại những khoảnh khắc đời sống, thiên nhiên và góc nhìn nghệ thuật thông qua ánh sáng và bố cục.
          </p>
          <ul class="skill-list">
            <li>
              <strong>Bố cục &amp; Ánh sáng</strong>
              Áp dụng tỷ lệ khung hình, đường dẫn và tận dụng ánh sáng tự nhiên hiệu quả.
            </li>
            <li>
              <strong>Chụp ảnh Đời sống &amp; Phong cảnh</strong>
              Lưu giữ hình ảnh trường lớp, hoạt động tập thể và cảnh sắc quê hương.
            </li>
            <li>
              <strong>Hậu kỳ &amp; Chỉnh màu</strong>
              Cân chỉnh độ sáng, tương phản và màu sắc để bức ảnh hài hòa, có chiều sâu.
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Gallery Section -->
    <section id="bo-suu-tap">
      <div class="section-header">
        <span class="section-tag mono">// 03. GÓC LƯU TRỮ</span>
        <h2 class="section-title">Khoảnh khắc Nhiếp ảnh &amp; STEM</h2>
      </div>
      <div class="gallery-grid">
        <div class="photo-card">
          <img src="https://images.unsplash.com/photo-1516035069371-29a1b244cc32?auto=format&fit=crop&w=800&q=80" alt="Góc máy nhiếp ảnh" />
          <div class="photo-overlay">
            <span class="photo-meta mono">PHOTOGRAPHY • 35MM f/1.8</span>
            <div class="photo-caption">Góc nhìn qua ống kính</div>
          </div>
        </div>
        <div class="photo-card">
          <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=800&q=80" alt="Mạch điện tử STEM" />
          <div class="photo-overlay">
            <span class="photo-meta mono">STEM LAB • HARDWARE</span>
            <div class="photo-caption">Khám phá mạch điện tử &amp; công nghệ</div>
          </div>
        </div>
        <div class="photo-card">
          <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80" alt="Ánh sáng hoàng hôn" />
          <div class="photo-overlay">
            <span class="photo-meta mono">GOLDEN HOUR • ISO 100</span>
            <div class="photo-caption">Sắc màu ánh sáng tự nhiên</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="lien-he">
      <div class="contact-box">
        <span class="section-tag mono">// 04. KẾT NỐI</span>
        <h2 class="section-title">Cùng giao lưu về Nhiếp ảnh &amp; STEM</h2>
        <p>
          Bạn có thể sao chép nhanh thông tin giới thiệu của mình hoặc ghé thăm GitHub để cùng trao đổi, chia sẻ ý tưởng nhé!
        </p>
        <div class="contact-actions">
          <button type="button" class="btn btn-primary" id="copyInfoBtn">📋 Sao chép thông tin giới thiệu</button>
          <a href="https://github.com/" target="_blank" rel="noopener noreferrer" class="btn btn-outline">💻 GitHub cá nhân</a>
        </div>
        <div class="copy-feedback mono" id="copyFeedback" role="status" aria-live="polite"></div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <p>© 2026 <strong>Nguyễn Tuấn Thanh</strong> — Lớp 11T2, Trường THPT Chuyên Bến Tre (Vĩnh Long).</p>
    </div>
  </footer>

  <script>
    // Xử lý hiển thị ảnh chân dung hoặc khung placeholder nếu ảnh chưa tồn tại
    const avatarImg = document.getElementById('avatarImg');
    const avatarPlaceholder = document.getElementById('avatarPlaceholder');

    function syncAvatarState() {
      if (avatarImg.complete && avatarImg.naturalWidth > 0) {
        avatarImg.style.display = 'block';
        avatarPlaceholder.style.display = 'none';
      } else {
        avatarImg.style.display = 'none';
        avatarPlaceholder.style.display = 'block';
      }
    }

    avatarImg.addEventListener('load', syncAvatarState);
    avatarImg.addEventListener('error', syncAvatarState);
    syncAvatarState();

    // Chuyển đổi chế độ Sáng / Tối
    const themeToggle = document.getElementById('themeToggle');
    const htmlEl = document.documentElement;

    themeToggle.addEventListener('click', () => {
      const isDark = htmlEl.getAttribute('data-theme') === 'dark';
      const nextTheme = isDark ? 'light' : 'dark';
      htmlEl.setAttribute('data-theme', nextTheme);
      themeToggle.textContent = nextTheme === 'dark' ? '☀️ Sáng' : '🌙 Tối';
    });

    // Mở / đóng menu trên điện thoại
    const menuToggle = document.getElementById('menuToggle');
    const mobileMenu = document.getElementById('mobileMenu');

    function closeMobileMenu() {
      mobileMenu.classList.remove('open');
      menuToggle.setAttribute('aria-expanded', 'false');
      menuToggle.textContent = '☰';
    }

    menuToggle.addEventListener('click', () => {
      const isOpen = mobileMenu.classList.toggle('open');
      menuToggle.setAttribute('aria-expanded', String(isOpen));
      menuToggle.textContent = isOpen ? '✕' : '☰';
    });

    mobileMenu.querySelectorAll('a').forEach((link) => {
      link.addEventListener('click', closeMobileMenu);
    });

    window.addEventListener('resize', () => {
      if (window.innerWidth > 820) {
        closeMobileMenu();
      }
    });

    // Sao chép thông tin giới thiệu (có cơ chế dự phòng nếu clipboard bị chặn)
    const copyBtn = document.getElementById('copyInfoBtn');
    const feedback = document.getElementById('copyFeedback');
    const bioText = 'Nguyễn Tuấn Thanh - Học sinh lớp 11T2, Trường THPT Chuyên Bến Tre (tỉnh Vĩnh Long). Đam mê Nhiếp ảnh & STEM.';

    function showCopiedMessage() {
      feedback.textContent = '✓ Đã sao chép thông tin vào bộ nhớ tạm!';
      clearTimeout(showCopiedMessage.timer);
      showCopiedMessage.timer = setTimeout(() => {
        feedback.textContent = '';
      }, 3000);
    }

    copyBtn.addEventListener('click', async () => {
      try {
        if (navigator.clipboard && window.isSecureContext) {
          await navigator.clipboard.writeText(bioText);
        } else {
          const tempInput = document.createElement('textarea');
          tempInput.value = bioText;
          tempInput.setAttribute('readonly', '');
          tempInput.style.position = 'absolute';
          tempInput.style.left = '-9999px';
          document.body.appendChild(tempInput);
          tempInput.select();
          document.execCommand('copy');
          document.body.removeChild(tempInput);
        }
        showCopiedMessage();
      } catch (err) {
        feedback.textContent = 'Không thể tự động sao chép, bạn hãy bôi đen và copy thủ công nhé.';
      }
    });
  </script>
</body>
</html>
