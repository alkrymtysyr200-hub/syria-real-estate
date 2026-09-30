
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>المنصة السورية للعقارات</title>

<meta name="description" content="المنصة السورية للعقارات للبيع والشراء والتأجير في سوريا">

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Tahoma, Arial, sans-serif;
    background: #f4f6f8;
    color: #17202a;
}

header {
    background: linear-gradient(135deg, #075e54, #0b8f7f);
    color: white;
    text-align: center;
    padding: 25px 15px;
}

header h1 {
    margin: 0 0 10px;
    font-size: 28px;
}

header p {
    margin: 6px 0;
}

nav {
    background: white;
    padding: 12px;
    display: flex;
    justify-content: center;
    gap: 8px;
    flex-wrap: wrap;
    box-shadow: 0 2px 8px #0002;
    position: sticky;
    top: 0;
    z-index: 100;
}

nav button {
    border: none;
    background: #eef4f3;
    color: #075e54;
    padding: 11px 16px;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
    font-size: 15px;
}

nav button:hover {
    background: #075e54;
    color: white;
}

.container {
    max-width: 1150px;
    margin: auto;
    padding: 20px;
}

.page {
    display: none;
}

.page.active {
    display: block;
}

.box {
    background: white;
    border-radius: 15px;
    padding: 22px;
    margin-bottom: 20px;
    box-shadow: 0 3px 12px #0001;
}

h2 {
    color: #075e54;
    margin-top: 0;
}

h3 {
    color: #075e54;
}

.grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
}

input,
select,
textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccd3d8;
    border-radius: 8px;
    font-family: inherit;
    background: white;
}

textarea {
    min-height: 110px;
}

.full {
    grid-column: 1 / -1;
}

.btn {
    border: none;
    border-radius: 8px;
    padding: 12px 18px;
    cursor: pointer;
    font-weight: bold;
    margin-top: 10px;
}

.primary {
    background: #075e54;
    color: white;
}

.gold {
    background: #d99a18;
    color: white;
}

.red {
    background: #b83232;
    color: white;
}

.property-grid,
.plan-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
}

.card,
.plan {
    background: white;
    border-radius: 13px;
    padding: 18px;
    box-shadow: 0 3px 12px #0001;
}

.card {
    border-top: 4px solid #075e54;
}

.plan {
    text-align: center;
}

.plan-price {
    font-size: 24px;
    font-weight: bold;
    color: #075e54;
    margin: 15px 0;
}

.badge {
    display: inline-block;
    background: #075e54;
    color: white;
    padding: 5px 9px;
    border-radius: 20px;
    font-size: 12px;
}

.price {
    font-size: 20px;
    font-weight: bold;
    color: #075e54;
}

.payment {
    background: #fff8e5;
    border: 1px solid #e5c66b;
    padding: 18px;
    border-radius: 12px;
    margin-top: 20px;
}

.account {
    background: #075e54;
    color: white;
    padding: 15px;
    border-radius: 9px;
    word-break: break-all;
    font-size: 16px;
}

.notification {
    background: #e9f7f4;
    border-right: 5px solid #075e54;
    padding: 15px;
    border-radius: 8px;
    margin-bottom: 10px;
}

footer {
    background: #17202a;
    color: white;
    text-align: center;
    padding: 25px;
    margin-top: 30px;
}

.message {
    display: none;
    background: #e9f7f4;
    border-right: 5px solid #075e54;
    padding: 15px;
    border-radius: 8px;
    margin-top: 15px;
}

@media (max-width: 800px) {
    .grid,
    .property-grid,
    .plan-grid {
        grid-template-columns: 1fr;
    }

    .container {
        padding: 12px;
    }

    header h1 {
        font-size: 23px;
    }

    nav button {
        flex: 1 1 45%;
    }
}
</style>
</head>

<body>

<header>
    <h1>🏠 المنصة السورية للعقارات</h1>
    <p>بيع • شراء • تأجير العقارات في سوريا</p>
    <p>منصة سورية للأفراد والمكاتب والشركات</p>
</header>

<nav>
    <button type="button" onclick="openPage('home')">🏠 الرئيسية</button>
    <button type="button" onclick="openPage('publish')">➕ نشر إعلان</button>
    <button type="button" onclick="openPage('prices')">💰 الأسعار</button>
    <button type="button" onclick="openPage('offices')">🏢 المكاتب العقارية</button>
    <button type="button" onclick="openPage('notifications')">🔔 الإشعارات</button>
</nav>

<div class="container">

