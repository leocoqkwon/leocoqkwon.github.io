<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>권다솔 이력서</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&family=Noto+Serif+KR:wght@400;600;700&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink: #1a1714;
    --ink2: #4a4540;
    --ink3: #8a8580;
    --accent: #b5460f;
    --accent-light: #f5ece6;
    --gold: #c8983a;
    --line: #e2ddd8;
    --bg: #faf8f5;
    --white: #ffffff;
  }

  @page { margin: 0; size: A4; }

  body {
    background: #e8e4dc;
    font-family: 'Noto Sans KR', sans-serif;
    color: var(--ink);
    -webkit-font-smoothing: antialiased;
    padding: 40px 20px;
  }

  .page {
    width: 794px;
    min-height: 1123px;
    background: var(--bg);
    margin: 0 auto 40px;
    position: relative;
    overflow: hidden;
  }

  /* ── HEADER ── */
  .header {
    display: grid;
    grid-template-columns: 200px 1fr;
    min-height: 220px;
  }

  .header-left {
    background: var(--ink);
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 32px 28px;
    position: relative;
  }

  .header-left::after {
    content: '';
    position: absolute;
    bottom: 0; right: -1px;
    width: 0; height: 0;
    border-style: solid;
    border-width: 0 0 36px 36px;
    border-color: transparent transparent var(--bg) transparent;
  }

  .name-ko {
    font-family: 'Noto Serif KR', serif;
    font-size: 28px;
    font-weight: 700;
    color: #ffffff;
    letter-spacing: 0.08em;
    line-height: 1;
    margin-bottom: 4px;
  }

  .name-en {
    font-size: 11px;
    font-weight: 300;
    color: #888;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  .birth-tag {
    font-size: 11px;
    color: #aaa;
    font-weight: 300;
  }

  .header-right {
    background: var(--white);
    padding: 36px 40px 36px 44px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .header-title {
    font-family: 'DM Serif Display', serif;
    font-size: 13px;
    letter-spacing: 0.22em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 18px;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px 24px;
  }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .contact-icon {
    width: 28px; height: 28px;
    border-radius: 50%;
    background: var(--accent-light);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }

  .contact-icon svg {
    width: 13px; height: 13px;
    fill: var(--accent);
  }

  .contact-label {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 400;
    letter-spacing: 0.05em;
    display: block;
    margin-bottom: 1px;
  }

  .contact-value {
    font-size: 12.5px;
    color: var(--ink);
    font-weight: 400;
  }

  .header-bottom {
    display: flex;
    gap: 12px;
    margin-top: 20px;
    padding-top: 18px;
    border-top: 1px solid var(--line);
  }

  .tag {
    font-size: 11px;
    font-weight: 500;
    padding: 4px 12px;
    border-radius: 100px;
    letter-spacing: 0.03em;
  }

  .tag-dark { background: var(--ink); color: #fff; }
  .tag-outline { background: transparent; border: 1px solid var(--line); color: var(--ink2); }
  .tag-accent { background: var(--accent-light); color: var(--accent); }

  /* ── BODY ── */
  .body {
    display: grid;
    grid-template-columns: 200px 1fr;
  }

  /* ── SIDEBAR ── */
  .sidebar {
    background: #f0ede8;
    padding: 36px 0;
    border-right: 1px solid var(--line);
  }

  .sidebar-section {
    padding: 0 28px 32px;
    border-bottom: 1px solid #e0dbd4;
    margin-bottom: 0;
  }

  .sidebar-section:last-child {
    border-bottom: none;
  }

  .sidebar-title {
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: var(--ink3);
    text-transform: uppercase;
    margin-bottom: 16px;
    padding-top: 28px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .sidebar-title::before {
    content: '';
    display: block;
    width: 16px; height: 2px;
    background: var(--accent);
    border-radius: 1px;
  }

  .edu-item {
    margin-bottom: 20px;
  }

  .edu-item:last-child { margin-bottom: 0; }

  .edu-school {
    font-size: 12px;
    font-weight: 700;
    color: var(--ink);
    line-height: 1.4;
    margin-bottom: 3px;
  }

  .edu-dept {
    font-size: 11px;
    color: var(--ink2);
    font-weight: 400;
    margin-bottom: 3px;
  }

  .edu-period {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 300;
  }

  .edu-gpa {
    display: inline-block;
    margin-top: 5px;
    font-size: 10px;
    font-weight: 500;
    background: var(--white);
    color: var(--gold);
    border: 1px solid #e8d8b8;
    padding: 2px 8px;
    border-radius: 4px;
  }

  .edu-thesis {
    margin-top: 8px;
    font-size: 10px;
    color: var(--ink2);
    line-height: 1.6;
    padding-left: 10px;
    border-left: 2px solid var(--line);
    font-weight: 300;
  }

  .stat-row {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .stat-item {
    background: var(--white);
    border-radius: 8px;
    padding: 12px 14px;
    border: 1px solid var(--line);
  }

  .stat-num {
    font-family: 'DM Serif Display', serif;
    font-size: 22px;
    color: var(--ink);
    line-height: 1;
    margin-bottom: 3px;
  }

  .stat-num span {
    font-size: 13px;
    color: var(--ink3);
    font-family: 'Noto Sans KR', sans-serif;
    font-weight: 300;
  }

  .stat-label {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 400;
  }

  .info-list {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .info-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .info-key {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 400;
  }

  .info-val {
    font-size: 11px;
    color: var(--ink2);
    font-weight: 500;
    text-align: right;
  }

  /* ── MAIN CONTENT ── */
  .main {
    padding: 0 40px 40px;
  }

  .section {
    padding-top: 32px;
    margin-bottom: 8px;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 24px;
    padding-bottom: 12px;
    border-bottom: 2px solid var(--ink);
    position: relative;
  }

  .section-header::after {
    content: '';
    position: absolute;
    bottom: -2px; left: 0;
    width: 40px; height: 2px;
    background: var(--accent);
  }

  .section-name {
    font-family: 'Noto Serif KR', serif;
    font-size: 17px;
    font-weight: 700;
    color: var(--ink);
    letter-spacing: -0.01em;
  }

  .section-en {
    font-size: 10px;
    letter-spacing: 0.16em;
    color: var(--ink3);
    text-transform: uppercase;
    font-weight: 400;
  }

  .total-badge {
    margin-left: auto;
    font-size: 11px;
    font-weight: 500;
    color: var(--accent);
    background: var(--accent-light);
    padding: 3px 10px;
    border-radius: 100px;
  }

  /* Experience item */
  .exp-item {
    display: grid;
    grid-template-columns: 130px 1fr;
    gap: 0 24px;
    margin-bottom: 28px;
    position: relative;
  }

  .exp-item:not(:last-child)::after {
    content: '';
    position: absolute;
    bottom: -14px; left: 0;
    right: 0; height: 1px;
    background: var(--line);
  }

  .exp-left { padding-top: 2px; }

  .exp-period {
    font-size: 10.5px;
    color: var(--ink3);
    font-weight: 300;
    line-height: 1.6;
    margin-bottom: 4px;
  }

  .exp-duration {
    display: inline-block;
    font-size: 10px;
    font-weight: 500;
    color: var(--ink2);
    background: var(--line);
    padding: 2px 7px;
    border-radius: 4px;
    margin-bottom: 4px;
  }

  .exp-location {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 300;
    margin-top: 4px;
  }

  .exp-right {}

  .exp-top {
    display: flex;
    align-items: baseline;
    gap: 10px;
    margin-bottom: 4px;
    flex-wrap: wrap;
  }

  .exp-company {
    font-family: 'Noto Serif KR', serif;
    font-size: 15px;
    font-weight: 600;
    color: var(--ink);
    letter-spacing: -0.01em;
  }

  .exp-role {
    font-size: 11.5px;
    color: var(--accent);
    font-weight: 500;
    background: var(--accent-light);
    padding: 2px 9px;
    border-radius: 100px;
  }

  .exp-task {
    font-size: 10.5px;
    color: var(--ink3);
    font-weight: 400;
    margin-bottom: 10px;
  }

  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 7px;
  }

  .exp-bullets li {
    font-size: 12px;
    color: var(--ink2);
    line-height: 1.65;
    padding-left: 14px;
    position: relative;
    font-weight: 300;
  }

  .exp-bullets li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 10px;
    top: 3px;
  }

  .exp-highlight {
    display: inline;
    background: linear-gradient(to bottom, transparent 60%, #f5ece680 60%);
    font-weight: 500;
    color: var(--ink);
  }

  .kpi-row {
    display: flex;
    gap: 8px;
    margin-top: 10px;
    flex-wrap: wrap;
  }

  .kpi-badge {
    font-size: 10.5px;
    font-weight: 500;
    padding: 4px 10px;
    border-radius: 6px;
    background: #f0ede8;
    color: var(--ink2);
    border: 1px solid var(--line);
  }

  .kpi-badge.highlight {
    background: #fef3ea;
    color: #b5460f;
    border-color: #f0c9a8;
  }

  /* Wish section */
  .wish-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .wish-item {
    background: var(--white);
    border: 1px solid var(--line);
    border-radius: 10px;
    padding: 14px 16px;
  }

  .wish-label {
    font-size: 10px;
    color: var(--ink3);
    font-weight: 400;
    letter-spacing: 0.05em;
    margin-bottom: 5px;
  }

  .wish-value {
    font-size: 13px;
    font-weight: 600;
    color: var(--ink);
  }

  /* Footer */
  .footer {
    background: var(--ink);
    padding: 16px 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer-note {
    font-size: 10px;
    color: #666;
    font-weight: 300;
  }

  .footer-date {
    font-size: 10px;
    color: #888;
    font-weight: 400;
    letter-spacing: 0.05em;
  }
</style>
</head>
<body>

<div class="page">
  <!-- HEADER -->
  <div class="header">
    <div class="header-left">
      <div class="name-ko">권다솔</div>
      <div class="name-en">Kwon Dasol</div>
      <div class="birth-tag">1989년생 · 만 36세 · 여</div>
    </div>
    <div class="header-right">
      <div>
        <div class="header-title">Curriculum Vitae</div>
        <div class="contact-grid">
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
            </div>
            <div>
              <span class="contact-label">휴대폰</span>
              <span class="contact-value">010-2236-3854</span>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
            </div>
            <div>
              <span class="contact-label">이메일</span>
              <span class="contact-value">leocoqkwon@gmail.com</span>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M12 2C8.1 2 5 5.1 5 9c0 5.2 7 13 7 13s7-7.8 7-13c0-3.9-3.1-7-7-7zm0 9.5c-1.4 0-2.5-1.1-2.5-2.5S10.6 6.5 12 6.5s2.5 1.1 2.5 2.5S13.4 11.5 12 11.5z"/></svg>
            </div>
            <div>
              <span class="contact-label">주소</span>
              <span class="contact-value">경기 광명시 하안동</span>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 3c1.9 0 3.5 1.6 3.5 3.5S13.9 13 12 13s-3.5-1.6-3.5-3.5S10.1 6 12 6zm7 13H5v-.6c0-2 4-3.1 7-3.1s7 1.1 7 3.1V19z"/></svg>
            </div>
            <div>
              <span class="contact-label">포트폴리오</span>
              <span class="contact-value" style="font-size:11px;">Notion · Naver Blog</span>
            </div>
          </div>
        </div>
      </div>
      <div class="header-bottom">
        <span class="tag tag-dark">심리학 기반</span>
        <span class="tag tag-accent">교육 콘텐츠 기획</span>
        <span class="tag tag-outline">영어 교육</span>
        <span class="tag tag-outline">연구개발</span>
        <span class="tag tag-outline">B2B 영업</span>
      </div>
    </div>
  </div>

  <!-- BODY -->
  <div class="body">
    <!-- SIDEBAR -->
    <div class="sidebar">
      <!-- 학력 -->
      <div class="sidebar-section">
        <div class="sidebar-title">학력</div>

        <div class="edu-item">
          <div class="edu-school">고려대학교<br>공학대학원</div>
          <div class="edu-dept">산업경영공학과 (석사)</div>
          <div class="edu-period">2017.09 – 2019.06</div>
          <div class="edu-gpa">GPA 3.88 / 4.5</div>
          <div class="edu-thesis">자율주행시 비운전과제 모달리티가 운전자 스트레스 및 운전성능에 미치는 영향 분석</div>
        </div>

        <div class="edu-item">
          <div class="edu-school">George Mason<br>University</div>
          <div class="edu-dept">심리학과 (학사)</div>
          <div class="edu-period">2012.09 – 2015.12</div>
          <div class="edu-gpa">GPA 3.41 / 4.0</div>
        </div>
      </div>

      <!-- 경력 요약 -->
      <div class="sidebar-section">
        <div class="sidebar-title">경력 요약</div>
        <div class="stat-row">
          <div class="stat-item">
            <div class="stat-num">8<span>년 10개월</span></div>
            <div class="stat-label">총 경력 기간</div>
          </div>
          <div class="stat-item">
            <div class="stat-num">5<span>개 기관</span></div>
            <div class="stat-label">근무 기관 수</div>
          </div>
          <div class="stat-item">
            <div class="stat-num">1<span>년 1개월</span></div>
            <div class="stat-label">해외 근무 (미국 버지니아)</div>
          </div>
        </div>
      </div>

      <!-- 희망 근무 -->
      <div class="sidebar-section">
        <div class="sidebar-title">희망 근무</div>
        <div class="info-list">
          <div class="info-row">
            <span class="info-key">고용형태</span>
            <span class="info-val">정규직</span>
          </div>
          <div class="info-row">
            <span class="info-key">희망 근무지</span>
            <span class="info-val">서울 전지역</span>
          </div>

        </div>
      </div>

      <!-- 지원 분야 -->
      <div class="sidebar-section">
        <div class="sidebar-title">지원 분야</div>
        <div style="display:flex; flex-direction:column; gap:6px;">
          <div style="font-size:11px; font-weight:500; color:var(--ink2); background:var(--white); padding:7px 10px; border-radius:6px; border:1px solid var(--line);">제품영업 / 서비스영업</div>
          <div style="font-size:11px; font-weight:500; color:var(--ink2); background:var(--white); padding:7px 10px; border-radius:6px; border:1px solid var(--line);">교재개발 · 교수설계</div>
          <div style="font-size:11px; font-weight:500; color:var(--accent); background:var(--accent-light); padding:7px 10px; border-radius:6px; border:1px solid #f0c9a8;">교육기획 · 콘텐츠개발</div>
        </div>
      </div>
    </div>

    <!-- MAIN -->
    <div class="main">
      <!-- 경력 -->
      <div class="section">
        <div class="section-header">
          <span class="section-name">경력사항</span>
          <span class="section-en">Work Experience</span>
          <span class="total-badge">총 8년 10개월</span>
        </div>

        <!-- 인싸이트 -->
        <div class="exp-item">
          <div class="exp-left">
            <div class="exp-period">2022.06 – 2024.09</div>
            <div class="exp-duration">2년 4개월</div>
          </div>
          <div class="exp-right">
            <div class="exp-top">
              <span class="exp-company">인싸이트</span>
              <span class="exp-role">연구개발 대리</span>
            </div>
            <div class="exp-task">주요직무 · 반응형웹, 웹마스터</div>
            <ul class="exp-bullets">
              <li><span class="exp-highlight">아동 및 직장인 대상 심리검사 개발</span> — 사용자 특성에 따른 심리검사를 기획하고 데이터 수집·정리를 거쳐 웹사이트형 심리검사를 출간</li>
              <li>100개 이상의 심리검사를 활용하는 <span class="exp-highlight">고객관리 경험</span> — 고객에게 필요한 검사를 설명·소개하고 필요한 데이터를 제공</li>
            </ul>
            <div class="kpi-row">
              <span class="kpi-badge">심리검사 개발</span>
              <span class="kpi-badge">데이터 수집·분석</span>
              <span class="kpi-badge">고객관리 100+건</span>

            </div>
          </div>
        </div>

        <!-- 잉글리쉬에그 -->
        <div class="exp-item">
          <div class="exp-left">
            <div class="exp-period">2020.10 – 2024.08</div>
            <div class="exp-duration">3년 11개월</div>
          </div>
          <div class="exp-right">
            <div class="exp-top">
              <span class="exp-company">잉글리쉬에그</span>
              <span class="exp-role">액터팀 프리랜서</span>
            </div>
            <div class="exp-task">주요직무 · 영어 교육</div>
            <ul class="exp-bullets">
              <li>미취학 아동 대상 <span class="exp-highlight">영어 놀이 수업 진행</span> — 자연스러운 모국어 방식으로 영어 노출 및 언어 습득 지원</li>
              <li>체계적인 커리큘럼(스토리, 뮤지컬 노래, 게임, Arts &amp; Crafts, Physical Play Activity) 기반 수업 운영</li>
              <li>수업 후 보호자에게 내용·복습 방법을 전달하며 <span class="exp-highlight">가정 연계 학습 설계</span></li>
            </ul>
            <div class="kpi-row">
              <span class="kpi-badge">영어 놀이 교육</span>
              <span class="kpi-badge">커리큘럼 운영</span>
              <span class="kpi-badge">보호자 커뮤니케이션</span>
            </div>
          </div>
        </div>

        <!-- 피엘코리아 -->
        <div class="exp-item">
          <div class="exp-left">
            <div class="exp-period">2019.09 – 2020.05</div>
            <div class="exp-duration">9개월</div>
          </div>
          <div class="exp-right">
            <div class="exp-top">
              <span class="exp-company">피엘코리아</span>
              <span class="exp-role">영업팀 사원</span>
            </div>
            <div class="exp-task">주요직무 · 고객경험관리, 고객문의분석</div>
            <ul class="exp-bullets">
              <li>실리콘 부품 <span class="exp-highlight">B2B 옴니채널 판매 전략</span> 수립 및 KPI 작성·피드백 관리 (BSC 활용)</li>
              <li>파트너사별 차등 판매 전략으로 <span class="exp-highlight">전년 대비 20% 매출 증가</span> 달성</li>
              <li>협력사 담당자 밀착 네트워킹을 통해 <span class="exp-highlight">실제 판매율 115%</span> 달성 및 장기 거래 확보</li>
            </ul>
            <div class="kpi-row">
              <span class="kpi-badge highlight">매출 +20% YoY</span>
              <span class="kpi-badge highlight">판매율 115%</span>
              <span class="kpi-badge">BSC 기반 KPI</span>
              <span class="kpi-badge">B2B 영업관리</span>
            </div>
          </div>
        </div>

        <!-- Therapeutic Alliance -->
        <div class="exp-item">
          <div class="exp-left">
            <div class="exp-period">2016.01 – 2017.01</div>
            <div class="exp-duration">1년 1개월</div>
            <div class="exp-location">🇺🇸 미국 버지니아</div>
          </div>
          <div class="exp-right">
            <div class="exp-top">
              <span class="exp-company">Therapeutic Alliance</span>
              <span class="exp-role">ABA 연구원</span>
            </div>
            <div class="exp-task">주요직무 · 심리치료사</div>
            <ul class="exp-bullets">
              <li>자폐 스펙트럼 아동 대상 <span class="exp-highlight">Applied Behavior Analysis 행동치료</span> 수행</li>
              <li>클라이언트 행동 데이터 정량 수집·분석 후 슈퍼바이저와 협업하여 기능적 자료 평가 및 중재 프로그램 설계</li>
            </ul>
            <div class="kpi-row">
              <span class="kpi-badge">ABA 행동치료</span>
              <span class="kpi-badge">자폐 스펙트럼</span>
              <span class="kpi-badge">데이터 기반 중재</span>
            </div>
          </div>
        </div>

        <!-- FPCS -->
        <div class="exp-item">
          <div class="exp-left">
            <div class="exp-period">2013.01 – 2015.12</div>
            <div class="exp-duration">3년</div>
            <div class="exp-location">🇺🇸 미국 버지니아</div>
          </div>
          <div class="exp-right">
            <div class="exp-top">
              <span class="exp-company">Fairfax Public County School</span>
              <span class="exp-role">한국어 수업 프리랜서</span>
            </div>
            <div class="exp-task">주요직무 · 한국어 교육</div>
            <ul class="exp-bullets">
              <li>교포 아동 대상 <span class="exp-highlight">한글 기초반 수업 설계 및 운영</span> — 체계적 커리큘럼 제공</li>
              <li>버지니아주 FPCS에서 <span class="exp-highlight">한국어 제2외국어 공식 채택</span> 후 종일반 커리큘럼 구성 참여 및 After Class 진행</li>
            </ul>
            <div class="kpi-row">
              <span class="kpi-badge">한국어 커리큘럼</span>
              <span class="kpi-badge">공립학교 정규 채택</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-note">위의 모든 기재사항은 사실과 다름없음을 확인합니다. &nbsp;·&nbsp; 작성자: 권다솔</div>
    <div class="footer-date">최종 수정일: 2026. 03. 01</div>
  </div>
</div>

</body>
</html>
