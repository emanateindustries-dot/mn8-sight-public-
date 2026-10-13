# MN8 Sight - Android background spike

Goal: prove GPS logging and cue tones keep working with the screen off, before porting the full app.

## Run it (Windows)
1. Get this branch: `git checkout android-spike` (or download the branch ZIP from GitHub).
2. Open a terminal in the `android-app` folder and run:
   - `npm install`
   - `npx cap sync android`
   - `npx cap open android`  (opens Android Studio; first Gradle sync takes a few minutes, accept any SDK downloads)
3. On the Pixel 10: Settings > About phone > tap **Build number** 7 times, then Settings > System > Developer options > turn on **USB debugging**. Plug into the PC with USB and accept the prompt on the phone.
4. In Android Studio pick the Pixel in the device dropdown at the top and press the green Run button. The app installs and opens.
5. In the app: tap START TEST, allow location + notifications, press the power button, walk or ride 5+ minutes, turn the screen on, tap COPY RESULTS and paste them to Claude.

## What good looks like
- Roughly one GPS point per second the whole time (about 300 points in 5 minutes), no big gaps.
- Low tones (GPS callback) AND high tones (timer) every 15 s with the screen off.
