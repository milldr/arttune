# Step-by-Step Audio Tuning Guide for Call of Duty: Black Ops 6

This guide will help you optimize your audio settings for Call of Duty: Black Ops 6 using various software tools.

---

## 1. Introduction and Preliminary Notes

**Timestamp:** [00:00:00](https://www.youtube.com/watch?v=brFUbWlnbao&t=0s)

- **Do not skip steps**; watch the guide thoroughly.
- Use a separate device to follow along.
- Acknowledge that some in-game audio issues are due to the game's engine and may persist until patched.

---

## 2. Uninstall Previous Audio Configurations

**Timestamp:** [00:05:20](https://www.youtube.com/watch?v=brFUbWlnbao&t=320s)

- Open **Add or Remove Programs** in Windows.
- Uninstall the following applications:
  - **AIO Bridge Hi-Fi Cable**
  - **Equalizer APO**
    - Check **"Remove configurations and registry backups"** during uninstallation.
  - **ReaPlugs**
    - Click **No** when prompted during uninstallation.
  - **VoiceMeeter**

- **Restart your PC** after uninstallation.

---

## 3. Install Required Applications

**Timestamp:** [00:07:00](https://www.youtube.com/watch?v=brFUbWlnbao&t=420s)

- **Download the App Pack** from the provided Google Drive link or individual websites.
- **Extract** the downloaded zip file.
- **Install applications in the following order:**

### a. Hi-Fi Cable

- Navigate to the **Hi-Fi Cable** folder and run the installer.
- Click **Install**.
- When prompted to reboot, select **Restart later**.

### b. VoiceMeeter

- Navigate to the **VoiceMeeter** folder and run the installer.
- Click **Install**.
- Do not reboot when prompted.

### c. Equalizer APO

- Run the **Equalizer APO** installer.
- Install to the default directory: `C:\Program Files\EqualizerAPO`.
- In the Configurator:
  - Check **"Hi-Fi Cable Input"**.
  - Select **"Hi-Fi Cable Input"** and click **"Troubleshooting options"**.
  - Change from **SFX/EFX** to **LFX/GFX**.
  - Click **OK** twice and then **Finish**.

### d. Peace Equalizer

- Run the **Peace** installer.
- Follow the prompts and complete the installation.

### e. HeSuVi

- Install **HeSuVi**.
- Close the application after installation.

### f. ReaPlugs

- Run the **ReaPlugs** installer.
- **Important:** Install to `C:\Program Files\VSTPlugins\ReaPlugs`.

### g. Run the LoudEQEnable script

- Copy the command provided in the script.
- Open **PowerShell as Administrator**.
- Paste the command and press **Enter**.
- Type **A** to accept all changes.
- When prompted for the device name, type: `Hi-Fi Cable Input`.
- Close PowerShell after completion.

### h. Copy the EQ Profile

- Copy `ArtIsWar BO6 VST Base.txt` from the app pack.
- Paste it into `C:\Program Files\EqualizerAPO\Config`.

### i. Finish Equalizer APO

- Open **Equalizer APO** _again_.
- In the Configurator:
  - Check **"Hi-Fi Cable Input"**.
  - Select **"Hi-Fi Cable Input"** and click **"Troubleshooting options"**.
  - Change from **SFX/EFX** to **LFX/GFX**.
  - Click **OK** twice and then **Finish**.

---

## 4. Config HeSuVi

1. Open HeSuVi
2. Common HRIRs: `atmos-.wav`
3. Uncheck `Stereo` under Upmix Content
4. Set `Front` channel to 30

---

## 5. Equalizer APO

1. Open Equalizer APO Configuration Editor
2. Move HeSuVi above peace

---

## 6. Configure Windows Sound Settings

**Timestamp:** [00:32:30](https://www.youtube.com/watch?v=brFUbWlnbao&t=1950s)

- **Open Sound Control Panel:**
  - Press `Win + R`, type `mmsys.cpl`, and press **Enter**.

- **Playback Tab:**
  - Disable every `Voicemeeter In {n}`
  - Only `Voicemeeter Input` should be enabled
  - Set **"Hi-Fi Cable Input"** as the **Default Device**.
  - Configure **"Hi-Fi Cable Input"**:
    - Click **Configure** and set to **7.1 Surround**.
  - Rename **"Hi-Fi Cable Input"** to **Art Tune**
    - Click Properties and rename it
  - **Properties > Enhancements:**
    - Enable **Loudness Equalization**.
    - Click **Settings** and set **Release Time** to **Short**.
  - **Properties > Advanced:**
    - Set **Default Format** to match your hardware output (e.g., **24-bit, 48000 Hz**).

- **Recording Tab:**
  - Disable unnecessary devices (e.g., **VoiceMeeter Aux Output**, **B1**, **B2**, etc.).
  - Ensure **"Hi-Fi Cable Output"** is enabled.
  - Rename Hi-Fi Cable Output to "Art Tune"
  - **Properties > Advanced:**
    - Match the sample rate with the playback settings, (e.g., **24-bit, 48000 Hz**).
---

## 7. GadgetryTech EQ Settings

- **Import Your Headset's EQ Settings:**
  - Visit [**Squiglink**](https://gadgetrytech.squig.link/) or **AutoEQ** websites.
  - Find your specific headset/IEM model, select iit
  - Select Black Ops 6 V1
  - Equalizer tab > AutoEQ
  - Export the EQ settings as a file.
  - In Peace, click the **Import** button.
  - Select your downloaded EQ file.
  - When prompted, choose **"No"** to add filters.
  - Click **Save** and name your profile (e.g., `YourHeadset_BO6_Tuned`).
  - Assign an icon color if desired.

---

## 8. Set Up VoiceMeeter

**Timestamp:** [00:29:25](https://www.youtube.com/watch?v=brFUbWlnbao&t=1765s)

- **Open VoiceMeeter:**
  - Under **Hardware Input 1**, select **"Hi-Fi Cable Input"** using **WDM**.
  - Under **Hardware Out (A1)**, select your actual audio output device (e.g., your headset) using **WDM**.
  - Go to **Menu > System Tray (Run at Startup)**.
  - Open **System Settings/Options**:
    - Set **WDM Input/output** buffers to **256**.

- **Additional Settings:**
  - If experiencing audio issues, increase buffer size incrementally (e.g., to 512).


---

## 9. Configure In-Game Audio Settings

**Timestamp:** [00:36:37](https://www.youtube.com/watch?v=brFUbWlnbao&t=2197s)

- **Launch Call of Duty: Black Ops 6**.
- **Navigate to Audio Settings:**
  - Set **Master Volume** to **100**.
  - Set **Effects Volume** to **100**.
  - Set **Dialogue Volume** and **Music Volume** to preferred levels.
- **Audio Device Settings:**
  - Set **Game Sound Device** to **"Hi-Fi Cable Input (Art Tune)"**.
  - Set **Voice Chat Output Device** to **"VoiceMeeter Input"**.
- **Audio Mix:**
  - Choose **"Treyarch Mix"** or test other mixes to preference.
- **Disable:**
  - **Mono Audio**
  - **Enhanced Headphone Mode**

---

## 10. Testing and Final Adjustments

**Timestamp:** [00:39:08](https://www.youtube.com/watch?v=brFUbWlnbao&t=2348s)

- **Test the Audio Configuration:**
  - Play a match and listen for audio improvements.
- **Adjust HeSuVi Settings:**
  - Open **HeSuVi**.
  - Set **Front Channel Level** to **30** (adjust if necessary).
  - Ensure **Stereo** is unchecked.
- **Volume Adjustments:**
  - Use the **Volume Slider** in VoiceMeeter or your hardware controls.
  - Avoid changing the **Master Volume** in Windows to prevent altering the EQ effect.

---

**Note:** This guide aims to enhance in-game audio, specifically footsteps and ambient sounds, by fine-tuning your system's audio configuration.

---

For detailed explanations, refer to the original video: [YouTube Video](https://www.youtube.com/watch?v=brFUbWlnbao)
