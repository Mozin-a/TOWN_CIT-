<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TOWN CITY - الشات والقوانين القضائية</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }
        body {
            background-color: #0d0e11;
            color: #fff;
            padding: 20px;
        }
        .container {
            display: flex;
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
            flex-wrap: wrap;
        }
        /* قسم القوانين (اليمين) */
        .sidebar-laws {
            flex: 1;
            min-width: 300px;
            background: #111214;
            border: 2px solid #b8860b;
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 4px 15px rgba(184, 134, 11, 0.3);
            height: fit-content;
        }
        /* قسم الشات العام (اليسار) */
        .main-chat {
            flex: 2;
            min-width: 350px;
            background: #16181d;
            border: 1px solid #2f3136;
            border-radius: 12px;
            padding: 15px;
            display: flex;
            flex-direction: column;
            height: 600px;
        }
        .chat-messages {
            flex: 1;
            overflow-y: auto;
            background: #111214;
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #202225;
        }
        .message {
            margin-bottom: 10px;
            padding: 8px 12px;
            background: #202225;
            border-radius: 6px;
            border-right: 3px solid #b8860b;
        }
        .message .author {
            font-weight: bold;
            color: #ffd700;
            font-size: 13px;
            margin-bottom: 4px;
        }
        .message .text {
            font-size: 14px;
            color: #dcddde;
        }
        .chat-input-area {
            display: flex;
            gap: 8px;
        }
        .chat-input-area input {
            flex: 1;
            padding: 10px;
            border-radius: 6px;
            border: 1px solid #2f3136;
            background: #202225;
            color: #fff;
            outline: none;
        }
        .chat-input-area button {
            padding: 10px 20px;
            background: #b8860b;
            color: #fff;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }
        .chat-input-area button:hover {
            background: #d4af37;
        }
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        
        <!-- ================= قسم قوانين الدولة (يمين الشات) ================= -->
        <div class="sidebar-laws">
            <!-- صورة قضائية فخمة -->
            <div style="text-align: center; margin-bottom: 10px;">
                <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?q=80&w=600&auto=format&fit=crop" alt="القضاء والعدالة" style="width: 100%; height: 120px; object-fit: cover; border-radius: 8px; border: 1px solid #b8860b;">
            </div>

            <!-- العنوان المزخرف -->
            <h3 style="text-align: center; color: #ffd700; font-size: 17px; margin-bottom: 15px; text-shadow: 0 2px 4px rgba(0,0,0,0.5);">
                ⚖️ ┋ آلتـشـريـعـات والقـوانـيـن القضـائـيـة ┋ ⚖️
            </h3>

            <!-- الباب الأول -->
            <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
                <summary style="font-weight: bold; color: #ffdf00; font-size: 13px;">📜 الباب الأول: الجرائم الجنائية الكبرى</summary>
                <p style="font-size: 12px; color: #ccc; margin-top: 8px; line-height: 1.6;">
                    <strong>المادة (1) - القتل العمد:</strong> يُعاقب المتسبب بإزهاق روح عمداً بالسجن المشدد وغرامة مالية وتحويل محوري للمحاكمة العسكرية.<br>
                    <strong>المادة (2) - الشروع في القتل والإيذاء:</strong> الاعتداء المسلح على المواطنين أو الأجهزة الأمنية يعرض مرتكبه لسحب الرخصة والأسلحة.<br>
                    <strong>المادة (3) - الاحتجاز القسري:</strong> يُحظر تقييد حرية أي مواطن دون سند قانوني أو قضائي رسمي.
                </p>
            </details>

            <!-- الباب الثاني -->
            <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
                <summary style="font-weight: bold; color: #ffdf00; font-size: 13px;">🚗 الباب الثاني: المرور ومخالفات الطرق</summary>
                <p style="font-size: 12px; color: #ccc; margin-top: 8px; line-height: 1.6;">
                    <strong>المادة (4) - القيادة المتهورة:</strong> تعريض حياة المارة والدوريات للخطر يوجب حجز المركبة الفوري.<br>
                    <strong>المادة (5) - الهروب من الدوريات:</strong> الهروب من التفتيش أو تجاهل أوامر التوقف يضاعف المخالفة ويستوجب التوقيف الفوري.<br>
                    <strong>المادة (6) - التخريب المتعمد:</strong> إتلاف الممتلكات العامة أو إشارات المرور يوجب غرامة تعويضية وتوقيفاً مدنياً.
                </p>
            </details>

            <!-- الباب الثالث -->
            <details style="background: #1a1b1e; padding: 10px; margin-bottom: 8px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
                <summary style="font-weight: bold; color: #ffdf00; font-size: 13px;">🛡️ الباب الثالث: الأمن والجهات الرسمية</summary>
                <p style="font-size: 12px; color: #ccc; margin-top: 8px; line-height: 1.6;">
                    <strong>المادة (7) - إهانة موظف عام:</strong> يُمنع الإساءة اللفظية أو الجسدية لرجال الأمن أو القضاء أثناء أداء مهامهم.<br>
                    <strong>المادة (8) - حيازة الأسلحة المحظورة:</strong> يُمنع حمل الأسلحة الحربية بالأماكن العامة الحيوية ويحق للشرطة التفتيش عند الاشتباه.<br>
                    <strong>المادة (9) - الهروب من المحكمة:</strong> عرقلة العدالة أو الهروب أثناء جلسات المحاكمة يعتبر جناية مستقلة.
                </p>
            </details>

            <!-- الباب الرابع -->
            <details style="background: #1a1b1e; padding: 10px; border-radius: 6px; border-right: 4px solid #b8860b; cursor: pointer;">
                <summary style="font-weight: bold; color: #ffdf00; font-size: 13px;">💼 الباب الرابع: التجارة والأعمال</summary>
                <p style="font-size: 12px; color: #ccc; margin-top: 8px; line-height: 1.6;">
                    <strong>المادة (10) - الأنشطة التجارية:</strong> يجب أن تكون جميع الصفقات والأنشطة ضمن النطاق القانوني المعتمد.<br>
                    <strong>المادة (11) - الرشوة واستغلال النفوذ:</strong> يُحظر تقديم أو قبول الرشاوى لتخفيف الأحكام أو التهرب من العقوبات.
                </p>
            </details>
        </div>

        <!-- ================= قسم الشات العام (يسار الشات) ================= -->
        <div class="main-chat">
            <h3 style="color: #ffd700; margin-bottom: 10px; font-size: 16px; border-bottom: 1px solid #2f3136; padding-bottom: 8px;">💬 ┋ آلسـحـآبـة أو آلشـآت آلعـآم ┋ 💬</h3>
            
            <!-- صندوق الرسائل -->
            <div class="chat-messages" id="chatBox">
                <div class="message">
                    <div class="author">النظام القضائي</div>
                    <div class="text">مرحباً بك في مدينة Town City. اكتب رسالتك بالأسفل لترسل مباشرة إلى ديسكورد!</div>
                </div>
            </div>

            <!-- خانة الإرسال -->
            <div class="chat-input-area">
                <input type="text" id="messageInput" placeholder="أكتب رسالتك هنا..." onkeypress="checkEnter(event)">
                <button onclick="sendMessage()">إرسال</button>
            </div>
        </div>

    </div>

    <script>
        // إعدادات الـ Webhook الخاص بك للربط مع ديسكورد
        const WEBHOOK_URL = "https://discord.com/api/webhooks/1347915573752623196/hC28f9qCq5K_...انسخ رابط الويب هوك الخاص بك هنا إذا غيرته..."; 

        function checkEnter(event) {
            if (event.key === 'Enter') {
                sendMessage();
            }
        }

        function sendMessage() {
            const input = document.getElementById('messageInput');
            const chatBox = document.getElementById('chatBox');
            const text = input.value.trim();

            if (text === '') return;

            // عرض الرسالة محلياً فوراً في الموقع
            const msgDiv = document.createElement('div');
            msgDiv.className = 'message';
            msgDiv.innerHTML = `<div class="author">زائر (من الموقع)</div><div class="text">${text}</div>`;
            chatBox.appendChild(msgDiv);
            chatBox.scrollTop = chatBox.scrollHeight;
            input.value = '';

            // إرسال الرسالة إلى ديسكورد عبر الـ Webhook
            // (استبدل الرابط أدناه برابط الـ Webhook الصحيح لديك إذا احتجت)
            fetch("https://discord.com/api/webhooks/1347915573752623196/hC28f9qCq5K_...ضع_رابطك_هنا...", {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    content: `💬 **رسالة جديدة من الموقع:**\n${text}`
                })
            }).catch(err => console.log("خطأ في إرسال الويب هوك"));
        }
    </script>
</body>
</html>
