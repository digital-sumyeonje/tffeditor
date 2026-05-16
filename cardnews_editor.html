<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>카드뉴스 에디터</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Pretendard', -apple-system, 'Apple SD Gothic Neo', sans-serif; background: #f5f5f0; min-height: 100vh; }

  /* 폰트 로드 */
  @import url('https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable.min.css');

  /* 상단 탭 */
  .tabs { display: flex; background: #fff; border-bottom: 1px solid #e0e0e0; position: sticky; top: 0; z-index: 100; }
  .tab { flex: 1; padding: 14px 8px; text-align: center; font-size: 13px; font-weight: 500; color: #888; cursor: pointer; border-bottom: 2px solid transparent; transition: all .2s; }
  .tab.active { color: #111; border-bottom-color: #111; }

  /* 섹션 */
  .section { display: none; padding: 16px; }
  .section.active { display: block; }

  /* 설정 섹션 */
  .setting-group { background: #fff; border-radius: 12px; padding: 16px; margin-bottom: 12px; }
  .setting-label { font-size: 12px; font-weight: 600; color: #888; letter-spacing: .05em; text-transform: uppercase; margin-bottom: 10px; }
  .btn-group { display: flex; gap: 8px; flex-wrap: wrap; }
  .btn-opt { padding: 8px 14px; border-radius: 8px; border: 1.5px solid #ddd; background: #fff; font-size: 13px; color: #444; cursor: pointer; transition: all .15s; font-family: inherit; }
  .btn-opt.active { border-color: #111; background: #111; color: #fff; }

  /* 슬라이드 목록 */
  .slide-list { display: flex; flex-direction: column; gap: 10px; }
  .slide-item { background: #fff; border-radius: 12px; padding: 14px 16px; display: flex; align-items: center; gap: 12px; cursor: pointer; border: 2px solid transparent; transition: all .15s; }
  .slide-item.active { border-color: #111; }
  .slide-num { width: 28px; height: 28px; border-radius: 50%; background: #f0f0f0; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: 600; color: #555; flex-shrink: 0; }
  .slide-item.active .slide-num { background: #111; color: #fff; }
  .slide-info { flex: 1; }
  .slide-title { font-size: 14px; font-weight: 500; color: #111; }
  .slide-sub { font-size: 12px; color: #999; margin-top: 2px; }
  .slide-thumb { width: 44px; height: 44px; border-radius: 8px; background: #eee; object-fit: cover; flex-shrink: 0; display: flex; align-items: center; justify-content: center; color: #bbb; font-size: 18px; overflow: hidden; }
  .slide-thumb img { width: 100%; height: 100%; object-fit: cover; }
  .add-slide-btn { background: #fff; border: 1.5px dashed #ccc; border-radius: 12px; padding: 14px; text-align: center; color: #999; font-size: 14px; cursor: pointer; font-family: inherit; width: 100%; margin-top: 4px; }

  /* 에디터 */
  .editor-header { display: flex; align-items: center; gap: 10px; margin-bottom: 14px; }
  .back-btn { background: none; border: none; font-size: 20px; cursor: pointer; color: #444; padding: 4px; }
  .editor-title { font-size: 16px; font-weight: 600; }

  /* 미리보기 캔버스 영역 */
  .preview-wrap { background: #fff; border-radius: 12px; margin-bottom: 14px; overflow: hidden; }
  .canvas-container { position: relative; width: 100%; overflow: hidden; }
  .canvas-container canvas { display: block; width: 100%; height: auto; }

  /* 컴포넌트 토글 */
  .toggle-row { display: flex; align-items: center; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid #f0f0f0; }
  .toggle-row:last-child { border-bottom: none; }
  .toggle-label { font-size: 14px; color: #333; }
  .toggle-switch { position: relative; width: 44px; height: 24px; }
  .toggle-switch input { opacity: 0; width: 0; height: 0; }
  .toggle-slider { position: absolute; inset: 0; background: #ddd; border-radius: 24px; cursor: pointer; transition: .2s; }
  .toggle-slider:before { content: ''; position: absolute; width: 18px; height: 18px; left: 3px; top: 3px; background: #fff; border-radius: 50%; transition: .2s; }
  .toggle-switch input:checked + .toggle-slider { background: #111; }
  .toggle-switch input:checked + .toggle-slider:before { transform: translateX(20px); }

  /* 텍스트 입력 */
  .input-group { margin-bottom: 12px; }
  .input-label { font-size: 12px; font-weight: 600; color: #888; margin-bottom: 6px; display: block; }
  .text-input { width: 100%; padding: 10px 12px; border: 1.5px solid #e0e0e0; border-radius: 8px; font-size: 14px; font-family: inherit; color: #111; background: #fff; resize: vertical; outline: none; transition: border-color .15s; }
  .text-input:focus { border-color: #111; }

  /* 폰트/색상 */
  .row-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 12px; }
  select.text-input { appearance: none; cursor: pointer; }

  /* 이미지 업로드 */
  .img-upload { border: 2px dashed #ddd; border-radius: 10px; padding: 20px; text-align: center; cursor: pointer; color: #aaa; font-size: 13px; background: #fafafa; transition: all .15s; margin-bottom: 12px; }
  .img-upload:hover { border-color: #999; background: #f5f5f5; }
  .img-upload-input { display: none; }
  .img-preview { width: 100%; border-radius: 10px; margin-bottom: 12px; display: none; }

  /* 오버레이 설정 */
  .range-row { display: flex; align-items: center; gap: 10px; }
  .range-row input[type=range] { flex: 1; }
  .range-val { font-size: 13px; color: #555; min-width: 32px; text-align: right; }

  /* 내보내기 버튼 */
  .export-btn { width: 100%; padding: 14px; background: #111; color: #fff; border: none; border-radius: 10px; font-size: 15px; font-weight: 600; cursor: pointer; font-family: inherit; margin-top: 4px; }
  .export-all-btn { width: 100%; padding: 14px; background: #fff; color: #111; border: 1.5px solid #111; border-radius: 10px; font-size: 15px; font-weight: 600; cursor: pointer; font-family: inherit; margin-top: 8px; }

  /* 색상 피커 */
  .color-row { display: flex; align-items: center; gap: 10px; }
  .color-swatch { width: 36px; height: 36px; border-radius: 8px; border: 1.5px solid #e0e0e0; cursor: pointer; flex-shrink: 0; overflow: hidden; }
  .color-swatch input[type=color] { width: 200%; height: 200%; margin: -50%; border: none; cursor: pointer; }

  /* 위치 선택 */
  .position-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; }
  .pos-btn { padding: 8px; border: 1.5px solid #ddd; border-radius: 8px; font-size: 12px; text-align: center; cursor: pointer; color: #555; background: #fff; transition: all .15s; font-family: inherit; }
  .pos-btn.active { border-color: #111; background: #111; color: #fff; }

  .section-card { background: #fff; border-radius: 12px; padding: 16px; margin-bottom: 12px; }
  .section-card-title { font-size: 13px; font-weight: 600; color: #555; margin-bottom: 12px; }

  /* 빈 상태 */
  .empty-state { text-align: center; padding: 40px 20px; color: #999; }
  .empty-icon { font-size: 40px; margin-bottom: 12px; }
</style>
</head>
<body>

<!-- 상단 탭 -->
<div class="tabs">
  <div class="tab active" onclick="switchTab('setup')">설정</div>
  <div class="tab" onclick="switchTab('slides')">슬라이드</div>
  <div class="tab" onclick="switchTab('editor')">편집</div>
</div>

<!-- 설정 탭 -->
<div class="section active" id="tab-setup">
  <div class="setting-group">
    <div class="setting-label">규격</div>
    <div class="btn-group">
      <button class="btn-opt active" onclick="setFormat(this,'1:1')" data-w="1080" data-h="1080">피드 1:1</button>
      <button class="btn-opt" onclick="setFormat(this,'3:4')" data-w="1080" data-h="1440">피드 3:4</button>
      <button class="btn-opt" onclick="setFormat(this,'4:5')" data-w="1080" data-h="1350">피드 4:5</button>
      <button class="btn-opt" onclick="setFormat(this,'9:16')" data-w="1080" data-h="1920">릴스 9:16</button>
    </div>
  </div>
  <div class="setting-group">
    <div class="setting-label">기본 폰트</div>
    <select class="text-input" id="global-font" onchange="state.globalFont=this.value">
      <option value="Pretendard">Pretendard</option>
      <option value="'Apple SD Gothic Neo', sans-serif">Apple SD Gothic Neo</option>
      <option value="'Noto Sans KR', sans-serif">Noto Sans KR</option>
    </select>
  </div>
  <div class="setting-group">
    <div class="setting-label">브랜드 색상 (선택)</div>
    <div class="btn-group" style="align-items:center">
      <div class="color-row">
        <div class="color-swatch"><input type="color" id="brand-color" value="#ffffff" onchange="state.brandColor=this.value"></div>
        <span style="font-size:13px;color:#999">텍스트 배경 색상으로 사용</span>
      </div>
    </div>
  </div>
  <button class="export-btn" onclick="switchTab('slides');addSlideIfEmpty()" style="margin-top:4px">슬라이드 만들기 →</button>
</div>

<!-- 슬라이드 탭 -->
<div class="section" id="tab-slides">
  <div class="slide-list" id="slide-list"></div>
  <button class="add-slide-btn" onclick="addSlide()">+ 슬라이드 추가</button>
</div>

<!-- 편집 탭 -->
<div class="section" id="tab-editor">
  <div id="editor-empty" class="empty-state">
    <div class="empty-icon">✏️</div>
    <p>슬라이드 탭에서<br>편집할 슬라이드를 선택하세요</p>
  </div>
  <div id="editor-content" style="display:none">
    <div class="editor-header">
      <button class="back-btn" onclick="switchTab('slides')">←</button>
      <div class="editor-title" id="editor-slide-title">슬라이드 1</div>
    </div>

    <!-- 미리보기 -->
    <div class="preview-wrap">
      <div class="canvas-container" id="canvas-container">
        <canvas id="preview-canvas"></canvas>
      </div>
    </div>

    <!-- 이미지 업로드 -->
    <div class="section-card">
      <div class="section-card-title">이미지</div>
      <div class="img-upload" onclick="document.getElementById('img-input').click()">
        <div style="font-size:24px;margin-bottom:6px">📷</div>
        <div>이미지를 탭해서 업로드</div>
        <div style="font-size:11px;margin-top:4px;color:#bbb">JPG, PNG, WebP</div>
      </div>
      <input type="file" id="img-input" class="img-upload-input" accept="image/*" onchange="loadImage(this)">
    </div>

    <!-- 컴포넌트 -->
    <div class="section-card">
      <div class="section-card-title">컴포넌트</div>
      <div class="toggle-row">
        <span class="toggle-label">카피 (주 텍스트)</span>
        <label class="toggle-switch"><input type="checkbox" id="tog-copy" checked onchange="renderSlide()"><span class="toggle-slider"></span></label>
      </div>
      <div class="toggle-row">
        <span class="toggle-label">설명문</span>
        <label class="toggle-switch"><input type="checkbox" id="tog-desc" onchange="toggleDesc();renderSlide()"><span class="toggle-slider"></span></label>
      </div>
      <div class="toggle-row">
        <span class="toggle-label">출처 표기</span>
        <label class="toggle-switch"><input type="checkbox" id="tog-source" onchange="renderSlide()"><span class="toggle-slider"></span></label>
      </div>
      <div class="toggle-row">
        <span class="toggle-label">슬라이드 번호</span>
        <label class="toggle-switch"><input type="checkbox" id="tog-num" onchange="renderSlide()"><span class="toggle-slider"></span></label>
      </div>
    </div>

    <!-- 텍스트 입력 -->
    <div class="section-card">
      <div class="section-card-title">텍스트</div>
      <div class="input-group">
        <label class="input-label">카피</label>
        <textarea class="text-input" id="inp-copy" rows="2" placeholder="짧고 강렬하게" oninput="renderSlide()"></textarea>
      </div>
      <div class="input-group" id="desc-group" style="display:none">
        <label class="input-label">설명문</label>
        <textarea class="text-input" id="inp-desc" rows="3" placeholder="부연 설명을 입력하세요" oninput="renderSlide()"></textarea>
      </div>
      <div class="input-group" id="source-group" style="display:none">
        <label class="input-label">출처</label>
        <input type="text" class="text-input" id="inp-source" placeholder="© 출처 / 사진작가 등" oninput="renderSlide()">
      </div>
    </div>

    <!-- 스타일 -->
    <div class="section-card">
      <div class="section-card-title">스타일</div>
      <div class="row-2">
        <div>
          <label class="input-label">폰트</label>
          <select class="text-input" id="slide-font" onchange="renderSlide()">
            <option value="global">기본 폰트</option>
            <option value="Pretendard">Pretendard</option>
            <option value="'Apple SD Gothic Neo'">Apple SD Gothic Neo</option>
            <option value="serif">Serif</option>
          </select>
        </div>
        <div>
          <label class="input-label">카피 크기</label>
          <select class="text-input" id="copy-size" onchange="renderSlide()">
            <option value="64">작게</option>
            <option value="80" selected>보통</option>
            <option value="100">크게</option>
            <option value="120">매우 크게</option>
          </select>
        </div>
      </div>
      <div class="input-group">
        <label class="input-label">텍스트 위치</label>
        <div class="position-grid">
          <button class="pos-btn" onclick="setPos(this,'top-left')" data-pos="top-left">↖ 좌상</button>
          <button class="pos-btn" onclick="setPos(this,'top-center')" data-pos="top-center">↑ 중상</button>
          <button class="pos-btn" onclick="setPos(this,'top-right')" data-pos="top-right">↗ 우상</button>
          <button class="pos-btn" onclick="setPos(this,'mid-left')" data-pos="mid-left">← 좌중</button>
          <button class="pos-btn" onclick="setPos(this,'center')" data-pos="center">중앙</button>
          <button class="pos-btn" onclick="setPos(this,'mid-right')" data-pos="mid-right">→ 우중</button>
          <button class="pos-btn active" onclick="setPos(this,'bottom-left')" data-pos="bottom-left">↙ 좌하</button>
          <button class="pos-btn" onclick="setPos(this,'bottom-center')" data-pos="bottom-center">↓ 중하</button>
          <button class="pos-btn" onclick="setPos(this,'bottom-right')" data-pos="bottom-right">↘ 우하</button>
        </div>
      </div>
      <div class="input-group" style="margin-top:12px">
        <label class="input-label">오버레이 강도</label>
        <div class="range-row">
          <input type="range" min="0" max="90" value="50" id="overlay-opacity" oninput="document.getElementById('ov-val').textContent=this.value+'%';renderSlide()">
          <span class="range-val" id="ov-val">50%</span>
        </div>
      </div>
      <div class="input-group">
        <label class="input-label">텍스트 색상</label>
        <div class="color-row">
          <div class="color-swatch"><input type="color" id="text-color" value="#ffffff" onchange="renderSlide()"></div>
          <span style="font-size:13px;color:#999">카피·설명문 색상</span>
        </div>
      </div>
    </div>

    <!-- 내보내기 -->
    <button class="export-btn" onclick="exportSlide()">💾 이 슬라이드 저장</button>
    <button class="export-all-btn" onclick="exportAll()">📦 전체 저장</button>
  </div>
</div>

<script>
const state = {
  format: { w: 1080, h: 1080, ratio: '1:1' },
  globalFont: 'Pretendard',
  brandColor: '#ffffff',
  slides: [],
  currentSlide: null,
  currentImage: null,
};

// 초기 슬라이드
function init() {
  addSlide('표지');
  renderSlideList();
}

function addSlide(name) {
  const idx = state.slides.length + 1;
  state.slides.push({
    id: Date.now() + Math.random(),
    name: name || (idx === 1 ? '표지' : `슬라이드 ${idx}`),
    image: null,
    copy: '',
    desc: '',
    source: '',
    showCopy: true,
    showDesc: false,
    showSource: false,
    showNum: false,
    font: 'global',
    copySize: 80,
    pos: 'bottom-left',
    overlayOpacity: 50,
    textColor: '#ffffff',
  });
  renderSlideList();
}

function addSlideIfEmpty() {
  if (state.slides.length === 0) addSlide('표지');
}

function renderSlideList() {
  const list = document.getElementById('slide-list');
  list.innerHTML = state.slides.map((s, i) => `
    <div class="slide-item ${state.currentSlide?.id === s.id ? 'active' : ''}" onclick="selectSlide(${i})">
      <div class="slide-num">${i + 1}</div>
      <div class="slide-info">
        <div class="slide-title">${s.name}</div>
        <div class="slide-sub">${s.copy ? s.copy.slice(0,20) + (s.copy.length>20?'…':'') : '텍스트 없음'}</div>
      </div>
      <div class="slide-thumb">
        ${s.image ? `<img src="${s.image}">` : '🖼'}
      </div>
    </div>
  `).join('');
}

function selectSlide(idx) {
  state.currentSlide = state.slides[idx];
  state.currentImage = state.currentSlide.image;
  switchTab('editor');
  loadSlideToEditor();
}

function loadSlideToEditor() {
  const s = state.currentSlide;
  if (!s) return;
  document.getElementById('editor-empty').style.display = 'none';
  document.getElementById('editor-content').style.display = 'block';
  document.getElementById('editor-slide-title').textContent = s.name;
  document.getElementById('inp-copy').value = s.copy;
  document.getElementById('inp-desc').value = s.desc;
  document.getElementById('inp-source').value = s.source;
  document.getElementById('tog-copy').checked = s.showCopy;
  document.getElementById('tog-desc').checked = s.showDesc;
  document.getElementById('tog-source').checked = s.showSource;
  document.getElementById('tog-num').checked = s.showNum;
  document.getElementById('slide-font').value = s.font;
  document.getElementById('copy-size').value = s.copySize;
  document.getElementById('overlay-opacity').value = s.overlayOpacity;
  document.getElementById('ov-val').textContent = s.overlayOpacity + '%';
  document.getElementById('text-color').value = s.textColor;
  document.querySelectorAll('.pos-btn').forEach(b => b.classList.toggle('active', b.dataset.pos === s.pos));
  document.getElementById('desc-group').style.display = s.showDesc ? 'block' : 'none';
  document.getElementById('source-group').style.display = s.showSource ? 'block' : 'none';
  renderSlide();
}

function toggleDesc() {
  const show = document.getElementById('tog-desc').checked;
  document.getElementById('desc-group').style.display = show ? 'block' : 'none';
  const showSrc = document.getElementById('tog-source').checked;
  document.getElementById('source-group').style.display = showSrc ? 'block' : 'none';
}

function setFormat(btn, ratio) {
  document.querySelectorAll('.btn-opt').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  state.format = { w: +btn.dataset.w, h: +btn.dataset.h, ratio };
  if (state.currentSlide) renderSlide();
}

function setPos(btn, pos) {
  document.querySelectorAll('.pos-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  if (state.currentSlide) { state.currentSlide.pos = pos; renderSlide(); }
}

function loadImage(input) {
  const file = input.files[0];
  if (!file) return;
  const reader = new FileReader();
  reader.onload = e => {
    state.currentImage = e.target.result;
    if (state.currentSlide) {
      state.currentSlide.image = e.target.result;
      renderSlide();
      renderSlideList();
    }
  };
  reader.readAsDataURL(file);
}

function saveCurrentSlideState() {
  if (!state.currentSlide) return;
  const s = state.currentSlide;
  s.copy = document.getElementById('inp-copy').value;
  s.desc = document.getElementById('inp-desc').value;
  s.source = document.getElementById('inp-source').value;
  s.showCopy = document.getElementById('tog-copy').checked;
  s.showDesc = document.getElementById('tog-desc').checked;
  s.showSource = document.getElementById('tog-source').checked;
  s.showNum = document.getElementById('tog-num').checked;
  s.font = document.getElementById('slide-font').value;
  s.copySize = +document.getElementById('copy-size').value;
  s.overlayOpacity = +document.getElementById('overlay-opacity').value;
  s.textColor = document.getElementById('text-color').value;
}

function renderSlide() {
  saveCurrentSlideState();
  if (!state.currentSlide) return;
  const s = state.currentSlide;
  const { w, h } = state.format;
  const canvas = document.getElementById('preview-canvas');
  const container = document.getElementById('canvas-container');
  const displayW = container.offsetWidth || 340;
  canvas.width = w;
  canvas.height = h;
  canvas.style.width = displayW + 'px';
  canvas.style.height = (displayW * h / w) + 'px';
  const ctx = canvas.getContext('2d');
  ctx.clearRect(0, 0, w, h);

  // 배경
  ctx.fillStyle = '#1a1a1a';
  ctx.fillRect(0, 0, w, h);

  const font = s.font === 'global' ? state.globalFont : s.font;

  const drawText = () => {
    const pad = 60;
    const pos = s.pos || 'bottom-left';
    const isBottom = pos.startsWith('bottom');
    const isTop = pos.startsWith('top');
    const isMid = pos.startsWith('mid') || pos === 'center';
    const isLeft = pos.endsWith('left');
    const isRight = pos.endsWith('right');
    const isCenter = pos.endsWith('center') || pos === 'center';

    // 오버레이
    const ov = s.overlayOpacity / 100;
    const grad = ctx.createLinearGradient(0, isBottom ? h * 0.45 : isTop ? 0 : h * 0.2, 0, isBottom ? h : isTop ? h * 0.55 : h * 0.8);
    grad.addColorStop(0, `rgba(0,0,0,0)`);
    grad.addColorStop(1, `rgba(0,0,0,${ov})`);
    if (isBottom || isMid) {
      ctx.fillStyle = grad;
      ctx.fillRect(0, isBottom ? h * 0.45 : h * 0.2, w, h);
    }
    if (isTop) {
      const gTop = ctx.createLinearGradient(0, 0, 0, h * 0.55);
      gTop.addColorStop(0, `rgba(0,0,0,${ov})`);
      gTop.addColorStop(1, `rgba(0,0,0,0)`);
      ctx.fillStyle = gTop;
      ctx.fillRect(0, 0, w, h * 0.55);
    }

    const tc = s.textColor || '#ffffff';
    let y;
    if (isBottom) y = h - pad - (s.showSource ? 50 : 0);
    else if (isTop) y = pad + s.copySize;
    else y = h / 2;

    const align = isLeft ? 'left' : isRight ? 'right' : 'center';
    ctx.textAlign = align;
    const x = isLeft ? pad : isRight ? w - pad : w / 2;

    // 슬라이드 번호
    if (s.showNum) {
      const idx = state.slides.findIndex(sl => sl.id === s.id) + 1;
      ctx.font = `400 32px ${font}`;
      ctx.fillStyle = tc;
      ctx.globalAlpha = 0.6;
      ctx.fillText(`${idx} / ${state.slides.length}`, x, isBottom ? h - 36 : 36);
      ctx.globalAlpha = 1;
    }

    // 출처
    if (s.showSource && s.source) {
      ctx.font = `400 28px ${font}`;
      ctx.fillStyle = tc;
      ctx.globalAlpha = 0.55;
      ctx.fillText(s.source, x, isBottom ? h - 36 : h - 36);
      ctx.globalAlpha = 1;
    }

    // 설명문
    if (s.showDesc && s.desc) {
      const dSize = Math.round(s.copySize * 0.45);
      ctx.font = `400 ${dSize}px ${font}`;
      ctx.fillStyle = tc;
      ctx.globalAlpha = 0.8;
      const dLines = wrapText(ctx, s.desc, w - pad * 2);
      const lineH = dSize * 1.55;
      const totalH = dLines.length * lineH;
      let dy = isBottom ? y - totalH - 10 : isTop ? y + s.copySize * 1.3 : y + s.copySize * 0.7;
      dLines.forEach(ln => { ctx.fillText(ln, x, dy); dy += lineH; });
      if (isBottom) y -= totalH + 16;
      ctx.globalAlpha = 1;
    }

    // 카피
    if (s.showCopy && s.copy) {
      ctx.font = `700 ${s.copySize}px ${font}`;
      ctx.fillStyle = tc;
      const lines = wrapText(ctx, s.copy, w - pad * 2);
      const lineH = s.copySize * 1.3;
      let cy = isBottom ? y - (lines.length - 1) * lineH : y;
      lines.forEach(ln => { ctx.fillText(ln, x, cy); cy += lineH; });
    }
  };

  if (state.currentImage) {
    const img = new Image();
    img.onload = () => {
      // 커버 방식으로 이미지 그리기
      const scale = Math.max(w / img.width, h / img.height);
      const iw = img.width * scale;
      const ih = img.height * scale;
      const ix = (w - iw) / 2;
      const iy = (h - ih) / 2;
      ctx.drawImage(img, ix, iy, iw, ih);
      drawText();
    };
    img.src = state.currentImage;
  } else {
    drawText();
  }
}

function wrapText(ctx, text, maxW) {
  const words = text.split('');
  const lines = [];
  let line = '';
  // 줄바꿈 문자 처리
  const parts = text.split('\n');
  const result = [];
  parts.forEach(part => {
    const chars = part.split('');
    let ln = '';
    chars.forEach(ch => {
      const test = ln + ch;
      if (ctx.measureText(test).width > maxW && ln) {
        result.push(ln);
        ln = ch;
      } else ln = test;
    });
    if (ln) result.push(ln);
  });
  return result.length ? result : [''];
}

function exportSlide() {
  renderSlide();
  setTimeout(() => {
    const canvas = document.getElementById('preview-canvas');
    const link = document.createElement('a');
    const idx = state.slides.findIndex(s => s.id === state.currentSlide?.id) + 1;
    link.download = `card_${idx}_${state.format.ratio.replace(':','x')}.png`;
    link.href = canvas.toDataURL('image/png');
    link.click();
  }, 200);
}

function exportAll() {
  state.slides.forEach((slide, i) => {
    const prev = state.currentSlide;
    state.currentSlide = slide;
    state.currentImage = slide.image;
    setTimeout(() => {
      renderSlide();
      setTimeout(() => {
        const canvas = document.getElementById('preview-canvas');
        const link = document.createElement('a');
        link.download = `card_${i+1}_${state.format.ratio.replace(':','x')}.png`;
        link.href = canvas.toDataURL('image/png');
        link.click();
      }, 300);
      state.currentSlide = prev;
      state.currentImage = prev?.image || null;
    }, i * 600);
  });
}

function switchTab(name) {
  document.querySelectorAll('.tab').forEach((t, i) => {
    t.classList.toggle('active', ['setup','slides','editor'][i] === name);
  });
  document.querySelectorAll('.section').forEach((s, i) => {
    s.classList.toggle('active', ['tab-setup','tab-slides','tab-editor'][i] === 'tab-' + name);
  });
  if (name === 'slides') renderSlideList();
  if (name === 'editor' && state.currentSlide) renderSlide();
}

// source-group toggle fix
document.getElementById('tog-source').addEventListener('change', function() {
  document.getElementById('source-group').style.display = this.checked ? 'block' : 'none';
  renderSlide();
});

init();
</script>
</body>
</html>
