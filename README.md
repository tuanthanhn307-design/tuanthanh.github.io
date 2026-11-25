<!DOCTYPE html>
<html lang="vi" data-theme="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nguyễn Tuấn Thanh | 11T2 — Nhiếp ảnh, STEM &amp; Bóng chuyền</title>
  <meta name="description" content="Trang giới thiệu bản thân của Nguyễn Tuấn Thanh - Học sinh lớp 11T2, Trường THPT Chuyên Bến Tre tại Vĩnh Long. Đam mê Nhiếp ảnh, STEM, Thiết kế 3D &amp; Lập trình sáng tạo và Bóng chuyền (Chuyền 2)." />
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
      --accent-volley: #a78bfa;
      --accent-creative: #fb7185;
      --accent-charity: #34d399;
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
      --accent-volley: #7c3aed;
      --accent-creative: #e11d48;
      --accent-charity: #059669;
      --border-color: rgba(15, 23, 42, 0.12);
      --grid-color: rgba(2, 132, 199, 0.06);
      --shadow: 0 10px 25px rgba(15, 23, 42, 0.08);
    }

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
      gap: 18px;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-secondary);
      font-size: 0.9rem;
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

    .highlight-volley {
      color: var(--accent-volley);
    }

    .highlight-creative {
      color: var(--accent-creative);
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
      aspect-ratio: 4 / 4.5;
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
      object-position: center 22%;
      display: block;
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

    .info-value a {
      color: inherit;
      text-decoration: none;
    }

    .info-value a:hover {
      color: var(--accent-stem);
    }

    /* Skills & Gear Grids */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 24px;
    }

    .gear-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .skill-panel,
    .gear-card {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: 16px;
      padding: 26px;
      box-shadow: var(--shadow);
    }

    .skill-panel.stem {
      border-top: 3px solid var(--accent-stem);
    }

    .skill-panel.photo,
    .gear-card {
      border-top: 3px solid var(--accent-photo);
    }

    .skill-panel.volley {
      border-top: 3px solid var(--accent-volley);
    }

    .skill-panel.creative {
      border-top: 3px solid var(--accent-creative);
    }

    .gear-tag {
      display: inline-block;
      font-size: 0.75rem;
      padding: 3px 9px;
      border-radius: 6px;
      background: rgba(245, 158, 11, 0.14);
      color: var(--accent-photo);
      border: 1px solid rgba(245, 158, 11, 0.3);
      margin-bottom: 10px;
    }

    .gear-title {
      font-size: 1.2rem;
      font-weight: 700;
      margin-bottom: 6px;
    }

    .gear-lens {
      font-size: 0.92rem;
      color: var(--accent-stem);
      font-weight: 600;
      margin-bottom: 12px;
    }

    .panel-title {
      font-size: 1.2rem;
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