<!-- الرئيسية -->
<section id="home" class="page active">

    <div class="box">
        <h2>🔎 البحث عن عقار</h2>

        <div class="grid">

            <select id="searchGovernorate">
                <option value="">كل المحافظات</option>
                <option>دمشق</option>
                <option>ريف دمشق</option>
                <option>حلب</option>
                <option>حمص</option>
                <option>حماة</option>
                <option>اللاذقية</option>
                <option>طرطوس</option>
                <option>إدلب</option>
                <option>دير الزور</option>
                <option>الرقة</option>
                <option>الحسكة</option>
                <option>درعا</option>
                <option>السويداء</option>
                <option>القنيطرة</option>
            </select>

            <select id="searchType">
                <option value="">كل أنواع العقارات</option>
                <option>شقة</option>
                <option>منزل</option>
                <option>أرض</option>
                <option>محل تجاري</option>
                <option>مكتب</option>
                <option>مزرعة</option>
                <option>مستودع</option>
                <option>فيلا</option>
            </select>

            <select id="searchOperation">
                <option value="">بيع أو إيجار</option>
                <option>بيع</option>
                <option>إيجار</option>
            </select>

            <input id="searchText" placeholder="اكتب اسم المنطقة أو العقار">

        </div>

        <button class="btn primary" type="button" onclick="searchProperties()">
            🔍 بحث
        </button>
    </div>

    <div class="box">
        <h2>🏘️ أحدث العقارات</h2>
        <div id="propertyList" class="property-grid"></div>
    </div>

</section>


<!-- نشر إعلان -->
<section id="publish" class="page">

    <div class="box">

        <h2>➕ نشر إعلان عقاري</h2>

        <div class="grid">

            <div>
                <label>عنوان الإعلان</label>
                <input id="title" placeholder="مثال: شقة للبيع في دمشق">
            </div>

            <div>
                <label>نوع العقار</label>
                <select id="type">
                    <option>شقة</option>
                    <option>منزل</option>
                    <option>أرض</option>
                    <option>محل تجاري</option>
                    <option>مكتب</option>
                    <option>مزرعة</option>
                    <option>مستودع</option>
                    <option>فيلا</option>
                </select>
            </div>

            <div>
                <label>العملية</label>
                <select id="operation">
                    <option>بيع</option>
                    <option>إيجار</option>
                </select>
            </div>

            <div>
                <label>المحافظة</label>
                <select id="governorate">
                    <option value="">اختر المحافظة</option>
                    <option>دمشق</option>
                    <option>ريف دمشق</option>
                    <option>حلب</option>
                    <option>حمص</option>
                    <option>حماة</option>
                    <option>اللاذقية</option>
                    <option>طرطوس</option>
                    <option>إدلب</option>
                    <option>دير الزور</option>
                    <option>الرقة</option>
                    <option>الحسكة</option>
                    <option>درعا</option>
                    <option>السويداء</option>
                    <option>القنيطرة</option>
                </select>
            </div>

            <div>
                <label>المنطقة</label>
                <input id="area" placeholder="مثال: المزة">
            </div>

            <div>
                <label>السعر</label>
                <input id="price" placeholder="مثال: 150000000">
            </div>

            <div class="full">
                <label>وصف العقار</label>
                <textarea id="description" placeholder="اكتب تفاصيل العقار والمساحة والموقع"></textarea>
            </div>

            <div>
                <label>اسم المعلن</label>
                <input id="seller" placeholder="اسم المعلن">
            </div>

            <div>
                <label>رقم الهاتف أو واتساب</label>
                <input id="phone" placeholder="رقم التواصل">
            </div>

        </div>

        <h3>💰 اختر نوع الإعلان</h3>

        <div class="plan-grid">

            <div class="plan">
                <h3>🆓 عادي</h3>
                <div class="plan-price">مجاني</div>
                <p>نشر الإعلان بشكل عادي</p>
                <button class="btn primary" type="button" onclick="choosePlan('مجاني',0)">
                    اختيار
                </button>
            </div>

            <div class="plan">
                <h3>⭐ مميز</h3>
                <div class="plan-price">50,000 ل.س</div>
                <p>ظهور أفضل لمدة 7 أيام</p>
                <button class="btn gold" type="button" onclick="choosePlan('مميز 7 أيام',50000)">
                    اختيار
                </button>
            </div>

            <div class="plan">
                <h3>📌 مثبت</h3>
                <div class="plan-price">80,000 ل.س</div>
                <p>ظهور أعلى النتائج لمدة 7 أيام</p>
                <button class="btn red" type="button" onclick="choosePlan('مثبت 7 أيام',80000)">
                    اختيار
                </button>
            </div>

        </div>

        <div id="payment" class="payment" style="display:none;">

            <h3>💳 معلومات الدفع</h3>

            <p>
                الباقة المختارة:
                <strong id="chosenPlan"></strong>
            </p>

            <p>
                المبلغ:
                <strong id="chosenPrice"></strong>
                ل.س
            </p>

            <div id="paidInfo">

                <p>حوّل المبلغ عبر شام كاش إلى الحساب التالي:</p>

                <div class="account">
                    9a4550c00144ad5fccb0cafb4377f0ee
                </div>

                <p>بعد التحويل أدخل رقم العملية:</p>

                <input id="transaction" placeholder="رقم عملية التحويل">

            </div>

            <button class="btn primary" type="button" onclick="submitProperty()">
                ✅ إرسال الإعلان للمراجعة
            </button>

            <div id="publishMessage" class="message"></div>

        </div>

    </div>

