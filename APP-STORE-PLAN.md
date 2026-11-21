# Nne Says! — App Store plan

Goal: pass Apple review on the first submission and avoid a **Guideline 4.2 (Minimum Functionality)** rejection. Apple rejects apps that feel like a website in a wrapper, so the app needs to do things a website can't.

## How we build it

- **Capacitor** wraps the same game code as a real iOS and Android app.
- Everything is **bundled inside the app**: the game, Mama's art and all the audio. Nothing loads from a website, and the whole app works in airplane mode.
- Build on Chioma's **MacBook Pro M1** with Xcode (free). Test on her **iPhone 15 Pro Max**.

## Native features that make it "a real app" (the 4.2 checklist)

| # | Feature | Why Apple cares | How |
|---|---|---|---|
| 1 | Native tab bar: Lessons · Play · Phrasebook · Me | App-style navigation, not web pages | Built into the app shell |
| 2 | Works fully offline (audio included) | A website can't do this | Audio bundled in the app |
| 3 | Daily reminder from Mama ("Your Igbo is getting cold!") | Uses the device's notifications | `@capacitor/local-notifications` |
| 4 | Phone buzzes when the slipper hits | Uses device haptics | `@capacitor/haptics` |
| 5 | Share your score through the iPhone share sheet | Native sharing | `@capacitor/share` |
| 6 | **Say it like Mama**: record yourself and compare with Mama | Uses the microphone, a real learning feature | Native audio recorder plugin |
| 7 | Progress, streaks and unlocked units saved on the device | App-owned data | `@capacitor/preferences` |
| 8 | Igbo "word of the day" home-screen widget (version 1.1) | Strong native signal | iOS WidgetKit extension |
| 9 | Onboarding: pick your goal (heritage / travel / fun) | App-specific flow | Built into the app |
| 10 | App-styled offline, loading and error screens | No browser error pages | Built into the app |
| 11 | Splash screen and app icon from the logo | Polished, native feel | `@capacitor/splash-screen` |

## Money features (and the rules for each)

- **Rewarded ads ("slipper lives"):** Google AdMob rewarded ads via `@capacitor-community/admob`. On iOS, show Apple's App Tracking Transparency prompt before personalized ads. Rating 13+, so no child-directed ad restrictions.
- **Premium subscription:** must use **Apple In-App Purchase** on iOS and **Google Play Billing** on Android for digital content (Apple guideline 3.1.1). Use **RevenueCat** (free until you earn real revenue) to manage both. Suggested pricing: $4.99/month, $39.99/year, 7-day free trial. Premium = unlimited slippers, no ads, units 7–10 and future units, dialect packs.
- **Merch:** physical products can use outside checkout (Shopify + Printful or Printify print-on-demand). Link to the store from the "Me" tab.
- **Sponsors:** "Today's lesson is brought to you by…" cards between units. Keep them age-appropriate for 13+.

## Submission checklist

- [ ] Apple Developer Program ($99/year) under the business LLC, not a personal name
- [ ] Google Play Console ($25 once) + 12 testers opted in for 14 days (new personal accounts)
- [ ] Privacy policy and support page on nnesays.com
- [ ] App Privacy "nutrition label" filled in accurately (ads data, purchases)
- [ ] Age rating questionnaire → 13+
- [ ] Real screenshots of the app in use (lessons, Mama, phrasebook)
- [ ] Notes for the reviewer: what each tab does, how to test premium (sandbox), no login needed
- [ ] Every screen has a way back; external links open in an in-app browser
- [ ] Native-speaker review of all Igbo text and audio done
