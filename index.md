<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shilpa Angadi | Protocol Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #f8fafc;
      --card: #ffffff;
      --border: #e2e8f0;
      --text: #0f172a;
      --dim: #64748b;
      --accent: #2563eb;
      --accent-light: #3b82f6;
      --green: #059669;
      --orange: #ea580c;
      --code-bg: #f1f5f9;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'JetBrains Mono', monospace;
      background: 
        radial-gradient(ellipse at 20% 0%, rgba(37, 99, 235, 0.06) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 100%, rgba(5, 150, 105, 0.06) 0%, transparent 50%),
        radial-gradient(ellipse at 50% 50%, rgba(37, 99, 235, 0.02) 0%, transparent 70%),
        linear-gradient(180deg, #f8fafc 0%, #f1f5f9 50%, #e2e8f0 100%);
      background-attachment: fixed;
      color: var(--text);
      font-size: 13px;
      line-height: 1.7;
      min-height: 100vh;
    }

    /* Subtle grid pattern */
    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        linear-gradient(rgba(37, 99, 235, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(37, 99, 235, 0.03) 1px, transparent 1px);
      background-size: 60px 60px;
      pointer-events: none;
      z-index: -1;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 60px 24px;
      position: relative;
    }

    /* Header */
    .header {
      text-align: center;
      margin-bottom: 50px;
      animation: fadeInDown 0.8s ease;
    }

    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes scaleIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes slideInLeft {
      from { opacity: 0; transform: translateX(-30px); }
      to { opacity: 1; transform: translateX(0); }
    }

    @keyframes slideInRight {
      from { opacity: 0; transform: translateX(30px); }
      to { opacity: 1; transform: translateX(0); }
    }

    .avatar {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      background: linear-gradient(135deg, #2563eb, #059669);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 20px;
      animation: float 3s ease-in-out infinite, pulse 2s ease-in-out infinite;
      box-shadow: 0 10px 40px rgba(37, 99, 235, 0.25);
      position: relative;
    }

    .avatar svg {
      width: 48px;
      height: 48px;
      fill: white;
    }

    .avatar::after {
      content: '';
      position: absolute;
      width: 120%;
      height: 120%;
      border-radius: 50%;
      border: 2px dashed rgba(37, 99, 235, 0.2);
      animation: spin 20s linear infinite;
    }

    @keyframes spin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }

    @keyframes pulse {
      0%, 100% { box-shadow: 0 10px 40px rgba(37, 99, 235, 0.25); }
      50% { box-shadow: 0 10px 60px rgba(37, 99, 235, 0.4); }
    }

    .name {
      font-size: 28px;
      font-weight: 700;
      margin-bottom: 8px;
      animation: fadeIn 1s ease 0.3s both;
      background: linear-gradient(135deg, var(--text), var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .tagline {
      color: var(--dim);
      margin-bottom: 16px;
    }

    .rotating-text {
      display: inline-block;
      position: relative;
      height: 1.5em;
      overflow: hidden;
      vertical-align: bottom;
    }

    .rotate-item {
      display: block;
      animation: rotateText 10s infinite;
      opacity: 0;
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      white-space: nowrap;
    }

    .rotate-item:nth-child(1) { animation-delay: 0s; }
    .rotate-item:nth-child(2) { animation-delay: 2s; }
    .rotate-item:nth-child(3) { animation-delay: 4s; }
    .rotate-item:nth-child(4) { animation-delay: 6s; }
    .rotate-item:nth-child(5) { animation-delay: 8s; }

    @keyframes rotateText {
      0%, 16% { 
        opacity: 0; 
        transform: translateX(-50%) translateY(20px);
      }
      2%, 14% { 
        opacity: 1; 
        transform: translateX(-50%) translateY(0);
      }
      16%, 100% { 
        opacity: 0; 
        transform: translateX(-50%) translateY(-20px);
      }
    }

    @keyframes blink {
      50% { opacity: 0.4; }
    }

    .bio {
      color: var(--dim);
      margin-top: 16px;
      max-width: 580px;
      margin-left: auto;
      margin-right: auto;
      animation: fadeIn 1s ease 0.5s both;
    }

    .links {
      display: flex;
      justify-content: center;
      gap: 16px;
      margin-top: 20px;
      animation: fadeInUp 0.8s ease 0.6s both;
    }

    .links a {
      color: var(--dim);
      text-decoration: none;
      padding: 10px 20px;
      border: 1px solid var(--border);
      border-radius: 8px;
      transition: all 0.3s;
      background: var(--card);
      box-shadow: 0 2px 8px rgba(0,0,0,0.04);
    }

    .links a:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-3px);
      box-shadow: 0 8px 25px rgba(37, 99, 235, 0.15);
    }

    /* Ethics Banner */
    .ethics-banner {
      background: linear-gradient(135deg, rgba(5, 150, 105, 0.05), rgba(5, 150, 105, 0.1));
      border: 2px solid var(--green);
      border-radius: 16px;
      padding: 24px 28px;
      margin-bottom: 40px;
      animation: slideInLeft 0.8s ease 0.2s both;
      position: relative;
      overflow: hidden;
    }

    .ethics-banner::before {
      content: '';
      position: absolute;
      top: -50%;
      right: -50%;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle, rgba(5, 150, 105, 0.1) 0%, transparent 70%);
      pointer-events: none;
    }

    .ethics-title {
      font-weight: 700;
      color: var(--green);
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 14px;
    }

    .ethics-title svg {
      width: 20px;
      height: 20px;
      fill: var(--green);
    }

    .ethics-text {
      color: var(--dim);
      font-size: 12px;
      line-height: 1.8;
      position: relative;
    }

    .ethics-text strong {
      color: var(--text);
    }

    /* Stats Bar */
    .stats-bar {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
      margin-bottom: 40px;
    }

    .stat-item {
      text-align: center;
      padding: 24px 16px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      transition: all 0.3s;
      animation: scaleIn 0.6s ease both;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
      position: relative;
      overflow: hidden;
    }

    .stat-item::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--green));
      opacity: 0;
      transition: opacity 0.3s;
    }

    .stat-item:hover::before {
      opacity: 1;
    }

    .stat-item:nth-child(1) { animation-delay: 0.1s; }
    .stat-item:nth-child(2) { animation-delay: 0.2s; }
    .stat-item:nth-child(3) { animation-delay: 0.3s; }
    .stat-item:nth-child(4) { animation-delay: 0.4s; }

    .stat-item:hover {
      transform: translateY(-6px) scale(1.02);
      box-shadow: 0 20px 50px rgba(0,0,0,0.1);
      border-color: var(--accent);
    }

    .stat-num {
      font-size: 26px;
      font-weight: 700;
      background: linear-gradient(135deg, var(--accent), var(--green));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .stat-label {
      font-size: 11px;
      color: var(--dim);
      margin-top: 6px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    /* Terminal Block */
    .terminal {
      background: linear-gradient(135deg, #1e293b, #0f172a);
      border-radius: 16px;
      overflow: hidden;
      margin-bottom: 40px;
      animation: slideInLeft 0.8s ease 0.3s both;
      transition: transform 0.3s, box-shadow 0.3s;
      box-shadow: 0 10px 40px rgba(0,0,0,0.15);
    }

    .terminal:hover {
      transform: translateY(-4px);
      box-shadow: 0 25px 60px rgba(0,0,0,0.25);
    }

    .terminal-header {
      background: rgba(255,255,255,0.05);
      padding: 14px 18px;
      display: flex;
      gap: 8px;
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .terminal-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      animation: dotPulse 2s ease-in-out infinite;
    }

    .terminal-dot.red { background: #ff5f56; animation-delay: 0s; }
    .terminal-dot.yellow { background: #ffbd2e; animation-delay: 0.2s; }
    .terminal-dot.green { background: #27ca40; animation-delay: 0.4s; }

    @keyframes dotPulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.6; transform: scale(0.95); }
    }

    .terminal-body {
      padding: 24px;
      color: #e2e8f0;
      font-size: 12px;
    }

    .terminal-line {
      margin-bottom: 10px;
      animation: typeIn 0.5s ease both;
    }

    .terminal-line:nth-child(1) { animation-delay: 0.5s; }
    .terminal-line:nth-child(2) { animation-delay: 0.7s; }
    .terminal-line:nth-child(3) { animation-delay: 0.9s; }
    .terminal-line:nth-child(4) { animation-delay: 1.1s; }
    .terminal-line:nth-child(5) { animation-delay: 1.3s; }
    .terminal-line:nth-child(6) { animation-delay: 1.5s; }
    .terminal-line:nth-child(7) { animation-delay: 1.7s; }

    @keyframes typeIn {
      from { opacity: 0; transform: translateX(-10px); }
      to { opacity: 1; transform: translateX(0); }
    }

    .terminal-prompt { color: #4ade80; }
    .terminal-cmd { color: #fff; }
    .terminal-output { color: #94a3b8; }
    .terminal-highlight { color: #fbbf24; font-weight: 500; }

    /* Section */
    h2 {
      font-size: 15px;
      font-weight: 600;
      margin-bottom: 24px;
      display: flex;
      align-items: center;
      gap: 12px;
      animation: fadeIn 0.6s ease both;
    }

    h2::before {
      content: '';
      width: 4px;
      height: 20px;
      background: linear-gradient(180deg, var(--accent), var(--green));
      border-radius: 2px;
    }

    /* Project Cards */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      margin-bottom: 40px;
    }

    .project-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      animation: fadeInUp 0.6s ease both;
      position: relative;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .project-card:nth-child(1) { animation-delay: 0.1s; }
    .project-card:nth-child(2) { animation-delay: 0.15s; }
    .project-card:nth-child(3) { animation-delay: 0.2s; }
    .project-card:nth-child(4) { animation-delay: 0.25s; }
    .project-card:nth-child(5) { animation-delay: 0.3s; }
    .project-card:nth-child(6) { animation-delay: 0.35s; }
    .project-card:nth-child(7) { animation-delay: 0.4s; }
    .project-card:nth-child(8) { animation-delay: 0.45s; }

    .project-card:hover {
      transform: translateY(-8px) scale(1.01);
      box-shadow: 0 25px 60px rgba(0,0,0,0.12);
      border-color: var(--accent);
    }

    .project-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: linear-gradient(90deg, var(--accent), var(--green));
      transform: scaleX(0);
      transition: transform 0.4s;
      transform-origin: left;
    }

    .project-card:hover::before {
      transform: scaleX(1);
    }

    .project-icon {
      width: 48px;
      height: 48px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 18px;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .project-icon svg {
      width: 24px;
      height: 24px;
      fill: white;
    }

    .project-card:hover .project-icon {
      transform: scale(1.1) rotate(5deg);
      box-shadow: 0 8px 20px rgba(0,0,0,0.15);
    }

    .project-icon.sol { 
      background: linear-gradient(135deg, #9945FF, #14F195); 
      box-shadow: 0 4px 15px rgba(153, 69, 255, 0.3);
    }
    .project-icon.eth { 
      background: linear-gradient(135deg, #627eea, #8b9cf6); 
      box-shadow: 0 4px 15px rgba(98, 126, 234, 0.3);
    }
    .project-icon.data { 
      background: linear-gradient(135deg, #f59e0b, #ef4444); 
      box-shadow: 0 4px 15px rgba(245, 158, 11, 0.3);
    }
    .project-icon.tools { 
      background: linear-gradient(135deg, #06b6d4, #3b82f6); 
      box-shadow: 0 4px 15px rgba(6, 182, 212, 0.3);
    }

    .project-title {
      font-size: 15px;
      font-weight: 600;
      margin-bottom: 8px;
    }

    .project-chain {
      display: inline-block;
      font-size: 10px;
      padding: 4px 10px;
      background: linear-gradient(135deg, var(--code-bg), #e2e8f0);
      border-radius: 6px;
      color: var(--dim);
      margin-bottom: 14px;
      font-weight: 500;
    }

    .project-desc {
      color: var(--dim);
      font-size: 12px;
      margin-bottom: 18px;
      line-height: 1.8;
    }

    .project-metrics {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      font-size: 11px;
    }

    .metric {
      color: var(--green);
      font-weight: 600;
      padding: 4px 10px;
      background: rgba(5, 150, 105, 0.08);
      border-radius: 6px;
    }

    /* Why Me Section */
    .why-me {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 32px;
      margin-bottom: 40px;
      animation: fadeInUp 0.8s ease 0.3s both;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .why-me h3 {
      font-size: 14px;
      margin-bottom: 16px;
    }

    .why-list {
      list-style: none;
    }

    .why-list li {
      padding: 12px 0;
      border-bottom: 1px solid var(--border);
      color: var(--dim);
      font-size: 12px;
      display: flex;
      align-items: flex-start;
      gap: 12px;
    }

    .why-list li:last-child {
      border-bottom: none;
    }

    .why-list li::before {
      content: '→';
      color: var(--accent);
      font-weight: bold;
      flex-shrink: 0;
    }

    .why-list li strong {
      color: var(--text);
    }

    /* Skills Section */
    .skills-visual {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-bottom: 40px;
    }

    .skill-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px;
      text-align: center;
      transition: all 0.4s;
      animation: scaleIn 0.6s ease both;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
      position: relative;
      overflow: hidden;
    }

    .skill-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--green));
      opacity: 0;
      transition: opacity 0.3s;
    }

    .skill-card:hover::before {
      opacity: 1;
    }

    .skill-card:nth-child(1) { animation-delay: 0.1s; }
    .skill-card:nth-child(2) { animation-delay: 0.2s; }
    .skill-card:nth-child(3) { animation-delay: 0.3s; }

    .skill-card:hover {
      transform: translateY(-6px) scale(1.02);
      border-color: var(--accent);
      box-shadow: 0 20px 50px rgba(0,0,0,0.08);
    }

    .skill-icon-wrap {
      width: 60px;
      height: 60px;
      margin: 0 auto 16px;
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      animation: bounce 2s ease-in-out infinite;
    }

    .skill-icon-wrap svg {
      width: 32px;
      height: 32px;
      fill: white;
    }

    .skill-card:nth-child(1) .skill-icon-wrap { 
      background: linear-gradient(135deg, var(--accent), #60a5fa);
      box-shadow: 0 6px 20px rgba(37, 99, 235, 0.3);
      animation-delay: 0s; 
    }
    .skill-card:nth-child(2) .skill-icon-wrap { 
      background: linear-gradient(135deg, #9945FF, #14F195);
      box-shadow: 0 6px 20px rgba(153, 69, 255, 0.3);
      animation-delay: 0.3s; 
    }
    .skill-card:nth-child(3) .skill-icon-wrap { 
      background: linear-gradient(135deg, var(--green), #34d399);
      box-shadow: 0 6px 20px rgba(5, 150, 105, 0.3);
      animation-delay: 0.6s; 
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }

    .skill-title {
      font-weight: 600;
      margin-bottom: 10px;
      font-size: 14px;
    }

    .skill-list {
      color: var(--dim);
      font-size: 11px;
      line-height: 1.8;
    }

    /* Code Block */
    .code-block {
      background: linear-gradient(135deg, #1e293b, #0f172a);
      border-radius: 16px;
      padding: 24px;
      margin-bottom: 40px;
      overflow-x: auto;
      font-size: 12px;
      animation: fadeIn 0.8s ease 0.3s both;
      transition: transform 0.3s, box-shadow 0.3s;
      box-shadow: 0 10px 40px rgba(0,0,0,0.15);
      color: #e2e8f0;
    }

    .code-block:hover {
      transform: translateY(-2px);
      box-shadow: 0 15px 50px rgba(0,0,0,0.2);
    }

    .code-comment { color: #64748b; }
    .code-keyword { color: #c084fc; }
    .code-string { color: #4ade80; }
    .code-func { color: #60a5fa; }

    /* CTA */
    .cta {
      text-align: center;
      padding: 56px 40px;
      background: linear-gradient(135deg, rgba(37, 99, 235, 0.05), rgba(5, 150, 105, 0.05));
      border-radius: 20px;
      border: 1px solid var(--border);
      animation: fadeInUp 0.8s ease 0.4s both;
      position: relative;
      overflow: hidden;
    }

    .cta::before {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 200px;
      height: 200px;
      background: radial-gradient(circle, rgba(37, 99, 235, 0.1) 0%, transparent 70%);
      pointer-events: none;
    }

    .cta h3 {
      font-size: 22px;
      margin-bottom: 12px;
      position: relative;
    }

    .cta p {
      color: var(--dim);
      margin-bottom: 28px;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
      position: relative;
    }

    .cta-btn {
      display: inline-block;
      background: linear-gradient(135deg, var(--accent), var(--accent-light));
      color: #fff;
      padding: 16px 40px;
      border-radius: 12px;
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s;
      box-shadow: 0 8px 25px rgba(37, 99, 235, 0.3);
      position: relative;
    }

    .cta-btn:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 15px 40px rgba(37, 99, 235, 0.4);
    }

    /* Footer */
    footer {
      text-align: center;
      margin-top: 60px;
      padding-top: 24px;
      border-top: 1px solid var(--border);
      color: var(--dim);
      font-size: 11px;
      animation: fadeIn 1s ease 0.5s both;
    }

    /* Responsive */
    @media (max-width: 700px) {
      .stats-bar { grid-template-columns: repeat(2, 1fr); }
      .projects-grid { grid-template-columns: 1fr; }
      .skills-visual { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<div class="container">

  <!-- Header -->
  <header class="header">
    <div class="avatar">
      <svg viewBox="0 0 24 24"><path d="M12 1.5l-8 13.1L12 18.7l8-4.1L12 1.5zm0 18.4l-8-4.9L12 22.5l8-7.5-8 4.9z"/></svg>
    </div>
    <h1 class="name">Shilpa Angadi</h1>
    <p class="tagline">
      <span class="rotating-text">
        <span class="rotate-item">building the onchain future</span>
        <span class="rotate-item">shipping secure smart contracts</span>
        <span class="rotate-item">analyzing MEV & on-chain data</span>
        <span class="rotate-item">solidity · rust · anchor</span>
        <span class="rotate-item">0 exploits, 52 contracts</span>
      </span>
    </p>
    <p class="bio">
      10 years in data science. Now I ship smart contracts, build protocols, and analyze on-chain data. 
      Solidity, Rust, Solana, EVM. I read code. I build things that work.
    </p>
    <div class="links">
      <a href="https://github.com/RavikiranShilpa">GitHub</a>
      <a href="https://www.linkedin.com/in/shilpa-443b3516b/">LinkedIn</a>
      <a href="https://dune.com/">Dune</a>
      <a href="mailto:shilpa@example.com">Email</a>
    </div>
  </header>

  <!-- Ethics Banner -->
  <div class="ethics-banner">
    <div class="ethics-title">
      <svg viewBox="0 0 24 24"><path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.79-7 8.94V12H5V6.3l7-3.11v8.8z"/></svg>
      Ethics Matter
    </div>
    <div class="ethics-text">
      <strong>No rugs. No scams. No shady tokenomics.</strong> I've turned down projects with sketchy vesting, hidden mints, and "temporary" admin keys. 
      I believe crypto wins when we build things people can actually trust. Security audits aren't optional. Transparency isn't marketing—it's the baseline. 
      If your project needs to hide how it works, I'm not your dev.
    </div>
  </div>


  <!-- Stats -->
  <div class="stats-bar">
    <div class="stat-item">
      <div class="stat-num">$8.2M</div>
      <div class="stat-label">TVL Secured</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">52</div>
      <div class="stat-label">Contracts Shipped</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">6</div>
      <div class="stat-label">Chains</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">0</div>
      <div class="stat-label">Exploits</div>
    </div>
  </div>

  <!-- Terminal -->
  <div class="terminal">
    <div class="terminal-header">
      <div class="terminal-dot red"></div>
      <div class="terminal-dot yellow"></div>
      <div class="terminal-dot green"></div>
    </div>
    <div class="terminal-body">
      <div class="terminal-line">
        <span class="terminal-prompt">shilpa@crypto</span>:<span class="terminal-cmd">~$ whoami</span>
      </div>
      <div class="terminal-line terminal-output">
        protocol engineer | on-chain analyst | 10yr data background
      </div>
      <div class="terminal-line">
        <span class="terminal-prompt">shilpa@crypto</span>:<span class="terminal-cmd">~$ cat skills.txt</span>
      </div>
      <div class="terminal-line terminal-output">
        <span class="terminal-highlight">Solidity</span> · <span class="terminal-highlight">Rust</span> · <span class="terminal-highlight">Anchor</span> · Foundry · Yul · Python · Dune
      </div>
      <div class="terminal-line">
        <span class="terminal-prompt">shilpa@crypto</span>:<span class="terminal-cmd">~$ echo $PRINCIPLES</span>
      </div>
      <div class="terminal-line terminal-output">
        audit everything · no backdoors · users first · ship it right
      </div>
      <div class="terminal-line">
        <span class="terminal-prompt">shilpa@crypto</span>:<span class="terminal-cmd">~$ _</span>
      </div>
    </div>
  </div>

  <!-- Projects -->
  <h2>What I've Built</h2>
  <div class="projects-grid">

    <div class="project-card">
      <div class="project-icon sol">
        <svg viewBox="0 0 24 24"><path d="M17.71 6.55l-11.6-.03a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53zm-11.6 4.72a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53l-11.6-.03zm0 4.72a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53l-11.6-.03z"/></svg>
      </div>
      <h3 class="project-title">Solana Perps DEX</h3>
      <span class="project-chain">Solana · Rust · Anchor</span>
      <p class="project-desc">
        Built the matching engine from scratch. 20ms order execution. Custom oracle that aggregates Pyth + Switchboard for manipulation resistance. Liquidation engine processes 400+ positions per slot without congestion.
      </p>
      <div class="project-metrics">
        <span class="metric">$1.8M daily vol</span>
        <span class="metric">20ms latency</span>
        <span class="metric">0 liquidation failures</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon eth">
        <svg viewBox="0 0 24 24"><path d="M12 1.5l-8 13.1L12 18.7l8-4.1L12 1.5zm0 18.4l-8-4.9L12 22.5l8-7.5-8 4.9z"/></svg>
      </div>
      <h3 class="project-title">Prediction Market Protocol</h3>
      <span class="project-chain">Arbitrum · Solidity · UMA</span>
      <p class="project-desc">
        Polymarket-style but permissionless. LMSR pricing for accurate odds. UMA optimistic oracle for dispute resolution. Conditional tokens with proper ERC-1155 accounting. Gas optimized—89k for market creation.
      </p>
      <div class="project-metrics">
        <span class="metric">$2.1M TVL</span>
        <span class="metric">8,400+ markets</span>
        <span class="metric">99.4% resolution accuracy</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon data">
        <svg viewBox="0 0 24 24"><path d="M3 13h2v8H3v-8zm6-4h2v12H9V9zm6-3h2v15h-2V6zm6 7h2v8h-2v-8z"/></svg>
      </div>
      <h3 class="project-title">MEV Detection Pipeline</h3>
      <span class="project-chain">Ethereum · Python · Dune</span>
      <p class="project-desc">
        Parses transaction traces to classify sandwich attacks, atomic arb, and liquidations. XGBoost model trained on labeled MEV—96.2% precision. Runs against Flashbots relay data in real-time.
      </p>
      <div class="project-metrics">
        <span class="metric">18M txns analyzed</span>
        <span class="metric">$124M MEV tracked</span>
        <span class="metric">used by 3 protocols</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon eth">
        <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg>
      </div>
      <h3 class="project-title">Concentrated Liquidity AMM</h3>
      <span class="project-chain">Base · Solidity · Yul</span>
      <p class="project-desc">
        Uniswap V3 style with custom tick spacing. Position NFTs, multi-hop router, flash loans. Rewrote hot paths in Yul—38% gas reduction on swaps. Passed audit with 0 critical/high findings.
      </p>
      <div class="project-metrics">
        <span class="metric">$3.2M volume</span>
        <span class="metric">38% cheaper swaps</span>
        <span class="metric">audited</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon sol">
        <svg viewBox="0 0 24 24"><path d="M12 2L4.5 20.29l.71.71L12 18l6.79 3 .71-.71z"/></svg>
      </div>
      <h3 class="project-title">Token-2022 Launchpad</h3>
      <span class="project-chain">Solana · Rust · Jupiter</span>
      <p class="project-desc">
        Fair launch platform using Token-2022 extensions. Transfer hooks block sniping bots. Dutch auction with configurable decay curves. Zero successful bot attacks across 7 token launches.
      </p>
      <div class="project-metrics">
        <span class="metric">$4.2M raised</span>
        <span class="metric">7 successful TGEs</span>
        <span class="metric">0 bot exploits</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon tools">
        <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
      </div>
      <h3 class="project-title">Liquidation Keeper</h3>
      <span class="project-chain">ETH + L2s · Python · Flashbots</span>
      <p class="project-desc">
        Watches health factors across Aave, Compound, Maker. Flash loans for capital efficiency. Flashbots bundles to avoid gas wars and failed txns. Consistently profitable since launch.
      </p>
      <div class="project-metrics">
        <span class="metric">1,847 liquidations</span>
        <span class="metric">$520K volume</span>
        <span class="metric">net profitable</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon data">
        <svg viewBox="0 0 24 24"><path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.79-7 8.94V12H5V6.3l7-3.11v8.8z"/></svg>
      </div>
      <h3 class="project-title">Bridge Security Monitor</h3>
      <span class="project-chain">Multi-chain · TimescaleDB · Python</span>
      <p class="project-desc">
        Tracks 8 major bridges for anomalies: TVL drops, admin key usage, upgrade events. Caught 2 incidents before public disclosure. Alerts in under 30 seconds.
      </p>
      <div class="project-metrics">
        <span class="metric">$2.8B TVL monitored</span>
        <span class="metric">99.97% uptime</span>
        <span class="metric">2 incidents flagged early</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon tools">
        <svg viewBox="0 0 24 24"><path d="M13 2.05v2.02c3.95.49 7 3.85 7 7.93 0 3.21-1.92 6-4.72 7.28L13 17v5h5l-1.22-1.22C19.91 19.07 22 15.76 22 12c0-5.18-3.95-9.45-9-9.95zM11 2.05C5.94 2.55 2 6.81 2 12c0 3.76 2.09 7.07 5.22 8.78L6 22h5v-5l-2.28 2.28C6.92 18 5 15.21 5 12c0-4.08 3.05-7.44 7-7.93V2.05z"/></svg>
      </div>
      <h3 class="project-title">Gas Optimization Patterns</h3>
      <span class="project-chain">EVM · Solidity · Yul</span>
      <p class="project-desc">
        Open source library of gas patterns. Storage packing, assembly optimizations, unchecked math where safe. Benchmarked against OpenZeppelin and Solmate. Used by 14 production protocols.
      </p>
      <div class="project-metrics">
        <span class="metric">420 GitHub stars</span>
        <span class="metric">14 protocols using</span>
        <span class="metric">25-55% gas savings</span>
      </div>
    </div>

  </div>

  <!-- Why Me Section -->
  <h2>Why Work With Me</h2>
  <div class="why-me">
    <ul class="why-list">
      <li><strong>I've shipped.</strong> 52 contracts on mainnet. Not testnets, not "coming soon"—actual production code securing real money.</li>
      <li><strong>I read before I write.</strong> 10 years of data analysis means I understand systems before I build them. I've read more protocol code than most.</li>
      <li><strong>Security is default.</strong> Every contract gets fuzzed. I use Slither, Mythril, manual review. I've never shipped an exploitable bug.</li>
      <li><strong>I say no.</strong> Turned down projects with bad tokenomics, hidden admin functions, or "move fast and break things" attitudes toward user funds.</li>
      <li><strong>I know what companies actually need.</strong> Not just code—monitoring, documentation, incident response plans, upgrade paths.</li>
      <li><strong>Data background = edge.</strong> I can query Dune, build dashboards, analyze on-chain behavior. Most devs can't.</li>
    </ul>
  </div>

  <!-- What Crypto Needs -->
  <h2>What I Care About</h2>
  <div class="code-block">
<span class="code-comment">// The problems worth solving</span>

<span class="code-keyword">const</span> <span class="code-func">priorities</span> = {
  security: <span class="code-string">"users shouldn't lose funds to preventable bugs"</span>,
  transparency: <span class="code-string">"if you can't verify it, don't trust it"</span>,
  ux: <span class="code-string">"crypto is too hard to use, we can fix that"</span>,
  infrastructure: <span class="code-string">"oracles, bridges, sequencers—boring but critical"</span>,
  sustainability: <span class="code-string">"yield should come from somewhere real"</span>
};

<span class="code-comment">// I build with these in mind</span>
  </div>

  <!-- Skills -->
  <h2>Stack</h2>
  <div class="skills-visual">
    <div class="skill-card">
      <div class="skill-icon-wrap">
        <svg viewBox="0 0 24 24"><path d="M14 2H6c-1.1 0-1.99.9-1.99 2L4 20c0 1.1.89 2 1.99 2H18c1.1 0 2-.9 2-2V8l-6-6zm2 16H8v-2h8v2zm0-4H8v-2h8v2zm-3-5V3.5L18.5 9H13z"/></svg>
      </div>
      <div class="skill-title">Smart Contracts</div>
      <div class="skill-list">Solidity · Rust · Anchor · Yul · Foundry · Hardhat</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon-wrap">
        <svg viewBox="0 0 24 24"><path d="M17.71 6.55l-11.6-.03a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53zm-11.6 4.72a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53l-11.6-.03zm0 4.72a.76.76 0 0 0-.53.22l-1.5 1.55a.31.31 0 0 0 .22.53l11.6.03a.76.76 0 0 0 .53-.22l1.5-1.55a.31.31 0 0 0-.22-.53l-11.6-.03z"/></svg>
      </div>
      <div class="skill-title">Chains</div>
      <div class="skill-list">Ethereum · Solana · Arbitrum · Base · Optimism · Polygon</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon-wrap">
        <svg viewBox="0 0 24 24"><path d="M3.5 18.49l6-6.01 4 4L22 6.92l-1.41-1.41-7.09 7.97-4-4L2 16.99z"/></svg>
      </div>
      <div class="skill-title">Analytics</div>
      <div class="skill-list">Dune · The Graph · Python · SQL · MEV · Flashbots</div>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta">
    <h3>Let's talk</h3>
    <p>Protocol engineering · Smart contracts · On-chain analytics</p>
    <a href="mailto:shilpa@example.com" class="cta-btn">Get in touch →</a>
  </div>

  <footer>
    © 2024 Shilpa Angadi
  </footer>

</div>

</body>
</html>