</section>


<!-- الأسعار -->
<section id="prices" class="page">

    <div class="box">

        <h2>💰 أسعار الإعلانات</h2>

        <div class="plan-grid">

            <div class="plan">
                <h3>🆓 الإعلان العادي</h3>
                <div class="plan-price">مجاني</div>
                <p>نشر العقار بدون رسوم</p>
            </div>

            <div class="plan">
                <h3>⭐ مميز 7 أيام</h3>
                <div class="plan-price">50,000 ل.س</div>
                <p>ظهور أفضل في نتائج البحث</p>
            </div>

            <div class="plan">
                <h3>⭐ مميز 30 يومًا</h3>
                <div class="plan-price">120,000 ل.س</div>
                <p>ترويج لمدة شهر</p>
            </div>

            <div class="plan">
                <h3>📌 مثبت 7 أيام</h3>
                <div class="plan-price">80,000 ل.س</div>
                <p>ظهور أعلى النتائج</p>
            </div>

            <div class="plan">
                <h3>📌 مثبت 30 يومًا</h3>
                <div class="plan-price">200,000 ل.س</div>
                <p>تثبيت لمدة شهر</p>
            </div>

            <div class="plan">
                <h3>🏢 مكتب عقاري</h3>
                <div class="plan-price">500,000 ل.س</div>
                <p>باقة شهرية للمكاتب العقارية</p>
            </div>

            <div class="plan">
                <h3>🏗️ شركة / مشروع</h3>
                <div class="plan-price">750,000 ل.س</div>
                <p>إعلان تجاري لمدة شهر</p>
            </div>

        </div>

    </div>

</section>


<!-- المكاتب -->
<section id="offices" class="page">

    <div class="box">

        <h2>🏢 المكاتب والشركات العقارية</h2>

        <p>
            يمكن للمكاتب والشركات العقارية استخدام المنصة
            لعرض عقاراتهم والإعلانات التجارية.
        </p>

        <h3>الباقة الشهرية للمكتب</h3>

        <div class="plan-price">
            500,000 ل.س
        </div>

        <button class="btn primary" type="button" onclick="openPage('publish')">
            ➕ نشر إعلان
        </button>

    </div>

</section>


<!-- الإشعارات -->
<section id="notifications" class="page">

    <div class="box">

        <h2>🔔 الإشعارات</h2>

        <div class="notification">
            مرحبًا بك في المنصة السورية للعقارات.
        </div>

        <div class="notification">
            يمكنك نشر إعلان مجاني أو اختيار إعلان مدفوع.
        </div>

    </div>

</section>

</div>


<footer>
    <strong>المنصة السورية للعقارات</strong>
    <p>بيع • شراء • تأجير • مكاتب عقارية • إعلانات مدفوعة</p>
    <p>© 2026 جميع الحقوق محفوظة</p>
</footer>


<script>

let properties = [

    {
        title: "شقة للبيع في دمشق",
        type: "شقة",
        operation: "بيع",
        governorate: "دمشق",
        area: "المزة",
        price: "250,000,000",
        description: "شقة سكنية مناسبة للعائلة.",
        seller: "معلن",
        phone: ""
    },

    {
        title: "أرض للبيع في الرقة",
        type: "أرض",
        operation: "بيع",
        governorate: "الرقة",
        area: "الرقة المدينة",
        price: "100,000,000",
        description: "أرض مناسبة للاستثمار.",
        seller: "معلن",
        phone: ""
    },

    {
        title: "محل تجاري للإيجار في حلب",
        type: "محل تجاري",
        operation: "إيجار",
        governorate: "حلب",
        area: "وسط المدينة",
        price: "1,500,000 شهريًا",
        description: "محل تجاري في موقع جيد.",
        seller: "معلن",
        phone: ""
    }

];

let selectedPlan = "مجاني";
let selectedPrice = 0;


/* فتح الصفحات */

