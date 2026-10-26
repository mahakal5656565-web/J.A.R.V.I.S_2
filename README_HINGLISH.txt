KRISH JARVIS 0.1 — EXPANDED KOTLIN STARTER

THIS IS A NATIVE ANDROID / GRADLE PROJECT.
An HTML-to-APK Builder normally cannot compile Kotlin services. Open this project in Android Studio or a compatible Gradle Kotlin IDE such as a supported AIDE version.

FEATURES INCLUDED:
1. School monitoring activation/deactivation voice commands.
2. Notification Listener captures notification title/text exposed by apps while School Mode is active.
3. Local summary storage, Show Summary and Clear Summary buttons.
4. Daily 6:10 AM wake alarm with spoken "Sir, wake up." and a visible notification.
5. Voice snooze: say "snooze for 5 minutes" while Jarvis voice service is active and alarm is ringing.
6. Voice reminders such as "remind me to study in 10 minutes".
7. DeepSeek API key dialog and chat-completions request.
8. Supported app launch commands: "open YouTube", "open WhatsApp", "open Chrome", "open Gmail", "open Maps", "open Settings".
9. Web search: "search photosynthesis".
10. Text-to-Speech responses for supported actions and DeepSeek answers.

BUILD / SETUP:
1. Extract ZIP.
2. Open folder in Android Studio.
3. Sync Gradle; install Android SDK Platform 35 and JDK 17 if prompted.
4. Build and install on your Android phone.
5. Grant microphone and notification permissions.
6. Tap "Enable Notification Access"; enable Krish Jarvis in Android settings.
7. Save your own DeepSeek API key in the app.
8. Tap "Enable Alarms & Reminders" and grant special access.
9. Tap "Schedule Daily 6:10 AM Wake Alarm".
10. Tap "Start Background Voice" while app is visible.

VOICE COMMANDS:
- "Jarvis activate school monitoring"
- "Jarvis I am back"
- "snooze for 5 minutes"
- "open YouTube"
- "open WhatsApp"
- "open Chrome"
- "open Gmail"
- "open Maps"
- "open Settings"
- "search photosynthesis"
- "ask DeepSeek explain photosynthesis"
- "remind me to study in 10 minutes"
- "stop Jarvis listening"

IMPORTANT LIMITS:
- The microphone foreground service shows a persistent notification. Android may stop or interrupt speech recognition due to provider/network, noise, battery saver, OEM rules, or force-stop. This is not a guaranteed always-on hotword engine.
- This sample uses en-IN speech recognition. Offline recognition depends on the speech provider installed on the phone.
- The 6:10 alarm uses exact-alarm access where available. Grant "Alarms & reminders" access in Android settings; battery policies can still affect behavior.
- Alarm and reminder notifications are visible. The sample speaks a short message; voice playback depends on Android TTS being available.
- DeepSeek API key is stored in app-private SharedPreferences, not encrypted. Do not distribute the APK with your personal key; a production app should use stronger key handling or a backend.
- API model name availability can change; if DeepSeek rejects "deepseek-chat", update the model name to one enabled for your account.
- Notification Listener only gets content apps publish in notifications. It does not read all historical SMS/WhatsApp chats, hidden previews, or content not posted as a notification.
- App launching is limited to the supported package list and installed apps. Arbitrary touch control, unlocking, and unrestricted access to every app are not included.
- School Mode intentionally ignores ordinary commands and stays silent except the "I am back" deactivation command. It is not hidden monitoring.


GITHUB ACTIONS SE APK BANANE KA TARIKA (MOBILE)
================================================
1. Is ZIP ko extract karo.
2. GitHub ki private repository me ZIP upload karne ke bajay is folder ke ANDAR ki project files/folders upload karo, taaki `app/`, `build.gradle.kts`, `settings.gradle.kts` root par hon.
3. `.github/workflows/android.yml` file bhi upload honi chahiye. Phone ke GitHub web upload me hidden `.github` folder banana mushkil ho sakta hai; agar nahi ban pa raha, GitHub web par Add file > Create new file chuno aur filename me `.github/workflows/android.yml` likhkar workflow ka content paste karo.
4. Upload/commit ke baad repository ke Actions tab me jao. `Build Krish Jarvis APK` workflow select karo aur zarurat ho to `Run workflow` dabao.
5. Job successful ho to run page ke neeche Artifacts section me `Krish-Jarvis-debug-APK` download karo. ZIP artifact ko extract karke APK install karo.
6. Agar build red/fail ho, Actions log ka screenshot bhejo. APK tab tak nahi bana hoga.

SECURITY:
- Repository Private hi rakho.
- DeepSeek API key ko source code ya GitHub file me mat daalna. App ke andar API key save karna is starter build me encrypted nahi hai; personal key kisi ke saath share na karein.
- Ye workflow APK build karne ka prayas karta hai; build/test successful hone ki guarantee nahi. Device par alarm, mic service, notification access ko APK install ke baad test karo.
