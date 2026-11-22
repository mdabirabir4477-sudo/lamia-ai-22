LAMIA AI (LAMU) — Android source project

এই ZIP-এ Android Studio-তে খোলার মতো সোর্স কোড দেওয়া হয়েছে। এটি APK নয়।

যা আছে:
- বাংলা/ইংরেজি speech recognition locale নির্বাচন
- দৃশ্যমান foreground microphone service
- স্থায়ী notification এবং Stop action
- “Lamu/লামু” শব্দ শুনলে সাড়া দেওয়ার সাধারণ logic
- কয়েকটি স্থানীয় শিক্ষামূলক উত্তর (support, resistance, wick)

গুরুত্বপূর্ণ সীমাবদ্ধতা:
1. এটি পূর্ণাঙ্গ AI নয়; কোনো ChatGPT/API backend যুক্ত নেই।
2. Android SpeechRecognizer সাধারণত ফোনের speech service/ইন্টারনেটের ওপর নির্ভর করতে পারে।
3. “Lamu” শনাক্ত করতে SpeechRecognizer-কে বারবার চালানো হচ্ছে। এটি প্রকৃত on-device wake-word engine নয়; ব্যাটারি বেশি খরচ করতে পারে এবং সব ফোনে নির্ভরযোগ্যভাবে কাজ নাও করতে পারে।
4. Android 12+ এবং বিশেষ করে Android 14+ এ microphone foreground service চালুর নিয়ম কঠোর। অ্যাপ দৃশ্যমান থাকা অবস্থায় Start চাপতে হবে; সিস্টেম বা নির্মাতার battery policy সার্ভিস বন্ধ করতে পারে।
5. ফোনের TTS engine-এ নারী কণ্ঠ থাকলে সেটি নির্বাচন করা যাবে; কোড নির্দিষ্ট নারী কণ্ঠ নিশ্চিত করতে পারে না।
6. এই প্রজেক্ট এখানে Android Studio দিয়ে build বা বাস্তব ফোনে test করা হয়নি।

Build করার সাধারণ ধাপ:
- কম্পিউটারে Android Studio ইনস্টল করো।
- এই ফোল্ডারটি Open করো।
- Gradle sync শেষ হলে Build > Build APK(s) নির্বাচন করো।
- APK তৈরি হলে নিজের ফোনে ইনস্টল করার আগে Android-এর অনুমতি ও নিরাপত্তা সতর্কতা দেখে নাও।

নিরাপত্তা:
- মাইক্রোফোন চালু থাকলে notification দৃশ্যমান থাকবে।
- ব্যবহার না করলে অ্যাপের Stop বোতাম বা notification-এর Stop ব্যবহার করো।
- এই অ্যাপ কোনো real-money trading signal দেয় না। ট্রেডিংয়ের অংশটি শুধু শেখার জন্য।
