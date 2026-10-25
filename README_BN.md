# Row Player — Android project starter

এটি একটি native Android Kotlin starter project। এতে আছে:
- ফোন থেকে একটি ভিডিও বেছে চালানো (Android document picker; আলাদা storage permission লাগে না)
- সরাসরি HTTP/HTTPS video URL চালানো
- AndroidX Media3 ExoPlayer-এর built-in playback controls

## Android ফোন থেকে কীভাবে build করবে
1. ZIP ফাইলটি extract করো।
2. Android Studio-তে project folder খুলে Gradle sync/build করো। Android Studio সাধারণত কম্পিউটারে ব্যবহার করা হয়।
3. Android ফোনেই করতে চাইলে Android-compatible IDE/build environment দরকার হবে; শুধু Chrome দিয়ে native APK build হয় না।
4. প্রথম build-এর সময় ইন্টারনেট লাগবে, কারণ Gradle dependencies ডাউনলোড হবে।
5. Build সফল হলে Android Studio থেকে APK তৈরি করে ফোনে install/test করো।

## সীমাবদ্ধতা
- এটি starter version; এখনো playlist/gallery scanning, subtitles UI, background playback service, history বা Play Store signing নেই।
- Online playback-এর জন্য direct media/stream URL দরকার। সাধারণ YouTube/Facebook webpage URL সাধারণত সরাসরি playable নয়।
- DRM-protected বা login-required streams সমর্থিত নয়।
- Media3 dependency version: 1.11.1. Official guide: https://developer.android.com/media/media3/exoplayer/hello-world