function openPage(pageId) {

    const pages = document.querySelectorAll(".page");

    pages.forEach(function(page) {
        page.classList.remove("active");
    });

    const page = document.getElementById(pageId);

    if (page) {
        page.classList.add("active");
    }

    window.scrollTo(0, 0);
}


/* اختيار الباقة */

function choosePlan(plan, price) {

    selectedPlan = plan;
    selectedPrice = price;

    document.getElementById("payment").style.display = "block";

    document.getElementById("chosenPlan").textContent = plan;

    document.getElementById("chosenPrice").textContent =
        price.toLocaleString("ar-SY");

    const paidInfo = document.getElementById("paidInfo");

    if (price === 0) {

        paidInfo.style.display = "none";

    } else {

        paidInfo.style.display = "block";

    }

    document.getElementById("payment").scrollIntoView({
        behavior: "smooth"
    });
}


/* إرسال الإعلان */

function submitProperty() {

    const title = document.getElementById("title").value.trim();
    const governorate = document.getElementById("governorate").value;
    const area = document.getElementById("area").value.trim();
    const price = document.getElementById("price").value.trim();
    const seller = document.getElementById("seller").value.trim();
    const phone = document.getElementById("phone").value.trim();

    if (title === "") {
        showMessage("يرجى كتابة عنوان الإعلان.");
        return;
    }

    if (governorate === "") {
        showMessage("يرجى اختيار المحافظة.");
        return;
    }

    if (area === "") {
        showMessage("يرجى كتابة المنطقة.");
        return;
    }

    if (price === "") {
        showMessage("يرجى كتابة السعر.");
        return;
    }

    if (seller === "") {
        showMessage("يرجى كتابة اسم المعلن.");
        return;
    }

    if (phone === "") {
        showMessage("يرجى كتابة رقم التواصل.");
        return;
    }

    if (selectedPrice > 0) {

        const transaction =
            document.getElementById("transaction").value.trim();

        if (transaction === "") {
            showMessage("يرجى إدخال رقم عملية شام كاش.");
            return;
        }
    }

    const property = {

        title: title,

        type: document.getElementById("type").value,

        operation: document.getElementById("operation").value,

        governorate: governorate,

        area: area,

        price: price,

        description:
            document.getElementById("description").value.trim(),

        seller: seller,

        phone: phone

    };

    properties.unshift(property);

    renderProperties();

    showMessage(
        "تم تسجيل الإعلان بنجاح على هذا الجهاز. سيتم وضعه للمراجعة."
    );

    setTimeout(function() {
        openPage("home");
    }, 1500);
}


/* رسالة */

function showMessage(message) {

    const box = document.getElementById("publishMessage");

    box.textContent = message;

    box.style.display = "block";
}


/* عرض العقارات */

function renderProperties(list) {

    const container =
        document.getElementById("propertyList");

    container.innerHTML = "";

    const data = list || properties;

    if (data.length === 0) {

        container.innerHTML =
            "<p>لا توجد عقارات مطابقة للبحث.</p>";

        return;
    }

    data.forEach(function(property) {

        const card = document.createElement("div");

        card.className = "card";

        card.innerHTML = `

            <span class="badge">
                ${property.operation}
            </span>

            <h3>${property.title}</h3>

            <p>
                📍 ${property.governorate}
                - ${property.area}
            </p>

            <p>
                🏠 ${property.type}
            </p>

            <div class="price">
                ${property.price} ل.س
            </div>

            <p>
                ${property.description || ""}
            </p>

            <p>
                👤 ${property.seller}
            </p>

            ${
                property.phone
                ?
                `<p>📞 ${property.phone}</p>`
                :
                ""
            }

        `;

        container.appendChild(card);

    });
}


/* البحث */

function searchProperties() {

    const governorate =
        document.getElementById("searchGovernorate").value;

    const type =
        document.getElementById("searchType").value;

    const operation =
        document.getElementById("searchOperation").value;

    const text =
        document.getElementById("searchText").value
        .trim()
        .toLowerCase();

    const results = properties.filter(function(property) {

        const matchGovernorate =
            governorate === "" ||
            property.governorate === governorate;

        const matchType =
            type === "" ||
            property.type === type;

        const matchOperation =
            operation === "" ||
            property.operation === operation;

        const fullText =
            (
                property.title +
                " " +
                property.area +
                " " +
                property.governorate
            ).toLowerCase();

        const matchText =
            text === "" ||
            fullText.includes(text);

        return (
            matchGovernorate &&
            matchType &&
            matchOperation &&
            matchText
        );

    });

    renderProperties(results);
}


/* تشغيل المنصة */

renderProperties();

</script>

</body>
</html>
