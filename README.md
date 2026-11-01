PulseBottle-ad
A 20-second animated product advertisement for PulseBottle, a fictional smart water bottle used as a placeholder product. The ad has a hook, three product highlights and a call to action, built with kinetic typography, icon motion and a synthesized soundtrack.
Watch: `PulseBottle_Ad.mp4` (click the file, then play it in the GitHub viewer)
Video specs
Property	Value
Duration	20 seconds
Resolution	1920×1080 (16:9)
Frame rate	30 fps
Video codec	H.264
Audio	AAC stereo, synthesized music and sound effects
Voiceover	None (the script appears as on-screen text)
Scene breakdown
Time	Scene	What happens
0:00–0:03	Hook	"Forgot to drink water? Again?" with a buzzing reminder card and an empty glass
0:03–0:06	Product reveal	Liquid wipe transition, bottle drops in with a bounce, wordmark appears
0:06–0:10	Highlight 1: smart glow	Cap LED glows with ripples and a bell icon, "Glows to remind you"
0:10–0:14	Highlight 2: app tracking	Droplets fly to a phone, ring chart fills to 1,600 ml, "Tracks every sip"
0:14–0:17	Highlight 3: 24-hour cold	Ice cubes drop in, counter runs to 24h, frost spreads at the edges
0:17–0:20	Call to action	"Hydration, handled." with a pulsing "Order now" button and URL
Design
Palette: deep blue `#0E1A2B`, aqua `#2ED3F0`, coral `#FF6B4A`, white `#FFFFFF`
Fonts: Poppins ExtraBold / Bold (headlines), Inter Medium (labels)
Motion: word-by-word type with overshoot, squash-and-stretch bottle landing, liquid wipe transition, animated ring chart and counters, ripple and frost effects
Sound: pad chords, kick, bass and arpeggio, plus whooshes, chimes, counter ticks and a button click
Suggested voiceover
The video has no recorded voice. These lines match the scene timing:
Time	Line
0:00	Forgot to drink water? Again?
0:03	Meet PulseBottle.
0:06	It glows when it's time to sip.
0:10	Syncs with your phone to track every sip.
0:14	Keeps drinks cold for 24 hours.
0:17	PulseBottle. Hydration, handled. Order now.
To mix in a recording without re-encoding the picture (requires ffmpeg):
```bash
ffmpeg -i PulseBottle_Ad.mp4 -i voiceover.wav \
  -filter_complex "[0:a]volume=0.5[m];[m][1:a]amix=inputs=2:duration=first[a]" \
  -map 0:v -map "[a]" -c:v copy -c:a aac -b:a 192k PulseBottle_Ad_VO.mp4
```
Placeholders
Product: PulseBottle is fictional. Replace the name and features with your own.
URL: `yourbrand.com` is not a real website.
How it was made
Frames were drawn programmatically in Python (Pillow and NumPy), encoded scene by scene with ffmpeg, joined without re-encoding, and mixed with a synthesized audio track.
License
Add a `LICENSE` file to set the terms for this repository. Poppins and Inter are licensed under the SIL Open Font License, and the audio is synthesized with no third-party samples.
