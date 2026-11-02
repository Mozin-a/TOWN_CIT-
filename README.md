
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نظام الدكتاتوري كيلر</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap');

:root {
  --red: #a00000;
  --gold: #c9a44c;
  --black: #090909;
  --panel: #151515;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Cairo', sans-serif;
  background: var(--black);
  color: #eee;
  min-height: 100vh;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  z-index: -1;
  background:
    radial-gradient(circle at 50% 10%, #4b000033, transparent 45%),
    linear-gradient(135deg, #090909, #180606, #080808);
}

header {
  min-height: 340px;
  padding: 75px 20px 55px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-bottom: 1px solid #7b0000;
  background:
    linear-gradient(#0009, #000d),
    url("https://images.unsplash.com/photo-1519608487953-e999c86e7455?w=1600")
    center/cover;
}

.emblem {
  font-size: 55px;
  color: var(--gold);
  text-shadow: 0 0 25px #b00000;
}

header h1 {
  font-size: clamp(25px, 5vw, 43px);
  color: #fff;
  margin-top: 12px;
  text-shadow: 0 0 15px #a00000;
}

header p {
  color: #c9a44c;
  margin-top: 12px;
  letter-spacing: 2px;
}

.line {
  width: 130px;
  height: 3px;
  background: var(--red);
  margin: 20px auto;
  box-shadow: 0 0 15px red;
}

.container {
  width: min(1100px, 92%);
  margin: 45px auto;
}

.section-title {
  text-align: center;
  margin-bottom: 30px;
  color: var(--gold);
  font-size: 25px;
}

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
}

.card {
  position: relative;
  min-height: 220px;
  border: 1px solid #522020;
  border-radius: 12px;
  overflow: hidden;
  cursor: pointer;
  background: var(--panel);
  transition: .3s;
}

.card:hover {
  transform: translateY(-7px);
  border-color: var(--gold);
  box-shadow: 0 0 25px #a0000044;
}

.card-image {
  height: 135px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 65px;
  background:
    linear-gradient(#0005, #000b),
    var(--image) center/cover;
}

.card-info {
  padding: 13px;
  text-align: center;
}

.card-info h3 {
  color: var(--gold);
  font-size: 18px;
}

.card-info p {
  color: #aaa;
  font-size: 12px;
  margin-top: 5px;
}

.page {
  display: none;
  animation: appear .35s ease;
}

.page.active {
  display: block;
}

@keyframes appear {
  from { opacity: 0; transform: translateY(15px); }
  to { opacity: 1; transform: translateY(0); }
}

.back {
  background: #790000;
  color: white;
  border: 1px solid var(--gold);
  padding: 10px 25px;
  border-radius: 7px;
  cursor: pointer;
  font-family: inherit;
  margin-bottom: 25px;
}

.back:hover {
  background: #a00000;
}

.law-box {
  background: #141414;
  border-right: 4px solid var(--red);
  padding: 17px;
  border-radius: 7px;
  margin-bottom: 12px;
  line-height: 1.9;
  box-shadow: 0 4px 12px #0005;
}

.law-box strong {
  color: var(--gold);
}

.page h2 {
  color: var(--gold);
  margin-bottom: 25px;
  font-size: 26px;
}

footer {
  border-top: 1px solid #4b0000;
  text-align: center;
  padding: 25px;
  color: #777;
  margin-top: 60px;
  font-size: 13px;
}

footer span {
  color: var(--gold);
}

@media(max-width:500px) {
  header { min-height: 290px; }
  .cards { grid-template-columns: 1fr 1fr; gap: 12px; }
  .card { min-height: 190px; }
  .card-image { height: 110px; font-size: 48px; }
  .card-info h3 { font-size: 15px; }
}
</style>
</head>

<body>

<header>
  <div class="emblem">♛</div>
  <h1>أهلاً بك في نظام الدكتاتوري كيلر</h1>
  <div class="line"></div>
  <p>القانون • السلطة • النظام • الدولة</p>
</header>

<main class="container">

<!-- الصفحة الرئيسية -->
<section id="home" class="page active">
  <h2 class="section-title">▰ الأرشيف القانوني للدولة ▰</h2>

  <div class="cards">

    <div class="card" onclick="openPage('constitution')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1507842217343-583bb7270b66?w=700')">📜</div>
      <div class="card-info">
        <h3>القوانين الدستورية</h3>
        <p>الحاكم والصلاحيات ونظام الدولة</p>
      </div>
    </div>

    <div class="card" onclick="openPage('military')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1519074069444-1ba4fff66d16?w=700')">🎖️</div>
      <div class="card-info">
        <h3>القوانين العسكرية</h3>
        <p>الرتب والانضباط والقيادة</p>
      </div>
    </div>

    <div class="card" onclick="openPage('service')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1503919005314-30d93d07d823?w=700')">🪖</div>
      <div class="card-info">
        <h3>قوانين التجنيد الإجباري</h3>
        <p>الخدمة العسكرية والخدمة المدنية</p>
      </div>
    </div>

    <div class="card" onclick="openPage('police')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1453873531674-2151bcd01707?w=700')">🚔</div>
      <div class="card-info">
        <h3>قوانين الشرطة والأمن</h3>
        <p>الاعتقال والتحقيق والأمن الداخلي</p>
      </div>
    </div>

    <div class="card" onclick="openPage('court')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?w=700')">⚖️</div>
      <div class="card-info">
        <h3>القوانين القضائية</h3>
        <p>المحاكم والأحكام والاستئناف</p>
      </div>
    </div>

    <div class="card" onclick="openPage('crime')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1505664194779-8beaceb93744?w=700')">⛓️</div>
      <div class="card-info">
        <h3>قانون الجرائم والعقوبات</h3>
        <p>الجرائم والغرامات والسجن</p>
      </div>
    </div>

    <div class="card" onclick="openPage('traffic')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=700')">🚦</div>
      <div class="card-info">
        <h3>قوانين المرور</h3>
        <p>المركبات والمخالفات المرورية</p>
      </div>
    </div>

    <div class="card" onclick="openPage('government')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?w=700')">🏛️</div>
      <div class="card-info">
        <h3>قوانين الوزارات</h3>
        <p>المؤسسات والوزراء والوظائف</p>
      </div>
    </div>

    <div class="card" onclick="openPage('emergency')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1519608487953-e999c86e7455?w=700')">🚨</div>
      <div class="card-info">
        <h3>قانون الطوارئ</h3>
        <p>الأحكام الاستثنائية وحالة الطوارئ</p>
      </div>
    </div>

    <div class="card" onclick="openPage('citizens')">
      <div class="card-image" style="--image:url('https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?w=700')">👥</div>
      <div class="card-info">
        <h3>حقوق وواجبات المواطنين</h3>
        <p>الحقوق العامة والالتزامات</p>
      </div>
    </div>

  </div>
</section>

<!-- صفحات القوانين -->
<section id="constitution" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>📜 القوانين الدستورية</h2>
  <div id="constitution-laws"></div>
</section>

<section id="military" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🎖️ القوانين العسكرية</h2>
  <div id="military-laws"></div>
</section>

<section id="service" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🪖 قوانين التجنيد الإجباري والخدمة المدنية</h2>
  <div id="service-laws"></div>
</section>

<section id="police" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🚔 قوانين الشرطة والأمن</h2>
  <div id="police-laws"></div>
</section>

<section id="court" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>⚖️ القوانين القضائية</h2>
  <div id="court-laws"></div>
</section>

<section id="crime" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>⛓️ قانون الجرائم والعقوبات</h2>
  <div id="crime-laws"></div>
</section>

<section id="traffic" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🚦 قوانين المرور</h2>
  <div id="traffic-laws"></div>
</section>

<section id="government" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🏛️ قوانين الوزارات</h2>
  <div id="government-laws"></div>
</section>

<section id="emergency" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>🚨 قانون الطوارئ</h2>
  <div id="emergency-laws"></div>
</section>

<section id="citizens" class="page">
  <button class="back" onclick="goHome()">← العودة للرئيسية</button>
  <h2>👥 حقوق وواجبات المواطنين</h2>
  <div id="citizens-laws"></div>
</section>

</main>

<footer>
  <p>جميع الحقوق محفوظة © <span>نظام الدكتاتوري كيلر</span></p>
  <p>الأرشيف الرسمي للقوانين والمراسيم السيادية</p>
</footer>

<script>
const laws = {
  constitution: [
    ["المادة 1","الحاكم الأعلى هو رأس الدولة وصاحب السلطة التنفيذية العليا."],
    ["المادة 2","تُصدر القرارات السيادية باسم الحاكم الأعلى."],
    ["المادة 3","يحق للحاكم تعيين الوزراء وقادة المؤسسات وعزلهم."],
    ["المادة 4","تلتزم جميع المؤسسات بتنفيذ المراسيم الرسمية."],
    ["المادة 5","الحاكم هو القائد الأعلى للقوات المسلحة."],
    ["المادة 6","يُحظر إنشاء سلطة مستقلة عن مؤسسات الدولة."],
    ["المادة 7","يتولى مجلس الدولة متابعة شؤون المؤسسات الحكومية."],
    ["المادة 8","يُعد الدستور المرجع الأعلى لتنظيم شؤون الدولة."]
  ],

  military: [
    ["المادة 21","القوات المسلحة هي المؤسسة المسؤولة عن الدفاع عن الدولة."],
    ["المادة 22","يتولى الحاكم منصب القائد الأعلى للقوات المسلحة."],
    ["المادة 23","يشرف وزير الدفاع على تنظيم القوات المسلحة."],
    ["المادة 24","يجب احترام الرتب والتسلسل القيادي."],
    ["المادة 25","يُحظر انتحال رتبة عسكرية."],
    ["المادة 26","يُحظر ترك الموقع العسكري دون إذن."],
    ["المادة 27","يجب المحافظة على الممتلكات والمعدات العسكرية."],
    ["المادة 28","يُحظر تسريب المعلومات العسكرية السرية."],
    ["المادة 29","تُحال المخالفات العسكرية الجسيمة إلى المحكمة العسكرية."]
  ],

  service: [
    ["المادة 266","تكون مدة الخدمة العسكرية الإلزامية خمسة أيام."],
    ["المادة 267","يخضع المواطنون المشمولون للاستدعاء الرسمي."],
    ["المادة 268","يُحوّل المواطن الذي لديه إعاقة أو عائق يمنعه من الخدمة العسكرية إلى الخدمة المدنية."],
    ["المادة 269","تكون مدة الخدمة المدنية أربعة أيام."],
    ["المادة 270","اليوم الأول مخصص لصيانة سيارات المواطنين والطرق والإشارات المرورية."],
    ["المادة 271","اليوم الثاني مخصص لنقل أفراد القوات المسلحة إلى المستشفى بمركبات الدولة."],
    ["المادة 272","اليوم الثالث مخصص لنقل الإمدادات إلى الوحدات العسكرية."],
    ["المادة 273","اليوم الرابع مخصص للعمل في إحدى المنشآت الحكومية التي تحددها الدولة."],
    ["المادة 274","يُمنح المواطن شهادة إتمام بعد إكمال الخدمة."],
    ["المادة 275","يُسجل التغيب دون عذر كمخالفة للخدمة الوطنية."],
    ["المادة 276","يُحال الرافض أو الهارب إلى الجهات المختصة."],
    ["المادة 277","تكون عقوبة التهرب المتعمد يوماً كاملاً من الحبس وفق نظام السجن."],
    ["المادة 278","بعد الحبس، يُلزم المخالف بإكمال الخدمة المدنية ثم يومين إضافيين من الخدمة العسكرية."],
    ["المادة 279","تتولى وزارة الدفاع الإشراف على تنفيذ الخدمة الوطنية."]
  ],

  police: [
    ["المادة 91","الشرطة هي المؤسسة المسؤولة عن الأمن الداخلي."],
    ["المادة 92","تخضع الشرطة لوزارة الداخلية."],
    ["المادة 93","يجب توضيح سبب الاعتقال للموقوف."],
    ["المادة 94","يُحظر الاعتقال دون سبب قانوني."],
    ["المادة 95","يجب توثيق عمليات القبض والتفتيش."],
    ["المادة 96","يُحظر تلفيق التهم للمواطنين."],
    ["المادة 97","تُحال التجاوزات الشرطية إلى التحقيق."]
  ],

  court: [
    ["المادة 161","مجلس القضاء الأعلى هو الجهة المشرفة على المحاكم."],
    ["المادة 162","يجب على القاضي الالتزام بالإجراءات القضائية."],
    ["المادة 163","يحق للمتهم معرفة التهمة الموجهة إليه."],
    ["المادة 164","يحق للمتهم تقديم دفاعه والأدلة."],
    ["المادة 165","يجب تسبيب الأحكام القضائية."],
    ["المادة 166","يجوز استئناف الأحكام وفق النظام القضائي."],
    ["المادة 167","تختص المحكمة العسكرية بالنظر في الجرائم العسكرية."]
  ],

  crime: [
    ["المادة 131","يُعاقب مرتكب القتل العمد وفق جسامة الجريمة والأدلة."],
    ["المادة 132","يُعاقب مرتكب الاختطاف واحتجاز الرهائن."],
    ["المادة 133","يُعاقب مرتكب السطو المسلح."],
    ["المادة 134","يُعاقب مرتكب السرقة والاحتيال."],
    ["المادة 135","يُعاقب مرتكب الابتزاز والتهديد."],
    ["المادة 136","يُحظر تزوير الوثائق الرسمية."],
    ["المادة 137","يُحظر اختلاس الأموال العامة."],
    ["المادة 138","تُحدد العقوبات وفق الأدلة وجسامة الفعل."]
  ],

  traffic: [
    ["المادة 201","الالتزام بالإشارات المرورية واجب على جميع السائقين."],
    ["المادة 202","يُحظر تجاوز السرعة المحددة."],
    ["المادة 203","يُحظر تجاوز الإشارة الحمراء."],
    ["المادة 204","يُحظر القيادة عكس اتجاه السير."],
    ["المادة 205","يجب إعطاء الأولوية لمركبات الطوارئ."],
    ["المادة 206","يُحظر الهروب من الشرطة بعد أمر التوقف القانوني."],
    ["المادة 207","يجب الالتزام بتعليمات رجال المرور."]
  ],

  government: [
    ["المادة 181","تتولى وزارة الداخلية تنظيم شؤون الأمن الداخلي."],
    ["المادة 186","تتولى وزارة المالية إدارة الأموال العامة."],
    ["المادة 191","تتولى وزارة الصحة تنظيم الخدمات الطبية."],
    ["المادة 196","تتولى وزارة النقل تنظيم حركة النقل."],
    ["المادة 71","وزير الدفاع هو المسؤول الإداري الأعلى عن الوزارة."],
    ["المادة 73","يلتزم الوزراء بتقديم تقارير دورية إلى الحاكم."]
  ],

  emergency: [
    ["المادة 111","يحق للحاكم إعلان حالة الطوارئ عند وجود خطر جسيم يهدد أمن الدولة."],
    ["المادة 112","يجب تحديد أسباب إعلان الطوارئ."],
    ["المادة 113","يُعلن قرار الطوارئ رسمياً."],
    ["المادة 114","يجوز تشكيل مجلس طوارئ برئاسة الحاكم."],
    ["المادة 115","تتولى المؤسسات تنفيذ التدابير الداخلة ضمن اختصاصها."],
    ["المادة 116","تُراجع التدابير الاستثنائية عند انتهاء أسبابها."]
  ],

  citizens: [
    ["المادة 216","يلتزم المواطن باحترام قوانين الدولة."],
    ["المادة 217","يحق للمواطن الحصول على معاملة عادلة."],
    ["المادة 218","يحق للمواطن تقديم شكوى ضد أي مسؤول."],
    ["المادة 219","يُحظر الاعتداء على المواطنين دون مسوغ قانوني."],
    ["المادة 220","يلتزم المواطن بالمحافظة على الممتلكات العامة."],
    ["المادة 221","يخضع جميع المواطنين للقانون دون استثناء."]
  ]
};

function renderLaws() {
  for (const [section, items] of Object.entries(laws)) {
    const target = document.getElementById(section + "-laws");
    target.innerHTML = items.map(item => `
      <div class="law-box">
        <strong>${item[0]}</strong>
        <p>${item[1]}</p>
      </div>
    `).join("");
  }
}

function openPage(id) {
  document.querySelectorAll(".page").forEach(p => p.classList.remove("active"));
  document.getElementById(id).classList.add("active");
  window.scrollTo({ top: 0, behavior: "smooth" });
}

function goHome() {
  openPage("home");
}

renderLaws();
</script>

</body>
</html>
