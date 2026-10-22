
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101116">
<title>تاون ستي | Town City</title>

<style>
:root {
  --bg: #101116;
  --panel: #191b22;
  --panel2: #20222b;
  --gold: #d6b46a;
  --gold2: #f4dca0;
  --text: #f5f2e9;
  --muted: #aaaab3;
  --border: #383640;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  color: var(--text);
  background:
    radial-gradient(ellipse at top, #29251d 0, transparent 55%),
    var(--bg);
  font-family: Arial, Tahoma, sans-serif;
}

button, input, textarea { font: inherit; }

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  padding: 17px 5%;
  border-bottom: 1px solid var(--border);
  background: #111217ed;
  position: sticky;
  top: 0;
  z-index: 5;
  backdrop-filter: blur(12px);
}

.brand {
  font-weight: 900;
  font-size: 20px;
  color: var(--gold2);
  letter-spacing: 1px;
}

.brand small {
  display: block;
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 3px;
  margin-top: 5px;
}

.header-btn, .back-btn {
  color: var(--gold2);
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 9px;
  padding: 10px 14px;
  cursor: pointer;
}

main {
  width: min(1050px, 92%);
  margin: auto;
  padding-bottom: 50px;
}

.hero {
  text-align: center;
  padding: 55px 12px 36px;
}

.ornament {
  color: var(--gold);
  font-size: 19px;
  letter-spacing: 4px;
}

.hero h1 {
  font-size: clamp(27px, 6vw, 44px);
  margin: 17px 0 12px;
  line-height: 1.6;
}

.hero h1 span { color: var(--gold2); }

.hero p {
  color: var(--muted);
  line-height: 2;
  font-size: 14px;
  max-width: 550px;
  margin: auto;
}

.status {
  display: inline-block;
  color: var(--gold2);
  border: 1px solid #786642;
  background: #c5a35412;
  padding: 7px 13px;
  border-radius: 30px;
  font-size: 12px;
  margin-top: 20px;
}

.section-label {
  color: var(--gold2);
  text-align: center;
  margin: 12px 0 22px;
  font-size: 17px;
}

.cards {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 17px;
}

