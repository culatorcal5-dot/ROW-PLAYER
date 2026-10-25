# Android ফোন থেকে Row Player APK তৈরি করার সহজ পদ্ধতি

## যা লাগবে
- GitHub account
- এই ZIP ফাইল
- ইন্টারনেট সংযোগ

## ধাপ ১: GitHub repository বানাও
1. Chrome-এ https://github.com/new খোলো এবং sign in করো।
2. Repository name দাও `row-player`।
3. Public বা Private বেছে `Create repository` চাপো।

## ধাপ ২: ZIP-এর ফাইলগুলো upload করো
1. নতুন repository-তে `Add file` → `Upload files` চাপো।
2. ZIP ফাইলটি আগে ফোনে extract করো।
3. Extract করা folder-এর **ভেতরের সব ফাইল/ফোল্ডার** upload করো. `.github` hidden folder-ও upload করতে হবে. GitHub mobile web-এ hidden folder upload করা কঠিন হলে GitHub app/desktop mode/another file picker use করো.
4. Commit changes চাপো. Files root-ல் `settings.gradle.kts`, `build.gradle.kts`, `app/` மற்றும் `.github/workflows/build-apk.yml` இருக்க வேண்டும்.

## ধাপ ৩: Cloud build চালাও
1. Repository-তে `Actions` tab খোলো।
2. `Build Row Player APK` workflow নির্বাচন করো।
3. `Run workflow` চাপো, branch `main` নির্বাচন করে সবুজ `Run workflow` চাপো।
4. Build শেষ হওয়া পর্যন্ত অপেক্ষা করো। প্রথম build-এ কয়েক মিনিট লাগতে পারে।

## ধাপ ৪: APK ডাউনলোড করো
1. সফল workflow run খুলে নিচের `Artifacts` অংশে যাও।
2. `Row-Player-debug-APK` ডাউনলোড করো।
3. ZIP artifact extract করে `app-debug.apk` বের করো।
4. APK খোলো এবং Android-এর prompt এলে install অনুমতি দিয়ে install করো।

## সমস্যা হলে
- Build error হলে Actions run খুলে error-এর শেষ অংশের screenshot পাঠাও।
- `.github/workflows/build-apk.yml` ফাইলটি ঠিক এই path-এ থাকতে হবে।
- এটি **debug APK**, Play Store release-signed APK নয়।
- Online video চালাতে direct media URL দরকার; YouTube/Facebook page link সরাসরি চলবে না।
