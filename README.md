<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سیستم ایده‌پردازی کانون کریم اهل‌بیت</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --idea-color: #9b59b6;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), #1a2530);
            color: white;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            font-family: "Font Awesome 6 Free";
            font-weight: 900;
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 40px;
            opacity: 0.1;
        }
        
        header h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }
        
        header p {
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .admin-access {
            position: absolute;
            left: 20px;
            top: 20px;
        }
        
        .admin-btn {
            background: rgba(255,255,255,0.2);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
            }
        }
        
        .form-section, .ideas-section {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .section-title {
            color: var(--primary-color);
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            color: var(--accent-color);
        }
        
        .idea-title {
            color: var(--idea-color);
            border-bottom: 2px solid var(--idea-color);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary-color);
        }
        
        .required::after {
            content: " *";
            color: var(--accent-color);
        }
        
        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            transition: border 0.3s;
        }
        
        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.2);
        }
        
        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
            background: #f8f9fa;
            padding: 10px 15px;
            border-radius: 5px;
            border: 1px solid #eee;
            flex: 1;
            min-width: 180px;
        }
        
        .checkbox-item input {
            width: auto;
        }
        
        .checkbox-item.active {
            background-color: rgba(52, 152, 219, 0.1);
            border-color: var(--secondary-color);
        }
        
        .checkbox-item.disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }
        
        .counter {
            font-size: 12px;
            color: #777;
            margin-top: 5px;
        }
        
        .counter.error {
            color: var(--accent-color);
        }
        
        .form-actions {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }
        
        .btn {
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .btn-primary {
            background-color: var(--secondary-color);
            color: white;
            flex: 2;
        }
        
        .btn-secondary {
            background-color: var(--light-color);
            color: var(--primary-color);
            flex: 1;
        }
        
        .btn-idea {
            background-color: var(--idea-color);
            color: white;
        }
        
        .btn-admin {
            background-color: var(--warning-color);
            color: white;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
        }
        
        .idea-box {
            border: 2px dashed #e0e0e0;
            border-radius: 10px;
            padding: 25px;
            margin: 20px 0;
            transition: all 0.3s;
            background-color: #fcfcfc;
        }
        
        .idea-box:hover {
            border-color: var(--idea-color);
            background-color: rgba(155, 89, 182, 0.05);
        }
        
        .idea-box h3 {
            color: var(--idea-color);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .idea-content {
            padding: 15px;
            background-color: white;
            border-radius: 8px;
            margin: 15px 0;
            border-right: 4px solid var(--idea-color);
        }
        
        .idea-list {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-top: 20px;
        }
        
        .idea-item {
            padding: 20px;
            border-radius: 8px;
            background-color: #f8f9fa;
            border: 1px solid #e9ecef;
            transition: all 0.3s;
        }
        
        .idea-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }
        
        .idea-item.new {
            border-right: 4px solid var(--success-color);
            background-color: rgba(39, 174, 96, 0.05);
        }
        
        .idea-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .idea-title {
            font-size: 18px;
            color: var(--primary-color);
            margin: 0;
            border: none;
        }
        
        .idea-meta {
            font-size: 14px;
            color: #777;
            margin-top: 10px;
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .idea-tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-top: 10px;
        }
        
        .tag {
            background-color: rgba(52, 152, 219, 0.1);
            color: var(--secondary-color);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .tag-role {
            background-color: rgba(155, 89, 182, 0.1);
            color: var(--idea-color);
        }
        
        .tag-space {
            background-color: rgba(231, 76, 60, 0.1);
            color: var(--accent-color);
        }
        
        .idea-content {
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }
        
        .highlight {
            background-color: rgba(52, 152, 219, 0.1);
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
            border-right: 4px solid var(--secondary-color);
        }
        
        .highlight-idea {
            background-color: rgba(155, 89, 182, 0.1);
            border-right: 4px solid var(--idea-color);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #777;
            border-top: 1px solid #eee;
            margin-top: 30px;
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .modal-title {
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .close-modal {
            float: left;
            font-size: 24px;
            cursor: pointer;
            color: #777;
        }
        
        .help-text {
            font-size: 13px;
            color: #777;
            margin-top: 5px;
        }
        
        .error-message {
            color: var(--accent-color);
            font-size: 14px;
            margin-top: 5px;
            display: none;
        }
        
        .word-count {
            font-size: 12px;
            text-align: left;
            margin-top: 5px;
            color: #777;
        }
        
        .word-count.error {
            color: var(--accent-color);
        }
        
        .admin-panel {
            background-color: #fff8e1;
            border: 2px solid var(--warning-color);
            border-radius: 10px;
            padding: 20px;
            margin-top: 30px;
            display: none;
        }
        
        .admin-controls {
            display: flex;
            gap: 10px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .submissions-list {
            margin-top: 20px;
            max-height: 400px;
            overflow-y: auto;
        }
        
        .submission-item {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            border-left: 4px solid var(--secondary-color);
        }
        
        .inspiration {
            font-style: italic;
            color: #666;
            padding: 10px 15px;
            background-color: #f9f9f9;
            border-radius: 5px;
            margin: 10px 0;
            border-right: 3px solid var(--idea-color);
        }
        
        .empty-state {
            text-align: center;
            padding: 40px 20px;
            color: #777;
        }
        
        .empty-state i {
            font-size: 48px;
            color: #ddd;
            margin-bottom: 15px;
        }
        
        .space-count-info {
            background-color: rgba(52, 152, 219, 0.05);
            padding: 10px 15px;
            border-radius: 5px;
            margin-top: 10px;
            border-right: 3px solid var(--secondary-color);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="admin-access">
                <button class="admin-btn" id="adminLoginBtn"><i class="fas fa-lock"></i> ورود مدیران</button>
            </div>
            <h1><i class="fas fa-lightbulb"></i> سیستم ایده‌پردازی کانون کریم اهل‌بیت</h1>
            <p>فرم جمع‌آوری ایده‌های خلاقانه برای بهینه‌سازی و استفاده از فضای طبقه بالای مسجد</p>
        </header>
        
        <div class="main-content">
            <section class="form-section">
                <h2 class="section-title"><i class="fas fa-edit"></i> ایده‌پردازی شما</h2>
                
                <div class="idea-box">
                    <h3><i class="fas fa-question-circle"></i> چه ایده‌ای برای طبقه بالای مسجد دارید؟</h3>
                    <p class="inspiration">ما به ایده‌های خلاقانه شما نیاز داریم! فکر کنید اگر قرار باشد فضای طبقه بالای مسجد را طراحی کنید، چه چیزی می‌سازید؟</p>
                </div>
                
                <form id="ideaForm">
                    <div class="form-group">
                        <label for="memberName" class="required"><i class="fas fa-user"></i> نام و نام خانوادگی</label>
                        <input type="text" id="memberName" placeholder="نام کامل خود را وارد کنید" required>
                    </div>
                    
                    <div class="form-group">
                        <label class="required"><i class="fas fa-user-tag"></i> نقش‌های شما در کانون (حداقل ۱ و حداکثر ۳ مورد)</label>
                        <div class="checkbox-group" id="rolesContainer">
                            <!-- نقش‌ها با JavaScript اضافه می‌شوند -->
                        </div>
                        <div class="counter" id="roleCounter">۰ مورد انتخاب شده (حداقل ۱ و حداکثر ۳)</div>
                    </div>
                    
                    <div class="form-group">
                        <label class="required"><i class="fas fa-cube"></i> نوع فضا/اتاقی که پیشنهاد می‌دهید</label>
                        <div class="checkbox-group" id="spaceTypesContainer">
                            <!-- انواع فضاها با JavaScript اضافه می‌شوند -->
                        </div>
                        <div class="space-count-info">
                            <i class="fas fa-info-circle"></i> شما می‌توانید حداکثر <strong>۴ مورد</strong> از ۸ گزینه زیر را انتخاب کنید
                        </div>
                        <div class="counter" id="spaceCounter">۰ مورد انتخاب شده (حداقل ۱ و حداکثر ۴ مورد)</div>
                    </div>
                    
                    <div class="highlight highlight-idea">
                        <h3><i class="fas fa-tools"></i> با این فضا دقیقاً چه کار کنیم؟</h3>
                        <p>لطفاً به طور دقیق و جزء به جزء توضیح دهید که با این فضای پیشنهادی چه اقداماتی باید انجام شود:</p>
                    </div>
                    
                    <div class="form-group">
                        <label for="spaceActions" class="required"><i class="fas fa-list-check"></i> اقدامات اجرایی مورد نیاز</label>
                        <textarea id="spaceActions" rows="4" placeholder="مثال: دیوارها رنگ‌آمیزی شود، کف‌پوش مناسب نصب شود، پنجره‌ها عایق‌بندی شوند، نورپردازی مناسب انجام شود، میز و صندلی مناسب خریداری شود و..." required minlength="80"></textarea>
                        <div class="word-count" id="actionsCounter">۰ کاراکتر (حداقل ۸۰ کاراکتر - توصیه می‌شود جزئیات کامل بنویسید)</div>
                        <div class="help-text">لطفاً به ترتیب اولویت و با جزئیات اقدامات لازم را لیست کنید</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="spaceUsage" class="required"><i class="fas fa-calendar-alt"></i> نحوه استفاده و برنامه زمان‌بندی</label>
                        <textarea id="spaceUsage" rows="4" placeholder="مثال: صبح‌ها کلاس قرآن، بعدازظهر جلسات کانون، شب‌ها کارگاه‌های مهارتی، جمعه‌ها جلسات مشاوره، آخر هفته دورهمی اعضا و..." required minlength="60"></textarea>
                        <div class="word-count" id="usageCounter">۰ کاراکتر (حداقل ۶۰ کاراکتر)</div>
                        <div class="help-text">چگونه و در چه روزها و ساعاتی از این فضا استفاده شود؟</div>
                    </div>
                    
                    <div class="highlight">
                        <h3><i class="fas fa-bullseye"></i> اهداف و انتظارات از این فضا</h3>
                    </div>
                    
                    <div class="form-group">
                        <label for="spaceGoals" class="required"><i class="fas fa-flag"></i> اهداف اصلی این فضا چیست؟</label>
                        <textarea id="spaceGoals" rows="3" placeholder="مثال: ایجاد محیطی برای مطالعه و تحقیق، تقویت ارتباطات بین اعضا، آموزش مهارت‌های زندگی، مکانی برای مشاوره و راهنمایی، محل برگزاری کارگاه‌های تخصصی و..." required minlength="50"></textarea>
                        <div class="word-count" id="goalsCounter">۰ کاراکتر (حداقل ۵۰ کاراکتر)</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="targetAudience" class="required"><i class="fas fa-users"></i> مخاطبان این فضا چه کسانی هستند؟</label>
                        <textarea id="targetAudience" rows="2" placeholder="مثال: اعضای اصلی کانون، نوجوانان محله، خانواده‌ها، بانوان، عموم مردم و..." required minlength="30"></textarea>
                        <div class="word-count" id="audienceCounter">۰ کاراکتر (حداقل ۳۰ کاراکتر)</div>
                    </div>
                    
                    <div class="highlight highlight-idea">
                        <h3><i class="fas fa-lightbulb"></i> الزامات و امکانات مورد نیاز</h3>
                    </div>
                    
                    <div class="form-group">
                        <label for="equipmentNeeds" class="required"><i class="fas fa-laptop"></i> تجهیزات و وسایل مورد نیاز</label>
                        <textarea id="equipmentNeeds" rows="3" placeholder="مثال: ویدئو پروژکتور، سیستم صوتی، میز کنفرانس ۱۲ نفره، صندلی‌های راحت، قفسه کتاب، یخچال، مایکروفر، تخته وایت‌برد، کامپیوتر و..." required minlength="60"></textarea>
                        <div class="word-count" id="equipmentCounter">۰ کاراکتر (حداقل ۶۰ کاراکتر)</div>
                        <div class="help-text">لیست کاملی از تمام تجهیزات مورد نیاز با تعداد تقریبی</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="budgetEstimate"><i class="fas fa-calculator"></i> تخمین هزینه‌های راه‌اندازی (اختیاری)</label>
                        <textarea id="budgetEstimate" rows="2" placeholder="مثال: هزینه رنگ‌آمیزی: ۵ میلیون تومان، خرید میز و صندلی: ۱۵ میلیون تومان، تجهیزات صوتی: ۱۰ میلیون تومان و..."></textarea>
                        <div class="help-text">در صورت امکان، تخمینی از هزینه‌های مورد نیاز ارائه دهید</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="otherSuggestions" class="required"><i class="fas fa-comments"></i> سایر پیشنهادات، نکات و ملاحظات</label>
                        <textarea id="otherSuggestions" rows="3" placeholder="هر پیشنهاد دیگر، نکته ایمنی، محدودیت‌ها، فرصت‌ها و تهدیدها (حداقل ۸۰ کلمه)" required minlength="120"></textarea>
                        <div class="word-count" id="otherCounter">۰ کاراکتر (حداقل ۱۲۰ کاراکتر)</div>
                        <div class="help-text">نظرات شما با دقت بررسی خواهد شد و در تصمیم‌گیری‌ها استفاده می‌شود</div>
                    </div>
                    
                    <div class="form-actions">
                        <button type="submit" class="btn btn-idea"><i class="fas fa-paper-plane"></i> ارسال ایده</button>
                        <button type="button" id="resetBtn" class="btn btn-secondary"><i class="fas fa-redo"></i> پاک کردن فرم</button>
                    </div>
                </form>
            </section>
            
            <section class="ideas-section">
                <h2 class="section-title"><i class="fas fa-lightbulb"></i> ایده‌های مطرح‌شده</h2>
                
                <div id="ideasList">
                    <div class="empty-state" id="emptyIdeasState">
                        <i class="fas fa-lightbulb"></i>
                        <h3>هنوز ایده‌ای ثبت نشده است!</h3>
                        <p>اولین نفری باشید که ایده خود را مطرح می‌کند.</p>
                        <p>فرم سمت چپ را پر کنید و ایده خلاقانه خود را با ما به اشتراک بگذارید.</p>
                    </div>
                </div>
                
                <div class="highlight" style="margin-top: 30px;">
                    <h4><i class="fas fa-lightbulb"></i> راهنمای ارسال ایده</h4>
                    <ul style="padding-right: 20px; margin-top: 10px;">
                        <li><strong>خلاقانه فکر کنید:</strong> هر ایده‌ای، حتی اگر ساده باشد ارزشمند است</li>
                        <li><strong>جزئیات مهم است:</strong> هرچه دقیق‌تر توضیح دهید، امکان اجرا بیشتر می‌شود</li>
                        <li><strong>واقع‌بین باشید:</strong> ایده‌های قابل اجرا با امکانات موجود اولویت دارند</li>
                        <li><strong>مخاطب‌محور باشید:</strong> نیازهای واقعی اعضا و جامعه را در نظر بگیرید</li>
                        <li><strong>توجه:</strong> می‌توانید حداکثر ۴ نوع فضا را انتخاب کنید</li>
                    </ul>
                </div>
            </section>
        </div>
        
        <!-- پنل مدیریت -->
        <div class="admin-panel" id="adminPanel">
            <h2 class="section-title"><i class="fas fa-user-shield"></i> پنل مدیریت ایده‌ها</h2>
            <div class="form-group">
                <label for="adminPassword"><i class="fas fa-key"></i> رمز ورود مدیران</label>
                <input type="password" id="adminPassword" placeholder="فقط مدیران کانون مجاز به ورود هستند">
            </div>
            <div class="admin-controls">
                <button class="btn btn-admin" id="loginAdminBtn"><i class="fas fa-sign-in-alt"></i> ورود به پنل</button>
            </div>
            
            <div id="adminContent" style="display: none;">
                <div class="admin-controls">
                    <button class="btn btn-admin" id="viewIdeasBtn"><i class="fas fa-list"></i> مشاهده همه ایده‌ها</button>
                    <button class="btn btn-admin" id="exportIdeasBtn"><i class="fas fa-download"></i> خروجی Excel</button>
                    <button class="btn btn-admin" id="statsBtn"><i class="fas fa-chart-bar"></i> آمار و گزارش</button>
                    <button class="btn btn-secondary" id="changePasswordBtn"><i class="fas fa-key"></i> تغییر رمز</button>
                    <button class="btn btn-secondary" id="logoutAdminBtn"><i class="fas fa-sign-out-alt"></i> خروج از پنل</button>
                </div>
                <div class="submissions-list" id="submissionsList">
                    <!-- لیست ایده‌ها اینجا نمایش داده می‌شود -->
                </div>
            </div>
        </div>
        
        <footer>
            <p>کانون کریم اهل‌بیت | سیستم ایده‌پردازی فضای مسجد | نسخه نهایی</p>
            <p><i class="fas fa-envelope"></i> برای دسترسی مدیران با مسئول کانون تماس بگیرید</p>
            <p>تمام ایده‌ها محرمانه تلقی شده و صرفاً برای بهبود کانون استفاده می‌شوند</p>
        </footer>
    </div>
    
    <!-- مودال تغییر رمز -->
    <div class="modal" id="passwordModal">
        <div class="modal-content">
            <span class="close-modal" id="closePasswordModal">&times;</span>
            <h3 class="modal-title"><i class="fas fa-key"></i> تغییر رمز مدیریت</h3>
            <div class="form-group">
                <label>رمز فعلی</label>
                <input type="password" id="currentPassword">
            </div>
            <div class="form-group">
                <label>رمز جدید</label>
                <input type="password" id="newPassword">
            </div>
            <div class="form-group">
                <label>تکرار رمز جدید</label>
                <input type="password" id="confirmPassword">
            </div>
            <button class="btn btn-primary" id="savePasswordBtn">ذخیره رمز جدید</button>
        </div>
    </div>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // داده‌های اولیه
            const roles = [
                {id: 'media', name: 'رسانه', icon: 'fa-broadcast-tower'},
                {id: 'communications', name: 'ارتباطات', icon: 'fa-comments'},
                {id: 'ceremonies', name: 'مراسمات', icon: 'fa-calendar-alt'},
                {id: 'finance', name: 'امور مالی', icon: 'fa-wallet'},
                {id: 'logistics', name: 'تدارکات', icon: 'fa-truck'},
                {id: 'cultural', name: 'فرهنگی', icon: 'fa-book-open'},
                {id: 'sports', name: 'ورزشی', icon: 'fa-futbol'}
            ];
            
            const spaceTypes = [
                {id: 'educational', name: 'فضای آموزشی', icon: 'fa-chalkboard-teacher'},
                {id: 'cultural', name: 'فضای فرهنگی', icon: 'fa-book'},
                {id: 'meeting', name: 'فضای جلسات', icon: 'fa-users'},
                {id: 'counseling', name: 'فضای مشاوره', icon: 'fa-hands-helping'},
                {id: 'recreational', name: 'فضای تفریحی', icon: 'fa-gamepad'},
                {id: 'multipurpose', name: 'فضای چندمنظوره', icon: 'fa-th-large'},
                {id: 'workshop', name: 'کارگاه عملی', icon: 'fa-tools'},
                {id: 'media', name: 'استودیو رسانه', icon: 'fa-podcast'}
            ];
            
            // رمز مدیریتی (فقط مدیر اصلی می‌داند)
            let adminPassword = localStorage.getItem('karimAdminPassword') || "KarimSecret@1403";
            
            // متغیرهای DOM
            const form = document.getElementById('ideaForm');
            const rolesContainer = document.getElementById('rolesContainer');
            const spaceTypesContainer = document.getElementById('spaceTypesContainer');
            const roleCounter = document.getElementById('roleCounter');
            const spaceCounter = document.getElementById('spaceCounter');
            const adminPanel = document.getElementById('adminPanel');
            const adminContent = document.getElementById('adminContent');
            const ideasList = document.getElementById('ideasList');
            const emptyIdeasState = document.getElementById('emptyIdeasState');
            
            // متغیرهای انتخابی
            let selectedRoles = [];
            let selectedSpaces = [];
            const MAX_SPACES = 4; // نصف ۸ گزینه = ۴
            
            // تولید نقش‌ها
            roles.forEach(role => {
                const div = document.createElement('div');
                div.className = 'checkbox-item';
                div.innerHTML = `
                    <input type="checkbox" id="role_${role.id}" value="${role.name}">
                    <label for="role_${role.id}"><i class="fas ${role.icon}"></i> ${role.name}</label>
                `;
                rolesContainer.appendChild(div);
                
                const checkbox = div.querySelector('input');
                checkbox.addEventListener('change', function() {
                    if (this.checked) {
                        if (selectedRoles.length >= 3) {
                            this.checked = false;
                            alert('حداکثر می‌توانید ۳ نقش انتخاب کنید');
                            return;
                        }
                        selectedRoles.push(role.name);
                        div.classList.add('active');
                    } else {
                        selectedRoles = selectedRoles.filter(r => r !== role.name);
                        div.classList.remove('active');
                    }
                    updateRoleCounter();
                });
            });
            
            // تولید انواع فضاها
            spaceTypes.forEach(space => {
                const div = document.createElement('div');
                div.className = 'checkbox-item';
                div.innerHTML = `
                    <input type="checkbox" id="space_${space.id}" value="${space.name}">
                    <label for="space_${space.id}"><i class="fas ${space.icon}"></i> ${space.name}</label>
                `;
                spaceTypesContainer.appendChild(div);
                
                const checkbox = div.querySelector('input');
                checkbox.addEventListener('change', function() {
                    if (this.checked) {
                        if (selectedSpaces.length >= MAX_SPACES) {
                            this.checked = false;
                            alert(`حداکثر می‌توانید ${MAX_SPACES} نوع فضا انتخاب کنید`);
                            return;
                        }
                        selectedSpaces.push(space.name);
                        div.classList.add('active');
                    } else {
                        selectedSpaces = selectedSpaces.filter(s => s !== space.name);
                        div.classList.remove('active');
                    }
                    updateSpaceCounter();
                });
            });
            
            // به‌روزرسانی شمارنده نقش‌ها
            function updateRoleCounter() {
                roleCounter.textContent = `${selectedRoles.length} مورد انتخاب شده (حداقل ۱ و حداکثر ۳)`;
                if (selectedRoles.length === 0 || selectedRoles.length > 3) {
                    roleCounter.classList.add('error');
                } else {
                    roleCounter.classList.remove('error');
                }
            }
            
            // به‌روزرسانی شمارنده فضاها
            function updateSpaceCounter() {
                spaceCounter.textContent = `${selectedSpaces.length} مورد انتخاب شده (حداقل ۱ و حداکثر ${MAX_SPACES} مورد)`;
                if (selectedSpaces.length === 0 || selectedSpaces.length > MAX_SPACES) {
                    spaceCounter.classList.add('error');
                } else {
                    spaceCounter.classList.remove('error');
                }
            }
            
            // شمارنده کاراکترها
            function setupCounter(textareaId, counterId, minLength, recommendation = '') {
                const textarea = document.getElementById(textareaId);
                const counter = document.getElementById(counterId);
                
                textarea.addEventListener('input', function() {
                    const length = this.value.length;
                    const words = this.value.trim().split(/\s+/).length;
                    counter.textContent = `${words} کلمه، ${length} کاراکتر (حداقل ${minLength} کاراکتر) ${recommendation}`;
                    
                    if (length < minLength) {
                        counter.classList.add('error');
                    } else {
                        counter.classList.remove('error');
                    }
                });
            }
            
            // راه‌اندازی شمارنده‌ها
            setupCounter('spaceActions', 'actionsCounter', 80, '- توصیه: جزئیات کامل');
            setupCounter('spaceUsage', 'usageCounter', 60);
            setupCounter('spaceGoals', 'goalsCounter', 50);
            setupCounter('targetAudience', 'audienceCounter', 30);
            setupCounter('equipmentNeeds', 'equipmentCounter', 60);
            setupCounter('otherSuggestions', 'otherCounter', 120);
            
            // بررسی حداقل کاراکتر
            function validateMinLength(textareaId, minLength) {
                const textarea = document.getElementById(textareaId);
                return textarea.value.length >= minLength;
            }
            
            // ارسال فرم
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // اعتبارسنجی
                if (selectedRoles.length === 0 || selectedRoles.length > 3) {
                    alert('لطفاً بین ۱ تا ۳ نقش انتخاب کنید');
                    return;
                }
                
                if (selectedSpaces.length === 0 || selectedSpaces.length > MAX_SPACES) {
                    alert(`لطفاً بین ۱ تا ${MAX_SPACES} نوع فضا انتخاب کنید`);
                    return;
                }
                
                const validations = [
                    {id: 'spaceActions', min: 80, message: 'لطفاً اقدامات اجرایی را با حداقل ۸۰ کاراکتر توضیح دهید'},
                    {id: 'spaceUsage', min: 60, message: 'لطفاً نحوه استفاده را با حداقل ۶۰ کاراکتر توضیح دهید'},
                    {id: 'spaceGoals', min: 50, message: 'لطفاً اهداف فضا را با حداقل ۵۰ کاراکتر توضیح دهید'},
                    {id: 'targetAudience', min: 30, message: 'لطفاً مخاطبان را با حداقل ۳۰ کاراکتر توضیح دهید'},
                    {id: 'equipmentNeeds', min: 60, message: 'لطفاً تجهیزات مورد نیاز را با حداقل ۶۰ کاراکتر توضیح دهید'},
                    {id: 'otherSuggestions', min: 120, message: 'لطفاً سایر پیشنهادات را با حداقل ۱۲۰ کاراکتر توضیح دهید'}
                ];
                
                for (let validation of validations) {
                    if (!validateMinLength(validation.id, validation.min)) {
                        alert(validation.message);
                        document.getElementById(validation.id).focus();
                        return;
                    }
                }
                
                // جمع‌آوری داده‌ها
                const ideaData = {
                    id: Date.now(),
                    name: document.getElementById('memberName').value,
                    roles: selectedRoles,
                    spaces: selectedSpaces,
                    actions: document.getElementById('spaceActions').value,
                    usage: document.getElementById('spaceUsage').value,
                    goals: document.getElementById('spaceGoals').value,
                    audience: document.getElementById('targetAudience').value,
                    equipment: document.getElementById('equipmentNeeds').value,
                    budget: document.getElementById('budgetEstimate').value || 'تخمین زده نشده',
                    suggestions: document.getElementById('otherSuggestions').value,
                    timestamp: new Date().toLocaleString('fa-IR'),
                    status: 'جدید',
                    date: new Date().toISOString().split('T')[0]
                };
                
                // ذخیره در localStorage
                saveIdea(ideaData);
                
                // نمایش در لیست ایده‌ها
                addToIdeasList(ideaData);
                
                // نمایش پیام موفقیت
                alert(`ایده خلاقانه شما با موفقیت ثبت شد!\n\nاز تفکر و ایده‌پردازی شما متشکریم.\nایده شما با کد ${ideaData.id} ثبت شد و در اسرع وقت بررسی خواهد گردید.`);
                
                // بازنشانی فرم
                form.reset();
                selectedRoles = [];
                selectedSpaces = [];
                document.querySelectorAll('.checkbox-item').forEach(item => {
                    item.classList.remove('active');
                    item.querySelector('input').checked = false;
                });
                updateRoleCounter();
                updateSpaceCounter();
            });
            
            // ذخیره ایده در localStorage
            function saveIdea(data) {
                let ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                ideas.push(data);
                localStorage.setItem('karimIdeas', JSON.stringify(ideas));
            }
            
            // بارگذاری ایده‌های ذخیره شده
            function loadSavedIdeas() {
                const ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                
                if (ideas.length === 0) {
                    emptyIdeasState.style.display = 'block';
                    return;
                }
                
                emptyIdeasState.style.display = 'none';
                
                // مرتب سازی بر اساس تاریخ (جدیدترین اول)
                ideas.sort((a, b) => new Date(b.date) - new Date(a.date));
                
                ideas.forEach(idea => {
                    addToIdeasList(idea, false);
                });
            }
            
            // افزودن به لیست نمایش ایده‌ها
            function addToIdeasList(data, prepend = true) {
                emptyIdeasState.style.display = 'none';
                
                const div = document.createElement('div');
                div.className = 'idea-item new';
                div.dataset.id = data.id;
                div.innerHTML = `
                    <div class="idea-header">
                        <h4 class="idea-title">${data.spaces.join('، ')}</h4>
                        <span class="tag">${data.status}</span>
                    </div>
                    <div class="idea-meta">
                        <span><i class="fas fa-user"></i> ${data.name}</span>
                        <span><i class="fas fa-calendar"></i> ${data.timestamp}</span>
                    </div>
                    <div class="idea-tags">
                        ${data.roles.map(role => `<span class="tag tag-role">${role}</span>`).join('')}
                        ${data.spaces.map(space => `<span class="tag tag-space">${space}</span>`).join('')}
                    </div>
                    <div class="idea-content">
                        <p><strong>اهداف:</strong> ${data.goals.substring(0, 80)}...</p>
                        <p><strong>مخاطبان:</strong> ${data.audience.substring(0, 60)}...</p>
                    </div>
                `;
                
                // کلیک برای نمایش جزئیات
                div.addEventListener('click', function() {
                    showIdeaDetails(data);
                });
                
                if (prepend) {
                    ideasList.prepend(div);
                } else {
                    ideasList.appendChild(div);
                }
            }
            
            // نمایش جزئیات ایده
            function showIdeaDetails(data) {
                const details = `
                    <div class="idea-item" style="background-color: #e8f4fc; cursor: default;">
                        <div class="idea-header">
                            <h4 class="idea-title">${data.spaces.join('، ')}</h4>
                            <span class="tag">${data.status}</span>
                        </div>
                        <div class="idea-meta">
                            <span><i class="fas fa-user"></i> ${data.name}</span>
                            <span><i class="fas fa-calendar"></i> ${data.timestamp}</span>
                            <span><i class="fas fa-hashtag"></i> کد: ${data.id}</span>
                        </div>
                        <div class="idea-tags">
                            ${data.roles.map(role => `<span class="tag tag-role">${role}</span>`).join('')}
                            ${data.spaces.map(space => `<span class="tag tag-space">${space}</span>`).join('')}
                        </div>
                        <div class="idea-content">
                            <p><strong>اقدامات اجرایی:</strong><br>${data.actions}</p>
                            <p><strong>نحوه استفاده:</strong><br>${data.usage}</p>
                            <p><strong>اهداف اصلی:</strong><br>${data.goals}</p>
                            <p><strong>مخاطبان هدف:</strong><br>${data.audience}</p>
                            <p><strong>تجهیزات مورد نیاز:</strong><br>${data.equipment}</p>
                            <p><strong>تخمین بودجه:</strong><br>${data.budget}</p>
                            <p><strong>سایر پیشنهادات:</strong><br>${data.suggestions}</p>
                        </div>
                        <button class="btn btn-secondary" onclick="window.location.reload()" style="margin-top: 15px;">
                            <i class="fas fa-arrow-right"></i> بازگشت به لیست ایده‌ها
                        </button>
                    </div>
                `;
                
                // جایگزین کردن لیست با جزئیات
                ideasList.innerHTML = details;
            }
            
            // مدیریت پنل ادمین
            document.getElementById('adminLoginBtn').addEventListener('click', function() {
                adminPanel.style.display = 'block';
            });
            
            // ورود به پنل مدیریت
            document.getElementById('loginAdminBtn').addEventListener('click', function() {
                const passwordInput = document.getElementById('adminPassword').value;
                
                if (passwordInput === adminPassword) {
                    adminContent.style.display = 'block';
                    document.getElementById('adminPassword').value = '';
                    alert('با موفقیت وارد پنل مدیریت شدید.');
                } else {
                    alert('رمز ورود اشتباه است. فقط مدیران کانون مجاز به ورود هستند.');
                }
            });
            
            // مشاهده ایده‌ها در پنل مدیریت
            document.getElementById('viewIdeasBtn').addEventListener('click', function() {
                const ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                
                if (ideas.length === 0) {
                    submissionsList.innerHTML = '<p>هنوز هیچ ایده‌ای ثبت نشده است.</p>';
                    return;
                }
                
                // مرتب سازی بر اساس تاریخ
                ideas.sort((a, b) => new Date(b.date) - new Date(a.date));
                
                let html = `<h3>تمامی ایده‌های ثبت‌شده (${ideas.length} مورد)</h3>`;
                
                ideas.forEach((idea, index) => {
                    html += `
                        <div class="submission-item">
                            <h4>ایده ${index + 1}: ${idea.spaces.join('، ')}</h4>
                            <p><strong>نام:</strong> ${idea.name}</p>
                            <p><strong>نقش‌ها:</strong> ${idea.roles.join('، ')}</p>
                            <p><strong>فضاها:</strong> ${idea.spaces.join('، ')}</p>
                            <p><strong>تاریخ ثبت:</strong> ${idea.timestamp}</p>
                            <p><strong>وضعیت:</strong> <span class="tag">${idea.status}</span></p>
                            <p><strong>اهداف:</strong> ${idea.goals.substring(0, 80)}...</p>
                            <div style="display: flex; gap: 10px; margin-top: 10px;">
                                <button class="btn btn-secondary" onclick="viewFullIdea(${idea.id})" style="padding: 5px 10px; font-size: 14px;">
                                    <i class="fas fa-eye"></i> مشاهده کامل
                                </button>
                                <button class="btn btn-secondary" onclick="changeStatus(${idea.id})" style="padding: 5px 10px; font-size: 14px;">
                                    <i class="fas fa-edit"></i> تغییر وضعیت
                                </button>
                            </div>
                        </div>
                    `;
                });
                
                submissionsList.innerHTML = html;
            });
            
            // خروجی Excel
            document.getElementById('exportIdeasBtn').addEventListener('click', function() {
                const ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                
                if (ideas.length === 0) {
                    alert('داده‌ای برای خروجی وجود ندارد');
                    return;
                }
                
                // ایجاد CSV
                let csv = 'کد,نام,نقش‌ها,فضاها,اقدامات اجرایی,نحوه استفاده,اهداف,مخاطبان,تجهیزات,بودجه,سایر پیشنهادات,تاریخ ثبت,وضعیت\n';
                
                ideas.forEach(idea => {
                    csv += `"${idea.id}","${idea.name}","${idea.roles.join(', ')}","${idea.spaces.join(', ')}","${idea.actions.replace(/"/g, '""')}","${idea.usage.replace(/"/g, '""')}","${idea.goals.replace(/"/g, '""')}","${idea.audience.replace(/"/g, '""')}","${idea.equipment.replace(/"/g, '""')}","${idea.budget}","${idea.suggestions.replace(/"/g, '""')}","${idea.timestamp}","${idea.status}"\n`;
                });
                
                // ایجاد فایل و دانلود
                const blob = new Blob(['\uFEFF' + csv], {type: 'text/csv;charset=utf-8;'});
                const link = document.createElement('a');
                link.href = URL.createObjectURL(blob);
                link.download = `ایده_های_کانون_کریم_${new Date().toLocaleDateString('fa-IR')}.csv`;
                link.click();
                
                alert(`فایل Excel با ${ideas.length} ایده دانلود شد`);
            });
            
            // آمار و گزارش
            document.getElementById('statsBtn').addEventListener('click', function() {
                const ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                
                if (ideas.length === 0) {
                    alert('داده‌ای برای تحلیل وجود ندارد');
                    return;
                }
                
                // تحلیل داده‌ها
                const spaceTypeCount = {};
                const roleCount = {};
                const statusCount = {};
                
                ideas.forEach(idea => {
                    // شمارش انواع فضا
                    idea.spaces.forEach(space => {
                        spaceTypeCount[space] = (spaceTypeCount[space] || 0) + 1;
                    });
                    
                    // شمارش نقش‌ها
                    idea.roles.forEach(role => {
                        roleCount[role] = (roleCount[role] || 0) + 1;
                    });
                    
                    // شمارش وضعیت‌ها
                    statusCount[idea.status] = (statusCount[idea.status] || 0) + 1;
                });
                
                // تولید گزارش
                let html = `<h3>گزارش آماری ایده‌ها</h3>`;
                html += `<p><strong>تعداد کل ایده‌ها:</strong> ${ideas.length}</p>`;
                html += `<p><strong>میانگین تعداد فضاهای انتخابی:</strong> ${(ideas.reduce((sum, idea) => sum + idea.spaces.length, 0) / ideas.length).toFixed(1)}</p>`;
                
                html += `<h4>توزیع بر اساس نوع فضا (${Object.keys(spaceTypeCount).length} نوع مختلف):</h4>`;
                // مرتب سازی بر اساس تعداد
                const sortedSpaces = Object.entries(spaceTypeCount).sort((a, b) => b[1] - a[1]);
                for (const [type, count] of sortedSpaces) {
                    const percentage = ((count / ideas.reduce((sum, idea) => sum + idea.spaces.length, 0)) * 100).toFixed(1);
                    html += `<p>${type}: ${count} انتخاب (${percentage}%)</p>`;
                }
                
                html += `<h4>توزیع بر اساس نقش (${Object.keys(roleCount).length} نقش مختلف):</h4>`;
                // مرتب سازی بر اساس تعداد
                const sortedRoles = Object.entries(roleCount).sort((a, b) => b[1] - a[1]);
                for (const [role, count] of sortedRoles) {
                    html += `<p>${role}: ${count} انتخاب</p>`;
                }
                
                html += `<h4>وضعیت ایده‌ها:</h4>`;
                for (const [status, count] of Object.entries(statusCount)) {
                    const percentage = ((count / ideas.length) * 100).toFixed(1);
                    html += `<p>${status}: ${count} مورد (${percentage}%)</p>`;
                }
                
                // میانگین طول ایده‌ها
                const avgLength = ideas.reduce((sum, idea) => 
                    sum + idea.actions.length + idea.usage.length + idea.suggestions.length, 0) / ideas.length;
                html += `<p><strong>میانگین حجم ایده‌ها:</strong> ${Math.round(avgLength)} کاراکتر</p>`;
                
                submissionsList.innerHTML = html;
            });
            
            // تغییر رمز
            document.getElementById('changePasswordBtn').addEventListener('click', function() {
                passwordModal.style.display = 'flex';
            });
            
            // بستن مودال
            document.getElementById('closePasswordModal').addEventListener('click', function() {
                passwordModal.style.display = 'none';
            });
            
            // ذخیره رمز جدید
            document.getElementById('savePasswordBtn').addEventListener('click', function() {
                const current = document.getElementById('currentPassword').value;
                const newPass = document.getElementById('newPassword').value;
                const confirm = document.getElementById('confirmPassword').value;
                
                if (current !== adminPassword) {
                    alert('رمز فعلی اشتباه است');
                    return;
                }
                
                if (newPass !== confirm) {
                    alert('رمز جدید و تکرار آن مطابقت ندارند');
                    return;
                }
                
                if (newPass.length < 8) {
                    alert('رمز جدید باید حداقل ۸ کاراکتر باشد');
                    return;
                }
                
                adminPassword = newPass;
                localStorage.setItem('karimAdminPassword', newPass);
                alert('رمز با موفقیت تغییر یافت');
                passwordModal.style.display = 'none';
                document.getElementById('currentPassword').value = '';
                document.getElementById('newPassword').value = '';
                document.getElementById('confirmPassword').value = '';
            });
            
            // خروج از پنل مدیریت
            document.getElementById('logoutAdminBtn').addEventListener('click', function() {
                adminContent.style.display = 'none';
                adminPanel.style.display = 'none';
                document.getElementById('adminPassword').value = '';
            });
            
            // بازنشانی فرم
            document.getElementById('resetBtn').addEventListener('click', function() {
                if (confirm('آیا مطمئنید می‌خواهید فرم را پاک کنید؟')) {
                    form.reset();
                    selectedRoles = [];
                    selectedSpaces = [];
                    document.querySelectorAll('.checkbox-item').forEach(item => {
                        item.classList.remove('active');
                        item.querySelector('input').checked = false;
                    });
                    updateRoleCounter();
                    updateSpaceCounter();
                    alert('فرم با موفقیت پاک شد');
                }
            });
            
            // تابع مشاهده کامل ایده (برای استفاده در دکمه‌ها)
            window.viewFullIdea = function(id) {
                const ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                const idea = ideas.find(i => i.id == id);
                
                if (idea) {
                    const details = `
                        <div class="submission-item" style="background-color: #e8f4fc;">
                            <h4>جزئیات کامل ایده (کد: ${idea.id})</h4>
                            <p><strong>نام:</strong> ${idea.name}</p>
                            <p><strong>نقش‌ها:</strong> ${idea.roles.join('، ')}</p>
                            <p><strong>فضاها:</strong> ${idea.spaces.join('، ')}</p>
                            <p><strong>وضعیت:</strong> <span class="tag">${idea.status}</span></p>
                            <p><strong>تاریخ ثبت:</strong> ${idea.timestamp}</p>
                            <hr>
                            <p><strong>اقدامات اجرایی:</strong><br>${idea.actions}</p>
                            <p><strong>نحوه استفاده:</strong><br>${idea.usage}</p>
                            <p><strong>اهداف اصلی:</strong><br>${idea.goals}</p>
                            <p><strong>مخاطبان هدف:</strong><br>${idea.audience}</p>
                            <p><strong>تجهیزات مورد نیاز:</strong><br>${idea.equipment}</p>
                            <p><strong>تخمین بودجه:</strong><br>${idea.budget}</p>
                            <p><strong>سایر پیشنهادات:</strong><br>${idea.suggestions}</p>
                            <div style="display: flex; gap: 10px; margin-top: 15px;">
                                <button class="btn btn-secondary" onclick="changeStatus(${idea.id})" style="padding: 5px 10px; font-size: 14px;">
                                    <i class="fas fa-edit"></i> تغییر وضعیت
                                </button>
                                <button class="btn btn-secondary" onclick="window.location.reload()" style="padding: 5px 10px; font-size: 14px;">
                                    <i class="fas fa-arrow-right"></i> بازگشت
                                </button>
                            </div>
                        </div>
                    `;
                    
                    submissionsList.innerHTML = details;
                }
            };
            
            // تابع تغییر وضعیت ایده
            window.changeStatus = function(id) {
                const newStatus = prompt('وضعیت جدید را وارد کنید (جدید، در حال بررسی، تأیید شده، اجرا شده):', 'در حال بررسی');
                
                if (newStatus && ['جدید', 'در حال بررسی', 'تأیید شده', 'اجرا شده'].includes(newStatus)) {
                    let ideas = JSON.parse(localStorage.getItem('karimIdeas') || '[]');
                    const index = ideas.findIndex(i => i.id == id);
                    
                    if (index !== -1) {
                        ideas[index].status = newStatus;
                        localStorage.setItem('karimIdeas', JSON.stringify(ideas));
                        
                        // به‌روزرسانی نمایش در لیست ایده‌ها
                        const ideaElement = document.querySelector(`.idea-item[data-id="${id}"]`);
                        if (ideaElement) {
                            ideaElement.querySelector('.tag').textContent = newStatus;
                        }
                        
                        alert(`وضعیت ایده ${id} به "${newStatus}" تغییر یافت`);
                    }
                }
            };
            
            // بارگذاری ایده‌های ذخیره شده هنگام لود صفحه
            loadSavedIdeas();
        });
    </script>
</body>
</html>
