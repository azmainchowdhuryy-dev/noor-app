# Android সেটআপ (লোকেশন ও ইন্টারনেট পারমিশন)

যদি লোকাল পিসিতে প্রথমবার রান করেন এবং `android/` ফোল্ডার না থাকে, তবে প্রজেক্ট রুটে চালান:

    flutter create --platforms=android --project-name noor_app --org com.azmain.noor .

এরপর `android/app/src/main/AndroidManifest.xml` ফাইলে `<manifest>` ট্যাগের ভেতরে,
`<application>` ট্যাগের আগে নিচের পারমিশনগুলো যোগ করুন:

    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>

তারপর: `flutter pub get`  →  `flutter run`
