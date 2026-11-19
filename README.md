<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>משחק זיכרון לספרות פאי (π)</title>
  <style>
    :root {
      --bg: #0f172a;
      --card: #1e293b;
      --card-hover: #334155;
      --text: #f8fafc;
      --muted: #94a3b8;
      --accent: #38bdf8;
      --accent-dark: #0284c7;
      --success: #22c55e;
      --danger: #ef4444;
      --warning: #f59e0b;
      --border: #334155;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px 15px;
    }

    .container {
      width: 100%;
      max-width: 680px;
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    header {
      text-align: center;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    header h1 {
      font-size: 1.9rem;
      color: var(--accent);
      letter-spacing: 0.5px;
    }

    header p {
      color: var(--muted);
      font-size: 0.95rem;
    }

    /* Mode Selector */
    .modes {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 8px;
    }

    .mode-btn {
      background: var(--card);
      color: var(--text);
      border: 2px solid var(--border);
      padding: 10px 6px;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 600;
      font-size: 0.9rem;
      transition: all 0.15s ease;
    }

    .mode-btn:hover {
      background: var(--card-hover);
    }

    .mode-btn.active {
      background: var(--accent-dark);
      border-color: var(--accent);
      color: #fff;
    }

    /* Stats Bar */
    .stats-bar {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 12px 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
    }

    .stat-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      min-width: 70px;
    }

    .stat-label {
      font-size: 0.75rem;
      color: var(--muted);
    }

    .stat-value {
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--text);
    }

    /* Timer Bar */
    .timer-container {
      width: 100%;
      height: 10px;
      background: var(--card);
      border-radius: 999px;
      overflow: hidden;
      border: 1px solid var(--border);
      display: none;
    }

    .timer-fill {
      height: 100%;
      width: 100%;
      background: var(--success);
      transition: width 0.05s linear, background-color 0.2s ease;
    }

    /* Pi Display */
    .pi-box {
      background: var(--card);
      border: 2px solid var(--border);
      border-radius: 14px;
      padding: 20px;
      min-height: 110px;
      display: flex;
      align-items: center;
      overflow-x: auto;
      direction: ltr;
      position: relative;
      transition: border-color 0.2s;
    }

    .pi-box.shake {
      animation: shake 0.3s ease-in-out;
      border-color: var(--danger);
    }

    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-6px); }
      75% { transform: translateX(6px); }
    }

    .pi-stream {
      font-family: 'Courier New', Courier, monospace;
      font-size: 2rem;
      font-weight: 700;
      white-space: nowrap;
      display: flex;
      align-items: center;
      gap: 2px;
      letter-spacing: 2px;
    }

    .pi-prefix {
      color: var(--accent);
      margin-right: 4px;
    }

    .digit-correct {
      color: var(--success);
    }

    .digit-guide {
      color: #475569;
    }

    .digit-guide.next-target {
      color: #94a3b8;
      text-decoration: underline;
      text-decoration-color: var(--accent);
    }

    .digit-group-space {
      width: 12px;
      display: inline-block;
    }

    .cursor {
      display: inline-block;
      width: 3px;
      height: 2rem;
      background: var(--accent);
      animation: blink 1s infinite;
      margin-left: 2px;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      51%, 100% { opacity: 0; }
    }

    /* Status Message */
    .message-bar {
      text-align: center;
      font-size: 0.95rem;
      min-height: 24px;
      color: var(--warning);
      font-weight: 600;
    }

    /* Controls */
    .action-controls {
      display: flex;
      justify-content: center;
      gap: 10px;
      flex-wrap: wrap;
    }

    .action-btn {
      background: var(--card);
      color: var(--text);
      border: 1px solid var(--border);
      padding: 8px 14px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 0.9rem;
      font-weight: 600;
      transition: background 0.15s;
    }

    .action-btn:hover:not(:disabled) {
      background: var(--card-hover);
    }

    .action-btn:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    /* Numpad */
    .numpad {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      max-width: 340px;
      width: 100%;
      margin: 0 auto;
    }

    .num-btn {
      background: var(--card);
      color: var(--text);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 16px 0;
      font-size: 1.5rem;
      font-weight: 700;
      cursor: pointer;
      transition: transform 0.08s, background 0.15s, border-color 0.15s;
      user-select: none;
    }

    .num-btn:hover {
      background: var(--card-hover);
    }

    .num-btn:active {
      transform: scale(0.95);
    }

    .num-btn.hint-highlight {
      border-color: var(--warning);
      box-shadow: 0 0 12px rgba(245, 158, 11, 0.5);
      background: rgba(245, 158, 11, 0.15);
    }

    .num-btn.zero-btn {
      grid-column: 2;
    }

    /* Notes Section */
    .notes-section {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 14px;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .notes-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .notes-header h3 {
      font-size: 1rem;
      color: var(--accent);
    }

    .notes-status {
      font-size: 0.8rem;
      color: var(--success);
    }

    textarea {
      width: 100%;
      min-height: 90px;
      background: var(--bg);
      color: var(--text);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 10px;
      font-size: 0.95rem;
      resize: vertical;
      line-height: 1.5;
    }

    textarea:focus {
      outline: none;
      border-color: var(--accent);
    }

    /* Study Reference Table */
    .study-table {
      display: none;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 14px;
      max-height: 240px;
      overflow-y: auto;
      direction: ltr;
      font-family: 'Courier New', Courier, monospace;
      font-size: 1.05rem;
      line-height: 1.8;
      color: var(--muted);
    }

    .study-group {
      display: inline-block;
      margin-right: 12px;
      padding: 2px 6px;
      border-radius: 4px;
      background: rgba(255, 255, 255, 0.03);
    }

    @media (max-width: 480px) {
      .modes {
        grid-template-columns: repeat(2, 1fr);
      }
      .pi-stream {
        font-size: 1.6rem;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <header>
      <h1>משחק זיכרון לספרות פאי (π)</h1>
      <p>הקלד כמה שיותר ספרות אחרי הנקודה העשרונית (3.)</p>
    </header>

    <!-- מצבי משחק -->
    <div class="modes">
      <button class="mode-btn active" data-mode="practice" onclick="setMode('practice')">תרגול</button>
      <button class="mode-btn" data-mode="hardcore" onclick="setMode('hardcore')">מצב קשוח</button>
      <button class="mode-btn" data-mode="timer" onclick="setMode('timer')">טיימר</button>
      <button class="mode-btn" data-mode="study" onclick="setMode('study')">מצב למידה</button>
    </div>

    <!-- נתונים -->
    <div class="stats-bar">
      <div class="stat-item">
        <span class="stat-label">ספרות</span>
        <span class="stat-value" id="scoreVal">0</span>
      </div>
      <div class="stat-item">
        <span class="stat-label">שיא אישי</span>
        <span class="stat-value" id="highScoreVal">0</span>
      </div>
      <div class="stat-item" id="livesStat">
        <span class="stat-label">חיים</span>
        <span class="stat-value" id="livesVal">❤️❤️❤️</span>
      </div>
      <div class="stat-item" id="timerStat" style="display:none;">
        <span class="stat-label">זמן</span>
        <span class="stat-value" id="timerText">3.0s</span>
      </div>
    </div>

    <!-- מד זמן למצב טיימר -->
    <div class="timer-container" id="timerBarContainer">
      <div class="timer-fill" id="timerFill"></div>
    </div>

    <!-- תצוגת פאי -->
    <div class="pi-box" id="piBox">
      <div class="pi-stream" id="piStream">
        <span class="pi-prefix">3.</span><span class="cursor"></span>
      </div>
    </div>

    <!-- הודעות מצב -->
    <div class="message-bar" id="messageBar">התחל להקליד את הספרה הראשונה: 1</div>

    <!-- כפתורי פעולה -->
    <div class="action-controls">
      <button class="action-btn" id="hintBtn" onclick="useHint()">💡 רמז (<span id="hintsLeft">3</span>)</button>
      <button class="action-btn" id="toggleTableBtn" style="display:none;" onclick="toggleStudyTable()">📖 הצג/הסתר טבלת 1,000 ספרות</button>
      <button class="action-btn" onclick="resetGame()">🔄 התחל מחדש</button>
      <button class="action-btn" id="soundBtn" onclick="toggleSound()">🔊 צלילים: פועל</button>
    </div>

    <!-- מקלדת מספרים -->
    <div class="numpad" id="numpad">
      <button class="num-btn" data-num="1" onclick="handleInput('1')">1</button>
      <button class="num-btn" data-num="2" onclick="handleInput('2')">2</button>
      <button class="num-btn" data-num="3" onclick="handleInput('3')">3</button>
      <button class="num-btn" data-num="4" onclick="handleInput('4')">4</button>
      <button class="num-btn" data-num="5" onclick="handleInput('5')">5</button>
      <button class="num-btn" data-num="6" onclick="handleInput('6')">6</button>
      <button class="num-btn" data-num="7" onclick="handleInput('7')">7</button>
      <button class="num-btn" data-num="8" onclick="handleInput('8')">8</button>
      <button class="num-btn" data-num="9" onclick="handleInput('9')">9</button>
      <button class="num-btn zero-btn" data-num="0" onclick="handleInput('0')">0</button>
    </div>

    <!-- רשימת ספרות מלאה למצב למידה -->
    <div class="study-table" id="studyTable"></div>

    <!-- תיבת כתיבה והערות אישית -->
    <div class="notes-section">
      <div class="notes-header">
        <h3>📝 המחברת שלי (הערות וטיפים לשינון)</h3>
        <span class="notes-status" id="notesStatus">נשמר אוטומטית</span>
      </div>
      <textarea id="userNotes" placeholder="כתוב כאן כל מה שאתה לומד, קבוצות ספרות שאתה מנסה לזכור, או הערות לעצמך..."></textarea>
    </div>
  </div>

  <script>
    // 1,000 הספרות הראשונות של פאי אחרי הנקודה העשרונית
    const PI_DIGITS = 
      "14159265358979323846264338327950288419716939937510" +
      "58209749445923078164062862089986280348253421170679" +
      "82148086513282306647093844609550582231725359408128" +
      "48111745028410270193852110555964462294895493038196" +
      "44288109756659334461284756482337867831652712019091" +
      "45648566923460348610454326648213393607260249141273" +
      "72458700660631558817488152092096282925409171536436" +
      "78925903600113305305488204665213841469519415116094" +
      "33057270365759591953092186117381932611793105118548" +
      "07446237996274956735188575272489122793818301194912" +
      "98336733624406566430860213949463952247371907021798" +
      "60943702770539217176293176752384674818467669405132" +
      "00056812714526356082778577134275778960917363717872" +
      "14684409012249534301465495853710507922796892589235" +
      "42019956112129021960864034418159813629774771309960" +
      "51870721134999999837297804995105973173281609631859" +
      "50244594553469083026425223082533446850352619311881" +
      "71010003137838752886587533208381420617177669147303" +
      "59825349042875546873115956286388235378759375195778" +
      "18577805321712268066130019278766111959092164201989";

    let currentMode = 'practice'; // 'practice', 'hardcore', 'timer', 'study'
    let currentIndex = 0;
    let lives = 3;
    let hints = 3;
    let isGameOver = false;
    let soundEnabled = true;

    // Timer variables
    let timerInterval = null;
    let timeLeft = 3.0;
    let maxTime = 3.0;
    let timerStarted = false;

    // High scores per mode
    let highScores = JSON.parse(localStorage.getItem('pi_high_scores_v2')) || {
      practice: 0,
      hardcore: 0,
      timer: 0,
      study: 0
    };

    // Audio Context (Simple Web Audio API without external files)
    let audioCtx = null;
    function playTone(freq, type = 'sine', duration = 0.08) {
      if (!soundEnabled) return;
      try {
        if (!audioCtx) {
          audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        }
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = type;
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
        gain.gain.setValueAtTime(0.12, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + duration);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start();
        osc.stop(audioCtx.currentTime + duration);
      } catch (e) {}
    }

    // Initialize study table
    function buildStudyTable() {
      const table = document.getElementById('studyTable');
      let html = '<strong style="color:var(--accent)">3.</strong> ';
      for (let i = 0; i < PI_DIGITS.length; i += 5) {
        html += `<span class="study-group">${PI_DIGITS.slice(i, i + 5)}</span>`;
      }
      table.innerHTML = html;
    }

    function toggleStudyTable() {
      const table = document.getElementById('studyTable');
      table.style.display = table.style.display === 'block' ? 'none' : 'block';
    }

    function setMode(mode) {
      currentMode = mode;
      document.querySelectorAll('.mode-btn').forEach(btn => {
        btn.classList.toggle('active', btn.dataset.mode === mode);
      });
      resetGame();
    }

    function resetGame() {
      clearInterval(timerInterval);
      timerStarted = false;
      currentIndex = 0;
      isGameOver = false;
      lives = currentMode === 'practice' ? 3 : 0;
      hints = currentMode === 'practice' ? 3 : 0;
      maxTime = 3.0;
      timeLeft = maxTime;

      // Clear hint highlights
      document.querySelectorAll('.num-btn').forEach(b => b.classList.remove('hint-highlight'));

      // Update UI visibility by mode
      document.getElementById('livesStat').style.display = currentMode === 'practice' ? 'flex' : 'none';
      document.getElementById('hintBtn').style.display = currentMode === 'practice' ? 'inline-block' : 'none';
      document.getElementById('timerStat').style.display = currentMode === 'timer' ? 'flex' : 'none';
      document.getElementById('timerBarContainer').style.display = currentMode === 'timer' ? 'block' : 'none';
      document.getElementById('toggleTableBtn').style.display = currentMode === 'study' ? 'inline-block' : 'none';

      if (currentMode !== 'study') {
        document.getElementById('studyTable').style.display = 'none';
      }

      document.getElementById('timerFill').style.width = '100%';
      document.getElementById('timerFill').style.backgroundColor = 'var(--success)';
      document.getElementById('timerText').textContent = '3.0s';

      updateStats();
      renderPiStream();

      if (currentMode === 'study') {
        setMessage('מצב למידה: הקלד חופשי לפי הספרות האפורות (ללא פסילות)', 'var(--accent)');
      } else if (currentMode === 'timer') {
        setMessage('מצב טיימר: הספירה לאחור תתחיל מיד כשתקליד 1!', 'var(--warning)');
      } else {
        setMessage('התחל להקליד את הספרה הראשונה: 1', 'var(--warning)');
      }
    }

    function updateStats() {
      document.getElementById('scoreVal').textContent = currentIndex;
      document.getElementById('highScoreVal').textContent = highScores[currentMode] || 0;
      
      if (currentMode === 'practice') {
        document.getElementById('livesVal').textContent = '❤️'.repeat(lives) + '🖤'.repeat(3 - lives);
        document.getElementById('hintsLeft').textContent = hints;
        document.getElementById('hintBtn').disabled = hints <= 0 || isGameOver;
      }
    }

    function setMessage(text, color = 'var(--warning)') {
      const msg = document.getElementById('messageBar');
      msg.textContent = text;
      msg.style.color = color;
    }

    function renderPiStream() {
      const stream = document.getElementById('piStream');
      let html = '<span class="pi-prefix">3.</span>';

      // Show typed digits (show last 35 to keep DOM super fast, or all if reasonable)
      const startShow = Math.max(0, currentIndex - 40);
      if (startShow > 0) {
        html += '<span style="color:var(--muted)">...</span>';
      }

      for (let i = startShow; i < currentIndex; i++) {
        if (i > 0 && i % 5 === 0) {
          html += '<span class="digit-group-space"></span>';
        }
        html += `<span class="digit-correct">${PI_DIGITS[i]}</span>`;
      }

      html += '<span class="cursor"></span>';

      // In study mode, show next 20 guide digits
      if (currentMode === 'study') {
        const endGuide = Math.min(PI_DIGITS.length, currentIndex + 20);
        for (let i = currentIndex; i < endGuide; i++) {
          if (i > 0 && i % 5 === 0) {
            html += '<span class="digit-group-space"></span>';
          }
          const targetClass = i === currentIndex ? 'digit-guide next-target' : 'digit-guide';
          html += `<span class="${targetClass}">${PI_DIGITS[i]}</span>`;
        }
      }

      stream.innerHTML = html;

      // Auto scroll right in LTR box
      const piBox = document.getElementById('piBox');
      piBox.scrollLeft = piBox.scrollWidth;
    }

    function startTimer() {
      clearInterval(timerInterval);
      // Gradually get slightly faster as score increases, min 1.5s
      maxTime = Math.max(1.5, 3.0 - Math.floor(currentIndex / 10) * 0.15);
      timeLeft = maxTime;

      timerInterval = setInterval(() => {
        timeLeft -= 0.05;
        if (timeLeft <= 0) {
          timeLeft = 0;
          clearInterval(timerInterval);
          triggerGameOver(`נגמר הזמן! הספרה הבאה הייתה ${PI_DIGITS[currentIndex]}`);
        }
        updateTimerUI();
      }, 50);
    }

    function updateTimerUI() {
      const pct = Math.max(0, (timeLeft / maxTime) * 100);
      const fill = document.getElementById('timerFill');
      fill.style.width = pct + '%';
      document.getElementById('timerText').textContent = timeLeft.toFixed(1) + 's';

      if (pct > 50) fill.style.backgroundColor = 'var(--success)';
      else if (pct > 25) fill.style.backgroundColor = 'var(--warning)';
      else fill.style.backgroundColor = 'var(--danger)';
    }

    function handleInput(digit) {
      if (isGameOver) return;
      if (currentIndex >= PI_DIGITS.length) {
        setMessage('מדהים! סיימת את כל 1,000 הספרות!', 'var(--success)');
        return;
      }

      // Clear any active hint highlights
      document.querySelectorAll('.num-btn').forEach(b => b.classList.remove('hint-highlight'));

      const expected = PI_DIGITS[currentIndex];

      if (digit === expected) {
        // Correct!
        currentIndex++;
        playTone(440 + (currentIndex % 12) * 35, 'sine', 0.07);

        if (currentIndex > (highScores[currentMode] || 0)) {
          highScores[currentMode] = currentIndex;
          localStorage.setItem('pi_high_scores_v2', JSON.stringify(highScores));
        }

        if (currentMode === 'timer') {
          timerStarted = true;
          startTimer();
        }

        updateStats();
        renderPiStream();
        setMessage(`מעולה! הגעת ל-${currentIndex} ספרות`, 'var(--success)');
      } else {
        // Wrong digit
        playTone(160, 'sawtooth', 0.2);
        const box = document.getElementById('piBox');
        box.classList.remove('shake');
        void box.offsetWidth; // trigger reflow
        box.classList.add('shake');

        if (currentMode === 'study') {
          setMessage(`טעות קלה! הספרה הבאה היא ${expected}`, 'var(--warning)');
          return;
        }

        if (currentMode === 'practice') {
          lives--;
          updateStats();
          if (lives <= 0) {
            triggerGameOver(`נגמרו החיים! טעית בספרה ${currentIndex + 1} (היה צריך להיות ${expected})`);
          } else {
            setMessage(`טעות! נשארו לך ${lives} חיים. נסה שוב!`, 'var(--danger)');
          }
        } else {
          // Hardcore or Timer mode -> instant game over
          clearInterval(timerInterval);
          triggerGameOver(`נפסלת! לחצת ${digit}, אבל הספרה הנכונה היא ${expected}`);
        }
      }
    }

    function triggerGameOver(reason) {
      isGameOver = true;
      clearInterval(timerInterval);
      setMessage(reason + ' — לחץ על "התחל מחדש" כדי לשחק שוב.', 'var(--danger)');
      updateStats();
    }

    function useHint() {
      if (currentMode !== 'practice' || hints <= 0 || isGameOver) return;
      hints--;
      updateStats();
      const nextDigit = PI_DIGITS[currentIndex];
      const btn = document.querySelector(`.num-btn[data-num="${nextDigit}"]`);
      if (btn) btn.classList.add('hint-highlight');
      setMessage(`רמז: הספרה הבאה היא ${nextDigit}`, 'var(--warning)');
      playTone(660, 'triangle', 0.12);
    }

    function toggleSound() {
      soundEnabled = !soundEnabled;
      document.getElementById('soundBtn').textContent = soundEnabled ? '🔊 צלילים: פועל' : '🔇 צלילים: כבוי';
    }

    // Physical keyboard support (ignore when typing in notes textarea)
    document.addEventListener('keydown', (e) => {
      if (document.activeElement === document.getElementById('userNotes')) return;
      if (e.key >= '0' && e.key <= '9') {
        e.preventDefault();
        handleInput(e.key);
      } else if (e.key === 'Enter' && isGameOver) {
        resetGame();
      }
    });

    // Auto-save user notes
    const notesArea = document.getElementById('userNotes');
    const notesStatus = document.getElementById('notesStatus');
    notesArea.value = localStorage.getItem('pi_user_notes') || '';

    notesArea.addEventListener('input', () => {
      localStorage.setItem('pi_user_notes', notesArea.value);
      notesStatus.textContent = 'שומר...';
      setTimeout(() => {
        notesStatus.textContent = 'נשמר אוטומטית ✓';
      }, 400);
    });

    // Init
    buildStudyTable();
    resetGame();
  </script>
</body>
</html>