.card {
  background: linear-gradient(145deg, #202129, #17181f);
  border: 1px solid var(--border);
  border-radius: 17px;
  padding: 28px 12px;
  min-height: 185px;
  text-align: center;
  color: var(--text);
  cursor: pointer;
  transition: .2s;
}

.card:hover {
  border-color: var(--gold);
  transform: translateY(-3px);
  background: #28261f;
}

.card .emoji {
  font-size: 42px;
  display: block;
  margin-bottom: 17px;
}

.card h2 {
  color: var(--gold2);
  font-size: 18px;
  margin: 0 0 9px;
}

.card p {
  color: var(--muted);
  font-size: 12px;
  line-height: 1.8;
  margin: 0;
}

footer {
  border-top: 1px solid var(--border);
  color: var(--muted);
  text-align: center;
  padding: 25px 12px;
  font-size: 12px;
  line-height: 2.2;
}

.page {
  display: none;
  padding: 25px 0 45px;
}

.page.active { display: block; }

.page-heading {
  text-align: center;
  padding: 22px 8px;
}

.page-heading .emoji { font-size: 42px; }

.page-heading h1 {
  color: var(--gold2);
  font-size: 27px;
  line-height: 1.7;
}

.page-heading p {
  color: var(--muted);
  line-height: 2;
  font-size: 14px;
}

.list {
  display: grid;
  gap: 12px;
  margin-top: 22px;
}

.list-btn {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  text-align: right;
  color: var(--text);
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 19px;
  cursor: pointer;
}

.list-btn:hover { border-color: var(--gold); }

.list-btn strong {
  display: block;
  color: var(--gold2);
  margin-bottom: 6px;
}

.list-btn small { color: var(--muted); }

.arrow { color: var(--gold); font-size: 20px; }

.paper {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 22px;
  line-height: 2.1;
  white-space: pre-wrap;
  overflow-wrap: anywhere;
  color: #e7e4dc;
  min-height: 130px;
}

.notice {
  text-align: center;
  color: var(--muted);
  font-size: 12px;
  line-height: 2;
  margin-top: 17px;
}

.chat-box {
  border: 1px solid var(--border);
  border-radius: 15px;
  overflow: hidden;
  background: #14151c;
}

.chat-top {
  background: var(--panel);
  border-bottom: 1px solid var(--border);
  padding: 15px;
  display: flex;
  justify-content: space-between;
  gap: 10px;
  align-items: center;
}

.chat-top strong { color: var(--gold2); }

.chat-top small {
  color: var(--muted);
  display: block;
  margin-top: 5px;
}

.messages {
  height: 310px;
  overflow-y: auto;
  padding: 15px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.message {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 11px;
  padding: 12px;
  max-width: 90%;
  align-self: flex-start;
  overflow-wrap: anywhere;
}

.message .author {
  color: var(--gold2);
  font-size: 12px;
  margin-bottom: 7px;
  font-weight: bold;
}

.message .body {
  white-space: pre-wrap;
  line-height: 1.8;
  font-size: 14px;
}

.message .time {
  color: var(--muted);
  font-size: 10px;
  margin-top: 6px;
}

.chat-compose {
  display: flex;
  gap: 8px;
  padding: 12px;
  border-top: 1px solid var(--border);
}

.chat-compose input {
  flex: 1;
  min-width: 0;
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 9px;
  color: white;
  padding: 12px;
  outline: none;
}

.gold-btn {
  background: var(--gold);
  color: #18140c;
  border: 0;
  border-radius: 9px;
  padding: 11px 14px;
  font-weight: bold;
  cursor: pointer;
}

.voice-panel {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 17px;
  margin-top: 15px;
  text-align: center;
}

.voice-panel p {
  color: var(--muted);
  font-size: 13px;
  line-height: 2;
}

.voice-btn {
  border: 1px solid var(--gold);
  border-radius: 10px;
  background: #c5a35416;
  color: var(--gold2);
  padding: 12px;
  cursor: pointer;
}

.profile-form {
  display: grid;
  gap: 10px;
  margin: 15px 0;
}

.profile-form input {
  padding: 12px;
  background: var(--panel2);
  border: 1px solid var(--border);
  color: white;
  border-radius: 9px;
  width: 100%;
}

@media (min-width: 700px) {
  .cards { grid-template-columns: repeat(4, minmax(0, 1fr)); }
  .card { min-height: 215px; padding-top: 36px; }
  .messages { height: 430px; }
}

@media (max-width: 360px) {
  header { padding: 13px 3%; }
  .brand { font-size: 16px; }
  .header-btn { padding: 9px; }
  .chat-compose { flex-wrap: wrap; }
  .chat-compose input { flex-basis: 100%; }
}
</style>
</head>

<body>

<header>
  <div class="brand">
    ✦ TOWN CITY ✦
    <small>مدينة النظام والقانون</small>
  </div>
  <button class="header-btn" onclick="goHome()">⌂ الرئيسية</button>
</header>

<main>

<!-- الصفحة الرئيسية -->
<section id="home" class="page active">
  <div class="hero">
    <div class="ornament">༺ ━━━━━ ✦ ━━━━━ ༻</div>
    <h1>أهلًا بك في <span>تاون ستي</span></h1>
    <p>
      ✦ بوابتك الرسمية إلى أخبار المدينة وقوانينها ✦
      <br>
      النظام أساس الحكم، والعدل أساس الاستقرار.
    </p>
    <div class="status">◆ البوابة الرسمية للمدينة ◆</div>
  </div>

  <h2 class="section-label">༺ اختر وجهتك ༻</h2>

  <div class="cards">
    <button class="card" onclick="openList('laws')">
      <span class="emoji">📚</span>
      <h2>⚖ قوانين المدينة</h2>
      <p>قوانين الرول والمسؤولين والديسكورد</p>
    </button>

    <button class="card" onclick="openList('news')">
      <span class="emoji">📰</span>
      <h2>✦ أخبار المدينة</h2>
      <p>آخر المستجدات والإعلانات الرسمية</p>
    </button>

    <button class="card" onclick="openPage('social')">
      <span class="emoji">🌐</span>
      <h2>◈ مواقع السيرفر الرسمية</h2>
      <p>بوابات التواصل الرسمية للمدينة</p>
    </button>

    <button class="card" onclick="openPage('chat')">
      <span class="emoji">💬</span>
      <h2>✧ الشات العام</h2>
      <p>مساحة التواصل بين المواطنين</p>
    </button>
  </div>
</section>

<!-- قوائم القوانين والأخبار -->
<section id="list" class="page">
  <button class="back-btn" onclick="goHome()">→ رجوع</button>
  <div class="page-heading">
    <div class="ornament">༺ ✦ ༻</div>
    <h1 id="listTitle">القسم</h1>
    <p id="listDescription">اختر القسم الذي تريد الاطلاع عليه.</p>
  </div>
  <div class="list" id="listItems"></div>
</section>

<!-- صفحات النصوص -->
<section id="article" class="page">
  <button class="back-btn" onclick="goBack()">→ رجوع</button>
  <div class="page-heading">
    <div class="ornament">༺ ━ ✦ ━ ༻</div>
    <h1 id="articleTitle">عنوان الصفحة</h1>
    <p>✦ بوابة تاون ستي الرسمية ✦</p>
  </div>
  <div class="paper" id="articleContent"></div>
  <p class="notice">هذه الصفحة مخصصة للقراءة فقط. تصدر التحديثات من إدارة الموقع.</p>
</section>

<!-- المواقع الرسمية -->
<section id="social" class="page">
  <button class="back-btn" onclick="goHome()">→ رجوع</button>
  <div class="page-heading">
    <div class="emoji">🌐</div>
    <h1>مواقع السيرفر الرسمية</h1>
    <p>جميع البوابات الرسمية لمدينة تاون ستي في مكان واحد.</p>
  </div>
  <div class="paper" id="socialContent">༺ ✦ المواقع الرسمية ✦ ༻

سيتم إضافة روابط الديسكورد ومواقع المدينة الرسمية هنا بعد استلامها من الإدارة.

تنبيه: تأكد من صحة الرابط قبل إدخال أي معلومات شخصية.</div>
</section>

<!-- الشات -->
<section id="chat" class="page">
  <button class="back-btn" onclick="goHome()">→ رجوع</button>
  <div class="page-heading">
    <div class="ornament">༺ ✦ ༻</div>
    <h1>الشات العام</h1>
    <p>ملتقى المواطنين للتواصل والنقاش باحترام.</p>
  </div>

  <div class="profile-form">
    <label for="username">اسمك الظاهر في الشات</label>
    <input id="username" maxlength="24" placeholder="اكتب اسمك هنا">
    <button class="gold-btn" onclick="saveName()">حفظ الاسم</button>
  </div>

  <div class="chat-box">
    <div class="chat-top">
      <div>
        <strong>✦ مجلس المواطنين</strong>
        <small id="chatStatus">وضع تجريبي على هذا الجهاز</small>
      </div>
      <span>💬</span>
    </div>

    <div class="messages" id="messages" aria-live="polite">
      <div class="message">
        <div class="author">إدارة تاون ستي</div>
        <div class="body">أهلًا بكم في الشات العام. يرجى الالتزام بالأدب والاحترام.</div>
      </div>
    </div>

    <form class="chat-compose" id="chatForm">
      <input id="messageInput" maxlength="500"
        placeholder="اكتب رسالتك..." autocomplete="off"
        aria-label="نص الرسالة">
      <button class="gold-btn" type="submit">إرسال</button>
    </form>
  </div>

  <div class="voice-panel">
    <h3>🎙 المجلس الصوتي</h3>
    <p>
      هذه الواجهة تمهيدية فقط. الاتصال الصوتي الحقيقي بين المواطنين
      يحتاج إلى خدمة صوتية وخادم متصل بالإنترنت.
    </p>
    <button class="voice-btn" onclick="voiceInfo()">
      معلومات الاتصال الصوتي
    </button>
    <p id="voiceStatus"></p>
  </div>

  <p class="notice">
    النسخة الحالية تعرض رسائلك محليًا على جهازك فقط.
    لا ترسل معلومات شخصية أو كلمات مرور.
  </p>
</section>

</main>

<footer>
  <div class="ornament">༺ ━━━━━ ✦ ━━━━━ ༻</div>
  <strong>✦ TOWN CITY | تاون ستي ✦</strong>
  <br>
  النظام • العدالة • المسؤولية
  <br>
  جميع الحقوق محفوظة لإدارة المدينة © 2026
</footer>

<script>
const sections = ["home", "list", "article", "social", "chat"];
let previousPage = "list";

const data = {
  laws: {
    title: "⚖ قوانين المدينة",
    description: "الأنظمة والتعليمات المعتمدة في تاون ستي.",
    items: [
      ["📜", "قوانين الرول", "قواعد تقمص الأدوار داخل المدينة"],
      ["💠", "قوانين الديسكورد", "قواعد مجتمع الديسكورد"],
      ["🏛️", "قوانين المسؤولين", "واجبات وصلاحيات المسؤولين"]
    ]
  },
  news: {
    title: "📰 الأخبار والإعلانات",
    description: "تابع آخر أخبار المدينة والسيرفر.",
    items: [
      ["🏙️", "أخبار المدينة", "القرارات والمستجدات المحلية"],
      ["🎮", "أخبار السيرفر", "التحديثات والإعلانات داخل اللعبة"],
      ["💠", "أخبار الديسكورد", "الإعلانات الخاصة بمجتمع الديسكورد"]
    ]
  }
};

const articles = {
  "قوانين الرول": "سيتم إضافة قوانين الرول الرسمية هنا لاحقًا.",
  "قوانين الديسكورد": "سيتم إضافة قوانين الديسكورد الرسمية هنا لاحقًا.",
  "قوانين المسؤولين": "سيتم إضافة قوانين المسؤولين الرسمية هنا لاحقًا.",
  "أخبار المدينة": "سيتم إضافة أخبار المدينة وإعلاناتها هنا لاحقًا.",
  "أخبار السيرفر": "سيتم إضافة أخبار السيرفر وتحديثاته هنا لاحقًا.",
  "أخبار الديسكورد": "سيتم إضافة أخبار الديسكورد هنا لاحقًا."
};

function openPage(id) {
  sections.forEach(function (section) {
    document.getElementById(section).classList.remove("active");
  });
  document.getElementById(id).classList.add("active");
  window.scrollTo({ top: 0, behavior: "smooth" });
}

function goHome() {
  openPage("home");
}

function openList(type) {
  const section = data[type];
  if (!section) return;

  document.getElementById("listTitle").textContent = section.title;
  document.getElementById("listDescription").textContent =
    section.description;

  const container = document.getElementById("listItems");
  container.replaceChildren();

  section.items.forEach(function (item) {
    const button = document.createElement("button");
    button.className = "list-btn";

    const text = document.createElement("div");
    const title = document.createElement("strong");
    const desc = document.createElement("small");

    title.textContent = item[0] + " " + item[1];
    desc.textContent = item[2];
    text.append(title, desc);

    const arrow = document.createElement("span");
    arrow.className = "arrow";
    arrow.textContent = "‹";

    button.append(text, arrow);
    button.addEventListener("click", function () {
      previousPage = "list";
      openArticle(item[1]);
    });

    container.appendChild(button);
  });

  openPage("list");
}

function openArticle(title) {
  document.getElementById("articleTitle").textContent = title;
  document.getElementById("articleContent").textContent =
    articles[title] || "سيتم إضافة المحتوى الرسمي لاحقًا.";
  openPage("article");
}

function goBack() {
  openPage(previousPage);
}

function saveName() {
  const field = document.getElementById("username");
  const name = field.value.trim();

  if (!name) {
    alert("اكتب اسمًا أولًا.");
    return;
  }

  try {
    localStorage.setItem("townCityName", name);
  } catch (error) {
    // Storage may be unavailable in some browsers.
  }

  alert("تم حفظ الاسم على هذا الجهاز إن كان التخزين متاحًا.");
}

try {
  document.getElementById("username").value =
    localStorage.getItem("townCityName") || "";
} catch (error) {
  // Continue without local storage.
}

document.getElementById("chatForm").addEventListener(
  "submit",
  function (event) {
    event.preventDefault();

    const input = document.getElementById("messageInput");
    const message = input.value.trim();
    let name = document.getElementById("username").value.trim();

    if (!message) return;

    if (!name) name = "مواطن";

    const bubble = document.createElement("div");
    bubble.className = "message";

    const author = document.createElement("div");
    author.className = "author";
    author.textContent = name;

    const body = document.createElement("div");
    body.className = "body";
    body.textContent = message;

    const time = document.createElement("div");
    time.className = "time";
    time.textContent = new Date().toLocaleTimeString("ar", {
      hour: "2-digit",
      minute: "2-digit"
    });

    bubble.append(author, body, time);

    const messages = document.getElementById("messages");
    messages.appendChild(bubble);
    messages.scrollTop = messages.scrollHeight;

    input.value = "";
    input.focus();
  }
);

function voiceInfo() {
  document.getElementById("voiceStatus").textContent =
    "الاتصال الصوتي غير مفعّل بعد. سنحتاج إلى إعداد خدمة صوتية وربطها بالموقع.";
}
</script>

</body>
</html>
