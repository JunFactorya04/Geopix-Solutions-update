<p align="center"><img src="geopix_logo.png" alt="Geopix Digital Solutions" width="200"></p>

# Geopix Pro Capture: user guide

For firmware **v2.0** and later. The version a box runs is shown under **SETTING › Info**.

Geopix Pro Capture triggers your camera automatically. Its **TF-Luna** distance sensor sees a
runner, an animal or a car go by and fires the camera over a cable or Bluetooth. It can shoot on
detection, on a timer (timelapse), as a long bulb exposure, and with several boxes working one
shot together.

**Contents**

1. [Basic controls](#1-basic-controls)
2. [Connecting the camera](#2-connecting-the-camera)
3. [AUTO SHOOT: shoot when something passes](#3-auto-shoot-shoot-when-something-passes)
4. [TIMELAPSE](#4-timelapse)
5. [TRIGGER: outputs and Bluetooth](#5-trigger-outputs-and-bluetooth)
6. [TRAIL MODE: semi-automatic bulb](#6-trail-mode-semi-automatic-bulb)
7. [MULTI BOX: boxes working together](#7-multi-box-boxes-working-together)
8. [SLEEP & WAKE: scheduled off / on](#8-sleep--wake-scheduled-off--on)
9. [Phone app (Phone Link)](#9-phone-app-phone-link)
10. [Several boxes from one phone](#10-several-boxes-from-one-phone)
11. [SETTING](#11-setting)
12. [Battery](#12-battery)
13. [Updating the firmware](#13-updating-the-firmware)
14. [Troubleshooting](#14-troubleshooting)

---

## 1. Basic controls

| Action | Does |
|---|---|
| **Hold the power button ~2 s** | Switch the box on |
| **Turn the knob** | Move between items, or change the value being edited |
| **Press the knob** | Select / start editing / save |
| **Hold the knob 1 s, then release** | Go back, or leave the mode for the menu |
| **POWER OFF** card on the menu | Switch the box off |

The knob is locked while it is pressed, so a press never slips onto the next item. A row with `>`
opens another screen; every settings screen ends with **< BACK**.

The screen dims after a while (SETTING › Power Save). Touch the knob once to wake it; that touch
does nothing else. The box keeps shooting while the screen is dark.

## 2. Connecting the camera

The box has two outputs for the camera's remote cable:

- **Shutter**: takes the picture. Every mode uses it.
- **Half press**: focuses. Used by **AF** in Auto Shoot, and by **Half Press G1** in Timelapse
  and Trail Mode.

> In the firmware, Shutter is **G2** and Half press is **G1**. On the case of current batches the
> labels are the other way round: the port printed **G1** is Shutter. Wire by function, not by
> the printed label.

The box can also fire over **Bluetooth**: a Sony camera, or a phone's camera app. See
[section 5](#5-trigger-outputs-and-bluetooth).

**A bulb exposure needs a direct cable to the camera.** Radio triggers such as PocketWizard send
"one press", not a button held for the whole exposure, so a bulb through one comes out as a short
frame. Use a direct cable, or a trigger that can hold its contact.

## 3. AUTO SHOOT: shoot when something passes

The box learns the **background** (the farthest thing the sensor sees, a wall for example). When
something is **closer than the background** by enough, it shoots.

Place the box so the sensor looks across the path, with something fixed behind it. After entering
the mode, give it a few seconds to learn the background (the header shows the sensor rate,
normally 200 Hz).

**Main screen**

| Item | Meaning |
|---|---|
| **Burst** | Shots per detection (1-10) |
| **AF / MF** | **AF**: half press first, wait **Focus Delay**, then shoot. **MF**: shoot at once. Press to choose it and open its settings |
| **Advance >** | Sensor settings |
| **START / STOP** | Start / stop |

- **AF**: Focus Delay 100-300 ms (default 150), Shutter 5-100 ms (default 17).
- **MF**: Shutter 5-100 ms.

**AF delays every shot by the Focus Delay.** If the camera is on manual focus, choose **MF** for
the fastest response.

**Advance**

| Item | Meaning |
|---|---|
| **Cooldown** | Minimum rest between two shots |
| **Detect** | How many cm closer than the background counts. The screen shows the measured noise next to it; **set Detect to at least twice the noise**, or the box will fire at nothing |
| **Retrigger** | While something stays in view, how far it must move to fire again |
| **Min Signal** | Ignore readings with too weak a return (0 = trust every reading) |
| **Range Filter / Min / Max** | Only shoot when the subject is inside this distance band (metres) |

## 4. TIMELAPSE

Shoots at a steady interval, for a timelapse video.

The **main screen** works in video terms: **Shoot Duration**, **Video Length** and **Video FPS**
(24/25/30). Change one and the other two follow.

**Advance**

| Item | Meaning |
|---|---|
| **Interval** | Rest between two shots (0.1 s to 1 hour) |
| **Total Shots** | How many shots, 0 = until Stop |
| **Bulb Mode** | Long exposure: hold the shutter for **Exposure** |
| **Exposure** | Exposure per shot in Bulb (1-900 s) |
| **Settle Delay** | Extra rest after each bulb shot so the camera can write the file (0-120 s) |
| **Half Press G1** | Every shot presses G1 first, then the shutter after **G1 Delay** (set in the phone app); Bulb holds both |

In Bulb, one shot takes **Exposure + Interval (+ Settle)**: the Interval is the **rest after the
exposure**, not from the start of the previous shot.

Press **START** to run, again for **PAUSE**, then **RESUME** to carry on. Pausing or stopping in
the middle of a bulb exposure closes the shutter at once. The first shot comes one Interval after
Start.

In the phone app the Timelapse page adds a **planner**: tap *Shoot time*, *Video* or *Shots* to
type a number and the app works out the rest. It also has quick presets (City, Clouds, Sunset,
Night sky, Building), the expected finish time, and the seconds of video shot so far. The
**Trigger Out** group sets the shutter pulse, Half Press G1 and the **G1 Delay**.

## 5. TRIGGER: outputs and Bluetooth

| Item | Meaning |
|---|---|
| **Beep** | Beep on every shot |
| **Bluetooth >** | Pair a Sony camera or a phone |
| **Advance > Pulse Width** | Length of the shutter pulse, 1-200 ms (default 6). Shared by every mode except Auto Shoot. Raise it if a camera, flash or radio trigger misses a shot now and then |
| **TEST TRIGGER** | Fire one test shot |

In the phone app, the **Trigger out** card has a **Test** button for each output (G2 shutter and
G1 half press).

**Bluetooth: one device at a time.**

- **Sony camera**: put the camera in Bluetooth pairing mode, then choose **Pair** (the box scans
  for about 10 seconds). Next time use **Connect**. Bulb over Bluetooth works with Sony.
- **Smartphone**: choose **Pair**, then in the phone's Bluetooth settings select
  **GEOPIX Remote**. The box sends "volume up", which the iOS and Android camera apps take as the
  shutter button. There is no bulb for a phone.
- **Forget**: removes that device's pairing.

Bluetooth switches itself off after **60 seconds** without a connection (a yellow countdown on
screen), to save the battery. The wired G2 output always fires, even while Bluetooth is
reconnecting.

## 6. TRAIL MODE: semi-automatic bulb

Made for trail-running photography: **you press to open the shutter, the sensor closes it** when
the runner crosses.

1. Put the box at the "finish line", its sensor looking across the trail.
2. Press **START**: the shutter opens at once (bulb).
3. For the first **Min Bulb**, the sensor is ignored (so you can step out of the frame).
4. After that, when someone crosses the sensor, the box waits **End Delay** and closes. If nobody
   crosses, it closes by itself at **Max Bulb**.

**Single**: one frame per START. **Auto**: after each frame it carries on by itself (rest
**Rest**, wait **Interval**, open again) until STOP.

Advance also has a **Sensor** page (Detect, Min Signal, Range) and **Trigger Out**: the shutter
always fires; **Half Press G1** (with its **G1 Delay**, set in the phone app) and Bluetooth are
optional.

In the app: the exposure timer, a large Shoot/Stop button, a 30-second distance chart, and the last
8 exposures (green = closed by the sensor, orange = reached Max Bulb, grey = Stop pressed).

## 7. MULTI BOX: boxes working together

Several boxes take one bulb shot together: the **Start box** sees the athlete set off and tells the
**Main box** (connected to the camera) to open the shutter; the Main box's own sensor sees them
finish and closes it. An optional **Flash box** fires a flash along the way.

| Role | Job |
|---|---|
| **Main** | Connected to the camera, opens and closes the bulb; its sensor is the finish line. Only one Main |
| **Start** | Its sensor is the start line. Only one Start |
| **Flash** | Connected to a flash, fires it when someone passes (with **Flash Delay**) |

**How to use it:**

1. Give each box a **Box Name** (SETTING › Phone Link): A, B, C… The **Node ID** follows the name
   (A = 1, B = 2…) by itself.
2. Open **MULTI BOX** on each box and set its **Role** under **ADVANCE**.
3. Pair the boxes: **Pair / Add Node** on each box, or **Pair all** in the app.
4. Press **START** on the Main box. Main enters the mode **STOPPED** so you can finish setting up
   first; the Start box shows **MAIN STOPPED** until then.
5. **STOP** on Main closes the shutter if it is open and stops the whole group.

Main's settings: **Min Bulb** (never closes sooner), **Max Bulb** (closes by itself), **Rest**
(pause between shots, so a queue of people cannot fire shots faster than the camera can write
them), **End Delay**.

A blinking warning on the bottom line: **ID IN USE** (two boxes with the same name),
**2x MAIN** / **2x START** (two boxes with the same role). Fix the name or the role and it clears.

In the phone app, the Multi Box page manages the whole group: the role of each box, **Open on all**,
**Pair all**, and the Main box's Start/Stop, exposure timer and history.

## 8. SLEEP & WAKE: scheduled off / on

The box switches itself off at **Sleep** and on at **Wake** on the chosen days (its clock keeps
running while it is off). On a scheduled wake it can go straight into **Auto Shoot** or
**Timelapse** and start after a 5-second "AUTO START" countdown, or just show the **Menu**.
Switched on by hand, it always shows the menu.

The schedule runs in every mode, even when SLEEP & WAKE is not open.

## 9. Phone app (Phone Link)

Control a box and see what it is doing from your phone, with no internet needed.

**Connecting:**

1. On the box: **SETTING › Phone Link** (opening this screen switches the box's WiFi on).
2. On the phone: in WiFi settings choose **GEOPIX-A** (after the box's name) and enter the password
   shown on the box's screen.
3. Open Safari at **http://geopix.local** (or **http://192.168.4.1**).
4. Tip: **Add to Home Screen** (Share › Add to Home Screen). Next time just join the WiFi and tap
   the Geopix icon. The same icon works for every box.
5. In the iPhone's WiFi settings, turn on **Auto-Join** for the GEOPIX network so the phone does
   not switch to mobile data (the box's network has no internet).

**In the app:**

- **Modes**: one card per mode. Tap one to see it live and change its settings; **Open on box**
  opens that mode on the box. The card of the mode that is running has a green outline.
- Tap any value to change it on a scroll wheel, or tap **Type** to enter an exact number.
- A setting changes in the app only once the box confirms it. If the box does not answer, the app
  says so and keeps the old value.
- The box's clock is set from the phone every time it connects.
- The icons at the top: WiFi, ESP-NOW (Multi Box), Bluetooth, and the box's battery.
- **Device**: the box's name, firmware, battery and clock, and a QR code to this guide.

Lock the phone and come back: the app reconnects by itself and returns to the page you were on.
The box's WiFi **stays on while it is shooting** (Auto Shoot, Timelapse, Trail, Multi Box) or while
other boxes are linked to it. Sitting on the menu with no phone connected, it switches its WiFi off
after **30 minutes** to save the battery.

## 10. Several boxes from one phone

The phone joins the WiFi of **one box (the hub)**. The other boxes are reached through it. Any box
can be the hub: it is simply the one whose WiFi the phone is on.

**First time, for each other box:**

1. On that box: **SETTING › Phone Link**, set a **Box Name** (B for example), turn **Join hub** ON,
   and **stay on that screen**. Its own WiFi does not need to be on.
2. In the app (joined to the hub): tap **+ Box › Search**, pick the box that is found, tap **Add**.
3. The box shows **"Pair with GEOPIX-A?"**: choose **OK**.

**After that:** the **A | B | C** bar at the top of the app shows each box (green dot = connected,
with its battery). Tap a box to control it: every page works, except firmware updates. **Tap a box
twice quickly** and it beeps, to find which physical box is which.

A linked box can be in any mode and still be controlled. **Join hub** is remembered when the box is
switched off and on. To remove a box: **+ Box › Linked boxes › Remove**. To swap roles (make B the
hub), join B's WiFi and add the other boxes to B.

## 11. SETTING

| Item | Meaning |
|---|---|
| **Date & Time** | Date and time (the phone app also sets it automatically) |
| **Speaker** | Sound on / off |
| **Brightness** | Screen brightness |
| **Power Save** | How long before the screen dims |
| **Theme** | Colour theme |
| **Rotation** | Turn the screen 180° |
| **Phone Link** | WiFi for the app, Box Name, Join hub |
| **Info** | Firmware version |

## 12. Battery

The battery icon is at the top left of every screen. The percentage moves slowly on purpose,
because the voltage dips briefly whenever WiFi, Bluetooth or the sensor are busy.

- **Low battery**: one beep, the icon turns red. The box carries on shooting.
- **Battery empty**: a low beep, the mode exits safely (closing the shutter if a bulb is open,
  saving its settings), then the box switches itself off.

The box cannot yet tell when it is charging or fully charged.

## 13. Updating the firmware

See the [README](README.md#updating-the-firmware): over WiFi on the box (OTA UPDATE), from the phone
app, or over USB. **A box running v1.9 or older must be flashed to v2.0 over USB once.**

## 14. Troubleshooting

| Problem | What to do |
|---|---|
| Auto Shoot fires with nobody there | Raise **Detect** to at least twice the noise shown on screen; check that the background behind is fixed |
| Shots come late | It is on **AF**: switch to **MF** if the camera is on manual focus |
| The camera now and then ignores a shot | Raise **Pulse Width** (TRIGGER › Advance) |
| A bulb comes out as a short frame | A radio trigger (PocketWizard…) is in between: use a direct cable |
| The app will not open | Check the box's WiFi is on (SETTING › Phone Link) and the phone is on the right GEOPIX network, then reopen the app |
| A linked box shows "out of reach" | Check it is on, **Join hub** is ON, and it is in range. If its own WiFi was just switched on and off, switch that box off and on once |
| A box stays on "Loading through the hub…" | Add it to the hub again (+ Box › Search › Add) |
| Multi Box blinks **ID IN USE** | Two boxes share a **Box Name**: rename one |
| The Start box shows **MAIN STOPPED** | Press **START** on the Main box |

---

© Geopix Digital Solutions · [www.geopix.tw](https://www.geopix.tw)
