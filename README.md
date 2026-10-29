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

.chat-box {
  border: 1px solid var(--border);
  border-radius: 15px;
  overflow: hidden;
  background: #14151c;
  margin-top: 20px;
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

.messages {
  height: 380px;
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
  max-width: 85%;
  align-self: flex-start;
  overflow-wrap: anywhere;
}

.message .author {
  color: var(--gold2);
  font-size: 12px;
  margin-bottom: 5px;
  font-weight: bold;
}

.message .body {
  white-space: pre-wrap;
  line-height: 1.6;
  font-size: 14px;
}

.message .time {
  color: var(--muted);
  font-size: 10px;
  margin-top: 6px;
  text-align: left;
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

.profile-form {
  display: flex;
  gap: 10px;
  margin-bottom: 15px;
}

.profile-form input {
  flex: 1;
  padding: 12px;
  background: var(--panel2);
  border: 1px solid var(--border);
  color: white;
  border-radius: 9px;
}

@media (min-width: 700px) {
  .cards { grid-template-columns: repeat(4, minmax(0, 1fr)); }
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

<section id="home" class="page active">
  <div class="hero">
    <div class="ornament">༺ ━━━━━ ✦ ━━━━━ ༻</div>
    <h1>أهلًا بك في <span>تاون ستي</span></h1>
    <p>بوابتك الرسمية إلى أخبار المدينة وقوانينها</p>
    <div class="status">◆ البوابة الرسمية للمدينة ◆</div>
  </div>

  <div class="cards">
    <button class="card" onclick="openPage('chat')">
      <span class="emoji">💬</span>
      <h2>✧ الشات العام</h2>
      <p>مساحة التواصل الحية بين المواطنين</p>
    </button>
  </div>
</section>

<!-- صفحة الشات العام المباشر -->
<section id="chat" class="page">
  <button class="back-btn" onclick="goHome()">→ رجوع</button>
  <div class="page-heading">
    <div class="ornament">༺ ✦ ༻</div>
    <h1>الشات العام المباشر</h1>
    <p>الرسائل محفوظة ومباشرة للجميع</p>
  </div>

  <div class="profile-form">
    <input id="username" maxlength="24" placeholder="اسمك في الشات...">
    <button class="gold-btn" onclick="saveName()">حفظ الاسم</button>
  </div>

  <div class="chat-box">
    <div class="chat-top">
      <strong>✦ مجلس المواطنين الحي</strong>
      <span id="chatStatus">🟢 متصل</span>
    </div>

    <div class="messages" id="messages">
      <!-- الرسائل ستظهر هنا مباشرة -->
    </div>

    <form class="chat-compose" id="chatForm">
      <input id="messageInput" maxlength="500" placeholder="اكتب رسالتك..." autocomplete="off">
      <button class="gold-btn" type="submit">إرسال</button>
    </form>
  </div>
</section>

</main>

<script>
const JSONBIN_BIN_ID = "6ada2e1bffd5d1605383153c"; 
const JSONBIN_API_KEY = "$2a$10$1Sbd.5T.7yoq3HH2ykIIw.Em2vYJBJmV3FEoOFobo63w/ghIRunv2"; 
const DISCORD_WEBHOOK_URL = "https://discord.com/api/webhooks/1562853512763801741/ky9MpmYs4u5715hls7bwzFD-HE_YcQp1lUYAjGiUgQ-z9Qhz-a3h3H8h9CM8pX063mZb";

const JSONBIN_URL = `https://api.jsonbin.io/v3/b/${JSONBIN_BIN_ID}`;

async function loadMessages() {
  try {
    const response = await fetch(JSONBIN_URL, {
      headers: { "X-Master-Key": JSONBIN_API_KEY }
    });
    const data = await response.json();
    const messages = data.record || [];
    
    const messagesDiv = document.getElementById("messages");
    messagesDiv.innerHTML = "";

    messages.forEach(msg => {
      displayMessage(msg.name, msg.text, msg.time);
    });
  } catch (err) {
    console.error("خطأ في جلب الرسائل:", err);
  }
}

loadMessages();
setInterval(loadMessages, 4000);

function openPage(id) {
  document.querySelectorAll(".page").forEach(p => p.classList.remove("active"));
  document.getElementById(id).classList.add("active");
  window.scrollTo({ top: 0, behavior: "smooth" });
}

function goHome() { openPage("home"); }

function saveName() {
  const name = document.getElementById("username").value.trim();
  if (name) {
    localStorage.setItem("townCityName", name);
    alert("تم حفظ اسمك بنجاح!");
  }
}

document.getElementById("username").value = localStorage.getItem("townCityName") || "";

document.getElementById("chatForm").addEventListener("submit", async function (e) {
  e.preventDefault();
  const input = document.getElementById("messageInput");
  const text = input.value.trim();
  let name = document.getElementById("username").value.trim() || "مواطن";

  if (!text) return;

  const timeStr = new Date().toLocaleTimeString("ar", { hour: "2-digit", minute: "2-digit" });
  input.value = "";

  try {
    const getRes = await fetch(JSONBIN_URL, {
      headers: { "X-Master-Key": JSONBIN_API_KEY }
    });
    const getData = await getRes.json();
    let currentMessages = getData.record || [];

    currentMessages.push({ name: name, text: text, time: timeStr });

    await fetch(JSONBIN_URL, {
      method: "PUT",
      headers: {
        "Content-Type": "application/json",
        "X-Master-Key": JSONBIN_API_KEY
      },
      body: JSON.stringify(currentMessages)
    });

    displayMessage(name, text, timeStr);
  } catch (err) {
    console.error("خطأ في حفظ الرسالة:", err);
  }

  if (DISCORD_WEBHOOK_URL) {
    fetch(DISCORD_WEBHOOK_URL, {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({
        username: name + " (من الموقع)",
        content: text
      })
    }).catch(err => console.error("Discord error:", err));
  }
});

function displayMessage(name, text, time) {
  const messagesDiv = document.getElementById("messages");
  const bubble = document.createElement("div");
  bubble.className = "message";
  bubble.innerHTML = `
    <div class="author">${escapeHtml(name)}</div>
    <div class="body">${escapeHtml(text)}</div>
    <div class="time">${time}</div>
  `;
  messagesDiv.appendChild(bubble);
  messagesDiv.scrollTop = messagesDiv.scrollHeight;
}

function escapeHtml(str) {
  return str.replace(/[&<>"']/g, match => ({
    '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;'
  }[match]));
}
</script>

</body>
<!-- قسم قوانين الدولة القضائية -->
<div class="laws-box" style="background: #111214; border: 2px solid #b8860b; border-radius: 12px; padding: 15px; margin-bottom: 20px; color: #fff; font-family: 'Cairo', sans-serif; box-shadow: 0 4px 15px rgba(184, 134, 11, 0.3);">
    
    <!-- صورة فخمة وقضائية -->
    <div style="text-align: center; margin-bottom: 10px;">
        <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?q=80&w=600&auto=format&fit=crop" alt="القضاء والعدالة" style="width: 100%; height: 120px; object-fit: cover; border-radius: 8px; border: 1px solid #b8860b;">
    </div>

    <!-- العنوان المزخرف -->
    <h3 style="text-align: center; color: #ffd700; font-size: 18px; margin-bottom: 15px; text-shadow: 0 2px 4px rgba(0,0,0,0.5);">
        ⚖️ ┋ آلتـشـريـعـات والقـوانـيـن القضـائـيـة ┋ ⚖️
    </h3>

    <!-- القائمة الطويلة للمواد القضائية -->
    <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
        <summary style="font-weight: bold; color: #ffdf00;">📜 الباب الأول: الجرائم الموجهة ضد الأفراد (الجنايات)</summary>
        <p style="font-size: 13px; color: #ccc; margin-top: 8px; line-height: 1.6;">
            <strong>المادة رقم (1) - القتل العمد:</strong> يُعاقب كل من تسبب عمداً في إزهاق روح شخص آخر بالسجن لمدة مشددة وغرامة مالية باهظة وتحويله فوراً للمحاكمة العسكرية أو الجنائية العليا.<br>
            <strong>المادة رقم (2) - الشروع في القتل والإيذاء البليغ:</strong> الاعتداء بالسلاح الأبيض أو الناري على أي مواطن أو رجل أمن يُعتبر جناية كبرى تستوجب إيقاف الرخصة وسحب الأسلحة فوراً.<br>
            <strong>المادة رقم (3) - الاحتجاز أو الاختطاف:</strong> يُحظر تماماً تقييد حرية أي شخص أو حجزه قسراً دون إذن قضائي أو صلاحية قانونية مخولة لجهات الامن.
        </p>
    </details>

    <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
        <summary style="font-weight: bold; color: #ffdf00;">🚗 الباب الثاني: المخالفات المرورية والجرائم الواقعة على الطرق</summary>
        <p style="font-size: 13px; color: #ccc; margin-top: 8px; line-height: 1.6;">
            <strong>المادة رقم (4) - القيادة المتهورة وعكس الاتجاه:</strong> يُعاقب كل قائد مركبة يعرض حياة المارة أو الدوريات للخطر بالسحب الفوري للمركبة وحجز رخصة القيادة.<br>
            <strong>المادة رقم (5) - الهروب من الدوريات الأمنية (الـ Pit Maneuver / Evasion):</strong> الهروب من نقطة تفتيش أو تجاهل أوامر التوقف الصادرة من القطاع العسكري أو الشرطي يضاعف قيمة المخالفة ويستوجب التوقيف الفوري.<br>
            <strong>المادة رقم (6) - التخريب المتعمد للممتلكات العامة:</strong> صدم أعمدة الإنارة، الإشارات، أو سيارات الخدمة العامة بقصد التخريب يعرض مرتكبها لغرامة تعويضية وتوقيف مدني.
        </p>
    </details>

    <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
        <summary style="font-weight: bold; color: #ffdf00;">🛡️ الباب الثالث: الجرائم الأمنية والتعامل مع الجهات الرسمية</summary>
        <p style="font-size: 13px; color: #ccc; margin-top: 8px; line-height: 1.6;">
            <strong>المادة رقم (7) - إهانة موظف عام أثناء تأدية عمله:</strong> يُحظر تماماً التاول أو الإساءة اللفظية أو الجسدية لأي رجل أمن (شرطة، إسعاف، إطفاء، أو قضاء) أثناء أداء مهامه الرسمية.<br>
            <strong>المادة رقم (8) - حيازة الأسلحة غير المرخصة أو الممنوعة:</strong> يُمنع منعاً باتاً حمل الأسلحة الحربية أو غير المرخصة في الأماكن العامة الحيوية ويحق للشرطة التفتيش عند الاشتباه.<br>
            <strong>المادة رقم (9) - عرقلة العدالة والهروب من قاعة المحكمة:</strong> محاولة الهروب أثناء المحاكمة أو التأثير على سير الإجراءات القضائية يعتبر جريمة مستقلة تغلظ العقوبة الأصلية.
        </p>
    </details>

    <details style="background: #1a1b1e; padding: 10px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
        <summary style="font-weight: bold; color: #ffdf00;">💼 الباب الرابع: التجارة والأعمال الاقتصادية داخل المدينة</summary>
        <p style="font-size: 13px; color: #ccc; margin-top: 8px; line-height: 1.6;">
            <strong>المادة رقم (10) - ممارسة التجارة والصفقات الرسمية:</strong> يجب أن تكون جميع الأنشطة التجارية والصفقات المالية داخل المدينة وفق النطاق القانوني المعترف به من الدولة.<br>
            <strong>المادة رقم (11) - الرشوة واستغلال النفوذ:</strong> يُمنع منعاً باتاً تقديم أو قبول رشاوى مالية أو عينية لتخفيف الأحكام أو الهروب من العقوبات القانونية.
        </p>
    </details>

</div>

</html>
