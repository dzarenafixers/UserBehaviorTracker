# 🕵️‍♂️ User Behavior Tracker - برنامج تحليل سلوك المستخدم

## 📌 Overview - نظرة عامة
**User Behavior Tracker** is a desktop application that monitors user activity.  
**برنامج تحليل سلوك المستخدم** هو تطبيق يقوم بمراقبة نشاط المستخدم على سطح المكتب.

### 🔍 Features - الميزات
- **🔵 Tracks running applications** and their CPU usage.  
  **يتتبع التطبيقات المفتوحة** واستهلاكها للمعالج.
- **⌨️ Records keyboard keystrokes** (keylogger functionality).  
  **يسجل ضغطات لوحة المفاتيح**.
- **🖱️ Monitors mouse clicks** and their locations.  
  **يراقب نقرات الفأرة** ويحدد مواقعها.

---

## 📂 Project Structure - بنية المشروع

UserBehaviorTracker/ │── src/ │ ├── tracker/ │ │ ├── Main.java # Entry point | نقطة التشغيل الرئيسية │ ├── tracking/ │ │ ├── AppTracker.java # App tracking | تتبع التطبيقات │ │ ├── KeyLogger.java # Key logging | تسجيل ضغطات المفاتيح │ │ ├── MouseTracker.java # Mouse tracking | تتبع الفأرة │ ├── data/ │ │ ├── DatabaseManager.java # Database manager | إدارة قاعدة البيانات │── libs/ # Third-party libraries | مكتبات الطرف الثالث │── README.md # Documentation file | ملف التوثيق │── pom.xml (If using Maven | إذا كنت تستخدم Maven) │── user_behavior.db # Local database | قاعدة البيانات المخزنة محليًا

---

## ⚙️ **Requirements - المتطلبات**
📌 **Make sure Java 17+ is installed.**  
📌 **تأكد من تثبيت Java 17+ على جهازك.**  

📌 **Required libraries:**
📌 **المكتبات المطلوبة:**
1. **JNativeHook** for keyboard/mouse tracking.  
   **لتتبع لوحة المفاتيح والفأرة**.
2. **OSHI** for system data.  
   **للحصول على بيانات النظام**.
3. **SQLite JDBC** for database storage.  
   **لتخزين البيانات في قاعدة بيانات SQLite**.

### ✅ **Maven Users - إذا كنت تستخدم Maven**
Add the following dependencies to **`pom.xml`**:  
أضف الأسطر التالية إلى **`pom.xml`**:
```xml
<dependencies>
    <dependency>
        <groupId>com.github.kwhat</groupId>
        <artifactId>jnativehook</artifactId>
        <version>2.2.2</version>
    </dependency>
    <dependency>
        <groupId>com.github.oshi</groupId>
        <artifactId>oshi-core</artifactId>
        <version>6.2.2</version>
    </dependency>
    <dependency>
        <groupId>org.xerial</groupId>
        <artifactId>sqlite-jdbc</artifactId>
        <version>3.39.3.0</version>
    </dependency>
</dependencies>
