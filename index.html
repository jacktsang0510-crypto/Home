<!doctype html>
<html lang="zh-HK">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>記帳 + 稅務估算</title>
  <style>
    body { font-family: system-ui, -apple-system, "PingFang HK", "Noto Sans HK", Arial; margin:0; background:#f6f7fb; }
    .wrap { max-width: 980px; margin: 0 auto; padding: 16px; }
    .card { background:#fff; border-radius: 16px; padding: 16px; box-shadow: 0 6px 18px rgba(0,0,0,.06); margin-bottom: 12px; }
    h1 { margin: 0 0 10px; font-size: 20px; }
    h2 { margin: 0 0 10px; font-size: 16px; }
    .row { display:flex; gap:10px; flex-wrap: wrap; }
    .col { flex:1; min-width: 170px; }
    label { font-size: 13px; opacity:.8; display:block; margin:0 0 6px; }
    input, select, button { width:100%; padding: 12px; border-radius: 12px; border:1px solid #dfe3ee; font-size: 16px; }
    button { border:0; background:#111; color:#fff; font-weight: 800; cursor:pointer; }
    button:active { transform: scale(.99); }
    .ghost { background:#e9ecf7; color:#111; }
    .danger { background:#ff3b30; }
    .big { font-size: 32px; font-weight: 900; }
    .sub { opacity:.75; font-size: 13px; line-height: 1.45; }
    .pill { display:inline-block; padding: 6px 10px; border-radius: 999px; font-size: 12px; background:#eef1ff; }
    .green { color:#16a34a; font-weight: 900; }
    .red { color:#dc2626; font-weight: 900; }
    .grid { display:grid; grid-template-columns: 1fr 1fr; gap:10px; }
    @media (max-width: 900px){ .grid { grid-template-columns: 1fr; } }
    table { width:100%; border-collapse: collapse; }
    td { padding: 10px 0; border-top:1px solid #eef0f6; }
    td:last-child { text-align:right; font-weight: 900; }
    .list { margin: 0; padding: 0; list-style:none; }
    .item { display:flex; justify-content:space-between; gap:10px; padding: 12px 0; border-top:1px solid #eef0f6; align-items:center; }
    .left { display:flex; flex-direction:column; gap:4px; }
    .meta { font-size: 12px; opacity:.7; }
    .tag { font-size:12px; padding:4px 8px; border-radius:999px; background:#f2f4ff; display:inline-block; }
    .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; }
  </style>
</head>
<body>
<div class="wrap">

  <div class="card">
    <h1>總覽</h1>
    <div class="big" id="netWorth">£0.00</div>
    <div class="sub">
      收入總額：<span class="green" id="incomeTotal">£0.00</span>　｜　
      支出總額：<span class="red" id="expenseTotal">£0.00</span>　｜　
      記錄：<span id="count">0</span> 筆
    </div>
    <div class="sub" style="margin-top:8px;">
      <span class="tag">總資產 = 收入 − 支出</span>
      <span class="tag">類別自動判斷收入/支出</span>
    </div>
  </div>

  <div class="card">
    <h2>新增紀錄</h2>
    <div class="row">
      <div class="col">
        <label>日期</label>
        <input id="date" type="date" />
      </div>

      <div class="col">
        <label>類別（自動決定收入/支出）</label>
        <select id="category">
          <option value="人工">人工（收入）</option>
          <option value="零用">零用（收入）</option>
          <option value="食飯">食飯（支出）</option>
          <option value="交通">交通（支出）</option>
          <option value="額外洗費">額外洗費（支出）</option>
        </select>
        <div class="sub" style="margin-top:6px;">
          呢筆會記做：<span id="typeBadge" class="pill">收入</span>
        </div>
      </div>

      <div class="col">
        <label>金額（只輸入正數）</label>
        <input id="amount" type="number" step="0.01" placeholder="例如：2000 / 8.5" />
      </div>

      <div class="col">
        <label>備註（可選）</label>
        <input id="note" type="text" placeholder="例如：2月人工 / lunch / bus" />
      </div>
    </div>

    <div class="row" style="margin-top:10px;">
      <div class="col"><button id="addBtn">加入</button></div>
      <div class="col"><button class="ghost" id="clearBtn">清空全部</button></div>
    </div>

    <div class="sub" style="margin-top:10px;">
      ✅ 收入：<b>人工、零用</b>（會加）｜ 支出：<b>食飯、交通、額外洗費</b>（會扣）
    </div>
  </div>

  <div class="grid">
    <div class="card">
      <h2>統計（按日 / 週 / 月 / 年）</h2>

      <div class="row">
        <div class="col">
          <label>按日（揀日期）</label>
          <input id="dayPick" type="date" />
        </div>
        <div class="col">
          <label>按週（揀週內任何一日）</label>
          <input id="weekPick" type="date" />
        </div>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col">
          <label>按月（揀月份）</label>
          <input id="monthPick" type="month" />
        </div>
        <div class="col">
          <label>按年（揀年份）</label>
          <input id="yearPick" type="number" min="2000" max="2100" step="1" />
        </div>
      </div>

      <div class="sub" style="margin-top:10px;">
        <span class="pill" id="rangeLabel">範圍：—</span>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col">
          <label>收入</label>
          <input id="rangeIncome" readonly />
        </div>
        <div class="col">
          <label>支出</label>
          <input id="rangeExpense" readonly />
        </div>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col">
          <label>結餘（收入−支出）</label>
          <input id="rangeNet" readonly />
        </div>
        <div class="col">
          <label>（提示）</label>
          <input id="rangeHint" readonly />
        </div>
      </div>

      <table id="rangeCatTable" style="margin-top:10px;"></table>
      <div class="sub" style="margin-top:10px;">
        類別小計：只計你選到嗰個範圍（日/週/月/年）。
      </div>
    </div>

    <div class="card">
      <h2>英國稅務估算（rUK · 2025/26 參考）</h2>

      <div class="row">
        <div class="col">
          <label>估稅基準</label>
          <select id="taxIncomeSource">
            <option value="manual" selected>我自己輸入（真實月薪/週薪）</option>
            <option value="recorded">用「已記錄收入總額」（當作一年）</option>
          </select>
        </div>
        <div class="col">
          <label>收入頻率（換算年收入）</label>
          <select id="incomeFreq">
            <option value="year">每年</option>
            <option value="month" selected>每月</option>
            <option value="week">每週</option>
            <option value="day">每日</option>
          </select>
        </div>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col">
          <label>用嚟估稅嘅「收入金額」</label>
          <input id="incomeForTax" type="number" step="0.01" placeholder="例如：2500（每月）" />
        </div>
        <div class="col">
          <label>Tax code（估 Personal Allowance）</label>
          <input id="taxCode" value="1257L" />
        </div>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col">
          <label>Pension %（供款，唔係稅）</label>
          <input id="pensionRate" type="number" step="0.1" value="5" />
        </div>
        <div class="col">
          <label>NI 類型（簡化）</label>
          <select id="niType">
            <option value="class1" selected>Class 1（僱員常用）</option>
            <option value="class4">Class 4（自僱常見）</option>
          </select>
        </div>
      </div>

      <div class="row" style="margin-top:10px;">
        <div class="col"><button id="recalcBtn">重新計算稅務</button></div>
        <div class="col"><button class="ghost" id="fillFromRecordedBtn">用已記錄收入填入（按你選嘅頻率）</button></div>
      </div>

      <div class="sub" style="margin-top:10px;">
        Personal Allowance：<span class="mono" id="pa">£12,570</span><br>
        年收入（換算後）：<span class="mono" id="annualIncome">£0.00</span>
      </div>

      <table id="taxTable" style="margin-top:10px;"></table>

      <div class="sub" style="margin-top:12px; color:#dc2626;">
        ※ 此為簡化估算工具，非官方稅務建議。請以 HMRC 為準。
      </div>
    </div>
  </div>

  <div class="card">
    <h2>記錄</h2>
    <div class="sub"><span class="pill" id="today"></span></div>
    <ul class="list" id="list"></ul>
  </div>

</div>

<script>
  const LS_KEY = "money_app_v8_auto_date_rollover";

  // ✅ 稅務參數抽成常數（方便你以後更新）
  const TAX = {
    // 2025/26 rUK（簡化）
    PA_DEFAULT: 12570,
    BASIC_LIMIT: 50270,
    HIGHER_LIMIT: 125140,
    BASIC_RATE: 0.20,
    HIGHER_RATE: 0.40,
    ADD_RATE: 0.45,

    // NI thresholds（簡化）
    NI_PT: 12570,
    NI_UEL: 50270,

    // NI rates（重點更新）
    NI_CLASS1_MAIN: 0.08,
    NI_CLASS1_UPPER: 0.02,
    NI_CLASS4_MAIN: 0.06, // ✅ 6%
    NI_CLASS4_UPPER: 0.02,

    WEEKS_PER_YEAR: 52,
    DAYS_PER_YEAR: 365
  };

  const $ = (id) => document.getElementById(id);

  const dateEl = $("date");
  const categoryEl = $("category");
  const amountEl = $("amount");
  const noteEl = $("note");
  const addBtn = $("addBtn");
  const clearBtn = $("clearBtn");

  const typeBadgeEl = $("typeBadge");

  const netWorthEl = $("netWorth");
  const incomeTotalEl = $("incomeTotal");
  const expenseTotalEl = $("expenseTotal");
  const countEl = $("count");

  const listEl = $("list");
  const todayEl = $("today");

  // range stats
  const dayPickEl = $("dayPick");
  const weekPickEl = $("weekPick");
  const monthPickEl = $("monthPick");
  const yearPickEl = $("yearPick");

  const rangeLabelEl = $("rangeLabel");
  const rangeIncomeEl = $("rangeIncome");
  const rangeExpenseEl = $("rangeExpense");
  const rangeNetEl = $("rangeNet");
  const rangeHintEl = $("rangeHint");
  const rangeCatTableEl = $("rangeCatTable");

  // tax
  const taxIncomeSourceEl = $("taxIncomeSource");
  const incomeFreqEl = $("incomeFreq");
  const incomeForTaxEl = $("incomeForTax");
  const taxCodeEl = $("taxCode");
  const pensionRateEl = $("pensionRate");
  const niTypeEl = $("niType");
  const recalcBtn = $("recalcBtn");
  const fillFromRecordedBtn = $("fillFromRecordedBtn");
  const paEl = $("pa");
  const annualIncomeEl = $("annualIncome");
  const taxTableEl = $("taxTable");

  // Rules
  const INCOME_CATS = new Set(["人工", "零用"]);
  const EXPENSE_CATS = new Set(["食飯", "交通", "額外洗費"]);
  const ALL_CATS = ["人工","零用","食飯","交通","額外洗費"];

  function fmtMoney(n) {
    const val = Number(n || 0);
    return val.toLocaleString("en-GB", { style: "currency", currency: "GBP" });
  }

  function ymd(d) {
    const x = new Date(d);
    const mm = String(x.getMonth()+1).padStart(2,"0");
    const dd = String(x.getDate()).padStart(2,"0");
    return `${x.getFullYear()}-${mm}-${dd}`;
  }

  function ym(d) {
    const x = new Date(d);
    const mm = String(x.getMonth()+1).padStart(2,"0");
    return `${x.getFullYear()}-${mm}`;
  }

  function parseYMD(s) {
    const [y,m,d] = s.split("-").map(Number);
    return new Date(y, m-1, d);
  }

  function load() {
    try { return JSON.parse(localStorage.getItem(LS_KEY)) || []; }
    catch { return []; }
  }

  function save(entries) {
    localStorage.setItem(LS_KEY, JSON.stringify(entries));
  }

  function getTypeFromCategory(category) {
    if (INCOME_CATS.has(category)) return "income";
    if (EXPENSE_CATS.has(category)) return "expense";
    return "expense";
  }

  function updateTypeBadge() {
    const type = getTypeFromCategory(categoryEl.value);
    if (type === "income") {
      typeBadgeEl.textContent = "收入（會加）";
      typeBadgeEl.style.background = "#eaffef";
      typeBadgeEl.style.color = "#0f7a31";
    } else {
      typeBadgeEl.textContent = "支出（會扣）";
      typeBadgeEl.style.background = "#ffecec";
      typeBadgeEl.style.color = "#b42318";
    }
  }

  function sumIncomeExpense(entries) {
    let income = 0, expense = 0;
    for (const e of entries) {
      const amt = Number(e.amount || 0);
      if (e.type === "income") income += amt;
      else expense += amt;
    }
    return { income, expense, net: income - expense };
  }

  function renderOverview() {
    const entries = load();
    const s = sumIncomeExpense(entries);
    netWorthEl.textContent = fmtMoney(s.net);
    incomeTotalEl.textContent = fmtMoney(s.income);
    expenseTotalEl.textContent = fmtMoney(s.expense);
    countEl.textContent = String(entries.length);
  }

  function renderList() {
    const entries = load();
    listEl.innerHTML = "";

    [...entries].reverse().forEach((e) => {
      const li = document.createElement("li");
      li.className = "item";

      const left = document.createElement("div");
      left.className = "left";

      const line1 = document.createElement("div");
      const sign = e.type === "income" ? "+" : "-";
      const cls = e.type === "income" ? "green" : "red";
      line1.innerHTML = `<span class="${cls}">${sign}${fmtMoney(e.amount)}</span> · ${e.category}`;

      const meta = document.createElement("div");
      meta.className = "meta";
      meta.textContent = `${e.date} · ${e.time}${e.note ? " · " + e.note : ""}`;

      left.appendChild(line1);
      left.appendChild(meta);

      const del = document.createElement("button");
      del.className = "danger";
      del.textContent = "刪除";
      del.onclick = () => {
        const all = load();
        const idx = all.findIndex(x => x.id === e.id);
        if (idx >= 0) {
          all.splice(idx, 1);
          save(all);
          renderAll();
        }
      };

      li.appendChild(left);
      li.appendChild(del);
      listEl.appendChild(li);
    });
  }

  // ✅ 避免自動覆蓋用戶正在選日期
  let userTouchedDate = false;
  dateEl.addEventListener("change", () => { userTouchedDate = true; });

  function addEntry() {
    const date = dateEl.value;
    const category = categoryEl.value;
    const amount = Number(amountEl.value);
    const note = noteEl.value.trim();

    if (!date) return alert("請揀日期");
    if (!Number.isFinite(amount) || amountEl.value === "" || amount <= 0) return alert("請輸入正數金額（> 0）");

    const type = getTypeFromCategory(category);

    const entry = {
      id: (crypto.randomUUID ? crypto.randomUUID() : String(Date.now()) + Math.random()),
      date,
      type,
      category,
      amount,
      note,
      time: new Date().toLocaleString("zh-HK", { hour12:false })
    };

    const entries = load();
    entries.push(entry);
    save(entries);

    amountEl.value = "";
    noteEl.value = "";
    amountEl.focus();

    // 新增完一筆，通常都係想回到今日（如果你冇手動改過日期）
    if (!userTouchedDate) dateEl.value = ymd(new Date());

    renderAll();
  }

  // ---------- Range stats helpers ----------
  function startOfWeekMonday(d) {
    const x = new Date(d);
    x.setHours(0,0,0,0);
    const day = (x.getDay() + 6) % 7; // Mon=0..Sun=6
    x.setDate(x.getDate() - day);
    return x;
  }

  function endOfWeekSunday(d) {
    const s = startOfWeekMonday(d);
    const e = new Date(s);
    e.setDate(e.getDate() + 6);
    e.setHours(23,59,59,999);
    return e;
  }

  function dateInRange(dateStr, start, end) {
    const d = parseYMD(dateStr);
    return d >= start && d <= end;
  }

  function computeRangeTotals(start, end) {
    const entries = load();

    let inc = 0, exp = 0;
    const sums = Object.fromEntries(ALL_CATS.map(c => [c, 0]));

    for (const e of entries) {
      if (!e.date) continue;
      if (!dateInRange(e.date, start, end)) continue;

      const amt = Number(e.amount || 0);
      sums[e.category] = (sums[e.category] || 0) + amt;

      if (e.type === "income") inc += amt;
      else exp += amt;
    }

    return { inc, exp, net: inc - exp, sums };
  }

  let activeMode = "month";

  function renderRangeStats() {
    const today = new Date();

    let start, end, label;

    if (activeMode === "day") {
      const d = dayPickEl.value ? parseYMD(dayPickEl.value) : today;
      start = new Date(d); start.setHours(0,0,0,0);
      end = new Date(d); end.setHours(23,59,59,999);
      label = `按日：${start.toLocaleDateString("zh-HK")}`;
    } else if (activeMode === "week") {
      const d = weekPickEl.value ? parseYMD(weekPickEl.value) : today;
      start = startOfWeekMonday(d);
      end = endOfWeekSunday(d);
      label = `按週：${start.toLocaleDateString("zh-HK")} → ${end.toLocaleDateString("zh-HK")}`;
    } else if (activeMode === "year") {
      const y = Number(yearPickEl.value) || today.getFullYear();
      start = new Date(y, 0, 1, 0,0,0,0);
      end = new Date(y, 11, 31, 23,59,59,999);
      label = `按年：${y}-01-01 → ${y}-12-31`;
    } else {
      const pick = monthPickEl.value || ym(today);
      const [y, m] = pick.split("-").map(Number);
      start = new Date(y, m-1, 1, 0,0,0,0);
      end = new Date(y, m, 0, 23,59,59,999);
      label = `按月：${pick}`;
    }

    const r = computeRangeTotals(start, end);

    rangeLabelEl.textContent = `範圍：${label}`;
    rangeIncomeEl.value = fmtMoney(r.inc);
    rangeExpenseEl.value = fmtMoney(r.exp);
    rangeNetEl.value = fmtMoney(r.net);

    rangeHintEl.value = (r.net >= 0) ? "✅ 有結餘" : "⚠️ 超支";

    let html = "";
    for (const c of ALL_CATS) {
      const isIncome = INCOME_CATS.has(c);
      html += `<tr><td>${c}${isIncome ? "（收入）" : "（支出）"}</td><td>${fmtMoney(r.sums[c] || 0)}</td></tr>`;
    }
    html += `<tr><td style="font-weight:900;">結餘（收入−支出）</td><td>${fmtMoney(r.net)}</td></tr>`;
    rangeCatTableEl.innerHTML = html;
  }

  // ----- TAX CALC (rUK simplified) -----
  function parsePersonalAllowanceFromTaxCode(code) {
    const m = String(code || "").toUpperCase().match(/^(\d+)/);
    if (!m) return TAX.PA_DEFAULT;
    const n = Number(m[1]);
    if (!Number.isFinite(n) || n <= 0) return TAX.PA_DEFAULT;
    return n * 10;
  }

  function annualizeIncome(amount, freq) {
    const a = Number(amount || 0);
    if (!Number.isFinite(a) || a < 0) return 0;
    if (freq === "year") return a;
    if (freq === "month") return a * 12;
    if (freq === "week") return a * TAX.WEEKS_PER_YEAR;
    if (freq === "day") return a * TAX.DAYS_PER_YEAR;
    return a;
  }

  function deAnnualize(amountAnnual, freq) {
    const a = Number(amountAnnual || 0);
    if (!Number.isFinite(a)) return 0;
    if (freq === "year") return a;
    if (freq === "month") return a / 12;
    if (freq === "week") return a / TAX.WEEKS_PER_YEAR;
    if (freq === "day") return a / TAX.DAYS_PER_YEAR;
    return a;
  }

  function calcIncomeTax_rUK(annualIncome, personalAllowance) {
    let allowance = personalAllowance;
    if (annualIncome > 100000) {
      const reduced = allowance - (annualIncome - 100000) / 2;
      allowance = Math.max(0, reduced);
    }

    const taxable = Math.max(0, annualIncome - allowance);

    const basicUpper = Math.max(0, TAX.BASIC_LIMIT - allowance);
    const higherUpper = Math.max(0, TAX.HIGHER_LIMIT - allowance);

    let tax = 0;
    let remaining = taxable;

    const basicChunk = Math.max(0, Math.min(remaining, basicUpper));
    tax += basicChunk * TAX.BASIC_RATE;
    remaining -= basicChunk;

    const higherChunk = Math.max(0, Math.min(remaining, higherUpper - basicUpper));
    tax += higherChunk * TAX.HIGHER_RATE;
    remaining -= higherChunk;

    tax += Math.max(0, remaining) * TAX.ADD_RATE;

    return { allowance, taxable, tax };
  }

  function calcNI(annualIncome, niType) {
    const PT = TAX.NI_PT;
    const UEL = TAX.NI_UEL;

    const mainBand = Math.max(0, Math.min(annualIncome, UEL) - PT);
    const upperBand = Math.max(0, annualIncome - UEL);

    if (niType === "class4") {
      return mainBand * TAX.NI_CLASS4_MAIN + upperBand * TAX.NI_CLASS4_UPPER;
    }
    return mainBand * TAX.NI_CLASS1_MAIN + upperBand * TAX.NI_CLASS1_UPPER;
  }

  function calcPension(annualIncome, ratePercent) {
    const r = Number(ratePercent || 0);
    if (!Number.isFinite(r) || r < 0) return 0;
    return annualIncome * (r / 100);
  }

  function getRecordedIncomeAnnual() {
    const entries = load();
    const s = sumIncomeExpense(entries);
    return s.income;
  }

  function renderTax() {
    const freq = incomeFreqEl.value;
    const source = taxIncomeSourceEl.value;

    let baseIncome = Number(incomeForTaxEl.value || 0);

    if (source === "recorded") {
      const annualRecorded = getRecordedIncomeAnnual();
      baseIncome = deAnnualize(annualRecorded, freq);
      incomeForTaxEl.value = (Math.round(baseIncome * 100) / 100).toString();
    }

    const annualIncome = annualizeIncome(baseIncome, freq);

    const pa = parsePersonalAllowanceFromTaxCode(taxCodeEl.value);
    paEl.textContent = fmtMoney(pa);
    annualIncomeEl.textContent = fmtMoney(annualIncome);

    const it = calcIncomeTax_rUK(annualIncome, pa);
    const ni = calcNI(annualIncome, niTypeEl.value);
    const pension = calcPension(annualIncome, pensionRateEl.value);

    const totalTax = it.tax + ni;
    const totalDeduct = it.tax + ni + pension;
    const netAfterAll = Math.max(0, annualIncome - totalDeduct);

    const per = (annual, f) => fmtMoney(deAnnualize(annual, f));

    taxTableEl.innerHTML = `
      <tr><td>Personal Allowance（估）</td><td>${fmtMoney(it.allowance)}</td></tr>
      <tr><td>應課稅收入（估）</td><td>${fmtMoney(it.taxable)}</td></tr>

      <tr><td>Income Tax（每年）</td><td>${fmtMoney(it.tax)}</td></tr>
      <tr><td>NI（每年）</td><td>${fmtMoney(ni)}</td></tr>
      <tr><td><span class="red">總稅款 Tax+NI（每年）</span></td><td class="red">${fmtMoney(totalTax)}</td></tr>

      <tr><td>Pension（每年，供款）</td><td>${fmtMoney(pension)}</td></tr>
      <tr><td>總扣款（稅+NI+Pension，每年）</td><td>${fmtMoney(totalDeduct)}</td></tr>
      <tr><td><b>到手（每年）</b></td><td><b>${fmtMoney(netAfterAll)}</b></td></tr>

      <tr><td class="sub" colspan="2" style="border-top:0;padding-top:14px;">
        <span class="pill">每月 / 每週 / 每日</span>
      </td></tr>

      <tr><td><span class="red">總稅款 Tax+NI（每月）</span></td><td class="red">${per(totalTax, "month")}</td></tr>
      <tr><td><span class="red">總稅款 Tax+NI（每週）</span></td><td class="red">${per(totalTax, "week")}</td></tr>
      <tr><td><span class="red">總稅款 Tax+NI（每日）</span></td><td class="red">${per(totalTax, "day")}</td></tr>

      <tr><td>到手（每月）</td><td>${per(netAfterAll, "month")}</td></tr>
      <tr><td>到手（每週）</td><td>${per(netAfterAll, "week")}</td></tr>
      <tr><td>到手（每日）</td><td>${per(netAfterAll, "day")}</td></tr>
    `;
  }

  function fillFromRecordedIncome() {
    taxIncomeSourceEl.value = "recorded";
    renderTax();
  }

  // ✅ 自動更新日期（跨日 rollover）
  function setDefaultPickersToToday(force = false) {
    const now = new Date();

    // 更新「今日」
    todayEl.textContent = now.toLocaleDateString("zh-HK", { year:"numeric", month:"long", day:"numeric" });

    const todayYMD = ymd(now);
    const todayYM = ym(now);
    const todayYear = String(now.getFullYear());

    // 新增紀錄日期：如果你已經手動揀緊日期，就唔覆蓋
    if (force || (!dateEl.value && !userTouchedDate)) dateEl.value = todayYMD;
    if (force || (!userTouchedDate && dateEl.value === ymd(new Date(Date.now() - 24*3600*1000)))) {
      // 如果之前係昨日而你未動過，就更新到今日
      dateEl.value = todayYMD;
    }

    // 統計 picker：如果 force 就硬改；否則只喺空值時補
    if (force || !dayPickEl.value) dayPickEl.value = todayYMD;
    if (force || !weekPickEl.value) weekPickEl.value = todayYMD;
    if (force || !monthPickEl.value) monthPickEl.value = todayYM;
    if (force || !yearPickEl.value) yearPickEl.value = todayYear;
  }

  function startAutoDateRollover() {
    let last = ymd(new Date());
    setInterval(() => {
      const cur = ymd(new Date());
      if (cur !== last) {
        last = cur;
        setDefaultPickersToToday(true);
        renderRangeStats();
        renderTax();
      }
    }, 30000); // 每 30 秒檢查一次
  }

  function renderAll() {
    renderOverview();
    renderList();
    renderRangeStats();
    renderTax();
  }

  // Events
  addBtn.addEventListener("click", addEntry);
  amountEl.addEventListener("keydown", (e) => { if (e.key === "Enter") addEntry(); });

  clearBtn.addEventListener("click", () => {
    if (!confirm("真係要清空所有記錄？清空後無得復原。")) return;
    localStorage.removeItem(LS_KEY);
    renderAll();
  });

  categoryEl.addEventListener("change", updateTypeBadge);

  dayPickEl.addEventListener("change", () => { activeMode = "day"; renderRangeStats(); });
  weekPickEl.addEventListener("change", () => { activeMode = "week"; renderRangeStats(); });
  monthPickEl.addEventListener("change", () => { activeMode = "month"; renderRangeStats(); });
  yearPickEl.addEventListener("change", () => { activeMode = "year"; renderRangeStats(); });

  recalcBtn.addEventListener("click", renderTax);
  fillFromRecordedBtn.addEventListener("click", fillFromRecordedIncome);

  taxIncomeSourceEl.addEventListener("change", renderTax);
  incomeFreqEl.addEventListener("change", renderTax);
  niTypeEl.addEventListener("change", renderTax);
  pensionRateEl.addEventListener("change", renderTax);

  // Init
  activeMode = "month";
  updateTypeBadge();

  // 一開頁即刻 set 今日（force=true 保證一致）
  setDefaultPickersToToday(true);

  // 預設統計 picker（跟今日）
  dayPickEl.value = dayPickEl.value || ymd(new Date());
  weekPickEl.value = weekPickEl.value || ymd(new Date());
  monthPickEl.value = monthPickEl.value || ym(new Date());
  yearPickEl.value = yearPickEl.value || String(new Date().getFullYear());

  // 自動跨日更新
  startAutoDateRollover();

  renderAll();
</script>
</body>
</html>
