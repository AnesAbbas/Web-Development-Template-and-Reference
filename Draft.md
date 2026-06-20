

steps to follow:

- immerse yourself in designs online and ones saved for inspiration
- take screenshots on browser of interesting sites. F12, `c.s.p`, `screenshot full page`
- generate DESIGN.mds from screenshots
- exrtact parts interesting to you from the md into your own DESIGN.md 
- doodle desktop and mobile layouts
- decide breakpoints
- 
- 
- stickerize app with svg graphics and animations
- add animations last

flow

- create design.md
- create html a stylesheet for variables `variables.css` and one for the actual styles `styles.css` from the md
- print it as a reference
- 
- 
- 

use Lucide Icons
use tailwind


## Micro-interactions

short animations that play when the user interacts with the interface

overview: https://www.youtube.com/watch?v=jgrkV_hJdJw&loop=0

Agent Skill 1: https://github.com/solinkz/micro-interactions-skill  
Agent Skill 2: https://github.com/rastian/interaction-design-skills

----

design systems do not just deal with visualization but psycology

color
typography
iconography
illustrations
radius
spacing (letter and line)
shadows
components
layout
animations
breakpoints

----


create a design system generator

font   4 levels
colors 4 levels
radius 4 levels
...

heavy on 
icons 
micro animations
immersive scrolling
flat ui and colors
lottie files
3d assets
video assets
Card-based UI


glassmorphism
neomorphism
skeuomorphism
claymorphism
flat ui

https://lucide.dev/
https://lucide.dev/guide/

https://fontawesome.com/
https://docs.fontawesome.com/
https://docs.fontawesome.com/web/use-with/fa-cli



tailwind


>>> 

AI tool use in bedrock and structured output
Also to provider add image generation etc.
Also to provider add audio generation etc.

---

Things to go for

- Minimal and responsive flat UI design
- Rounded corner elements
- Flat colors
- Flat icons and illustrations
- SVG format graphics (whenever possible)
- Sans-serif modern font combinations
- Bold headers
- Light use of blob shapes and borders
- Light use of glassmorphic elements
- Light use of neumorphic elements
- Light use of flat illustration animations (if any)
- Micro-interaction subtle animations (clicking/pressing, scrolling into view, transitioning, etc.) (Library)
- Color variables
- Light and dark modes

Avoid

- 3d elements
- Serif fonts
- Sharp borders
- Drop shadows (with exception to glassmorphic and neumorphic use cases)



>>>>>>>>>>>>>>>>>>>>>>>>>


>> idea: daily reports on service like to recommendations

----
gray/white backdrop
flat ui
bento ui
card style
some glass morphism
iconography
bold font everywhere except for paragraphs

https://lottiefiles.com/
https://www.lottielab.com/
ad: https://www.youtube.com/watch?v=A_sjNPSA4kg&loop=0
https://www.youtube.com/@LottieFiles/playlists

---
- generate an image from a style refernce
- generate first and last frame with transparent or chroma background
- generate a 5 second video
- create a gif uisng an editor or ffmpeg and remove background
> use WebP instead of GIF (full alpha transparency,  millions of colors instead of 256 etc).

create multiple from same start reference for different reaction animations

tutorial: https://www.youtube.com/watch?v=gi-y_O5v1FQ&loop=0
---

stickerize

pulse loading
infinite scrolling

micro animations
scroll fade in effects
page transitions

3d interactive assets

---

eleven voice driven interface 

---

haptic feedback

card swivel on adding a new resource w haptic feedback
curtain up first time visit reveal https://blog.tubikstudio.com/ui-design-trends-2026/

---

video/gif loop play card/hero


# Happtic feedback

Yes, **modern web pages can trigger haptic feedback on many mobile devices**, but there are limitations.

## 1. Vibration API (Most Common)

Web pages can use the browser's **Vibration API**:

```javascript
// Short vibration
navigator.vibrate(50);

// Pattern: vibrate, pause, vibrate
navigator.vibrate([100, 50, 100]);
```

Example:

```javascript
button.addEventListener("click", () => {
    navigator.vibrate(20);
});
```

### Support

| Platform         | Support                   |
| ---------------- | ------------------------- |
| Android Chrome   | ✅ Good                    |
| Android Firefox  | ✅ Good                    |
| Samsung Internet | ✅ Good                    |
| iPhone Safari    | ❌ No                      |
| iPhone Chrome    | ❌ No (uses Safari engine) |
| iPad             | ❌ No                      |

Apple does not expose the iPhone's Taptic Engine to normal web pages.

---

## 2. Progressive Web Apps (PWA)

Even if installed as a PWA:

```javascript
navigator.vibrate(30);
```

* Android: ✅ works
* iPhone: ❌ still generally unavailable

---

## 3. Advanced Haptics

Native apps can create:

* light tap
* medium tap
* heavy tap
* success pattern
* warning pattern
* impact pattern

Examples:

* React Native
* Flutter
* Android SDK
* iOS SDK

Web browsers generally only expose simple vibration patterns.

---

## 4. Good Uses in Web Apps

Many Android web apps use haptics for:

* Button presses
* Toggle switches
* Completing a task
* Pull-to-refresh
* Timer completion
* Game interactions
* Virtual keyboards

Example:

```javascript
function haptic() {
    if ("vibrate" in navigator) {
        navigator.vibrate(15);
    }
}
```

---

## 5. Best Practice

Always feature-detect:

```javascript
const supportsHaptics = "vibrate" in navigator;

if (supportsHaptics) {
    navigator.vibrate(20);
}
```

This prevents errors on unsupported devices such as iPhones.

### Practical Reality (2026)

| Device         | Web Haptics           |
| -------------- | --------------------- |
| Android phones | ✅ Usually works       |
| Samsung phones | ✅ Usually works       |
| Google Pixel   | ✅ Usually works       |
| iPhone         | ❌ No reliable support |
| iPad           | ❌ No reliable support |

If your audience is primarily Android users, haptic feedback from a web page is quite feasible. If you need reliable haptics on both Android and iPhone, a native app or hybrid app (e.g., Flutter or React Native) is usually required.


# UI/UX Design Reference

![alt text](images/banner.png)

![alt text](images/logo.png)

## Workflow

Collect inspirations
Filter inspiration ideas
Sitemap
Wireframe
Styleguide
Design samples
Create master layout and component library + documentation
Implement Design and build product

## Design Lingo
 
Emotion centric UX
Minimalism
3D and motion
Microinteractions

Glassmorphic
Pnuemorphic

![alt text](<images/ui vs ux.png>)