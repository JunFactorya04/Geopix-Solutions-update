<p align="center"><img src="geopix_logo.png" alt="Geopix Digital Solutions" width="220"></p>

# Geopix Pro Capture: firmware updates

Geopix Pro Capture is an intelligent automated camera triggering system designed for sports and
event photography, delivering precise, fast, and reliable captures so you never miss a moment.

This repository is where its **firmware** is published. A Geopix box looks for new versions here
when you update it (OTA UPDATE on the box, or the Update page in the phone app).

- **Latest version:** see [Releases](../../releases/latest)
- **User guide:** [USER_GUIDE.md](USER_GUIDE.md)

---

## Updating the firmware

There are three ways. The firmware that is running stays in place until the new one has been
downloaded and verified, so if power or the connection is lost halfway, the box still starts
normally on the old version.

### 1. On the box, over WiFi (OTA UPDATE)

1. On the main menu, open **OTA UPDATE**.
2. Pick a WiFi network **with internet access** (your home WiFi, or your phone's hotspot) and
   enter its password.
3. The box lists the published versions. Pick the one to install and confirm.
4. Wait for the progress bar to finish. The box restarts on the new version.

### 2. From the phone app (v2.0 and later)

1. Join the box's WiFi with your phone (see [Phone app](USER_GUIDE.md#9-phone-app-phone-link)).
2. Open the app and go to **Update**. The app fetches the list of versions from this page over the
   phone's mobile data.
3. Pick the version to install. If the phone cannot download it directly, download
   `geopix_<version>_firmware.bin` from the Releases page and use **Choose a .bin file**.

The box must be on its **main menu** while it updates from the app.

### 3. Over USB (computer)

Use this for a box with no firmware yet, or one running **v1.9 or older** (see below).

**The easy way (M5Burner or any single-file flashing tool):**

1. Download `geopix_<version>_merged_full_flash.bin`.
2. In M5Burner choose **Custom Firmware Burning**, select that file, address **`0x0000`**,
   baud rate 460800 (drop to 115200 if it fails partway).

**With esptool (four files):**

```bash
esptool.py --chip esp32s3 --port <port> --baud 460800 write_flash \
  0x0000  geopix_<v>_bootloader.bin \
  0x8000  geopix_<v>_partitions.bin \
  0xe000  geopix_<v>_boot_app0.bin \
  0x10000 geopix_<v>_firmware.bin
```

A box **with no firmware** does not show up as a USB port: hold the **BOOT** button while plugging
the cable in, and after flashing unplug it and plug it in again normally.

---

## ⚠ Boxes running v1.9 or older

Older versions look for updates at an address that is no longer available. **Flash v2.0 once over
USB** (method 3). From v2.0 on, the box updates itself over OTA or from the app, from this page.

---

## Files in each release

| File | Use it for |
|---|---|
| `geopix_<v>_firmware.bin` | OTA / app updates, or USB flashing at `0x10000` |
| `geopix_<v>_merged_full_flash.bin` | M5Burner: one file at `0x0000` |
| `geopix_<v>_bootloader.bin` | USB, four-file flashing, at `0x0000` |
| `geopix_<v>_partitions.bin` | USB, four-file flashing, at `0x8000` |
| `geopix_<v>_boot_app0.bin` | USB, four-file flashing, at `0xe000` |
| `SHA256SUMS.txt` | Checking that the downloaded files are intact |

On macOS or Linux: `shasum -a 256 -c SHA256SUMS.txt`

---

© Geopix Digital Solutions · [www.geopix.tw](https://www.geopix.tw)
