# 📁 Output Folder Structure - Tahajjud Dua Avatar Studio

## Ye File Kia Kaam Karti Hai?

### 1. **Hindi Voice Generation (TTS)**
   - Text-to-Speech using Qwen TTS (agar available ho) ya Edge TTS
   - Hindi male elder voice (hi-IN-MadhurNeural)
   - Pitch shift karke buzurg awaaz banati hai
   - Output: `.wav` audio files

### 2. **Avatar Video Animation**
   - SadTalker use karke static image ko animate karti hai
   - Audio ke hisaab se lipsync aur facial expressions
   - Calm, spiritual style mein movement
   - Output: `.mp4` video files

### 3. **Automatic Output Management**
   - Har line ka alag video banta hai (5 lines = 5 videos)
   - Audio files bhi save hoti hain
   - Timestamp ke saath organized folders

---

## 📂 Output Folder Structure

Jab aap "Generate" button dabate hain, ye folders automatically banenge:

```
/content/
├── outputs/                          # Main output folder
│   ├── video_line_1.mp4             # Line 1 ka video
│   ├── video_line_2.mp4             # Line 2 ka video
│   ├── video_line_3.mp4             # Line 3 ka video
│   ├── video_line_4.mp4             # Line 4 ka video
│   └── video_line_5.mp4             # Line 5 ka video
│
├── audio_temp/                       # Temporary audio files
│   ├── line_1.wav                   # Line 1 ki audio
│   ├── line_2.wav                   # Line 2 ki audio
│   ├── line_3.wav                   # Line 3 ki audio
│   ├── line_4.wav                   # Line 4 ki audio
│   └── line_5.wav                   # Line 5 ki audio
│
└── final_outputs_YYYYMMDD_HHMMSS/   # Final organized folder (timestamp ke saath)
    ├── video_line_1.mp4
    ├── video_line_2.mp4
    ├── video_line_3.mp4
    ├── video_line_4.mp4
    ├── video_line_5.mp4
    └── audio/                        # Saari audio files ek saath
        ├── line_1.wav
        ├── line_2.wav
        ├── line_3.wav
        ├── line_4.wav
        └── line_5.wav
```

---

## 🎯 Kaise Download Karein?

### Google Colab Mein:

1. **Left sidebar mein folder icon click karein** 📁
2. **Navigate karein:** `/content/final_outputs_[timestamp]/`
3. **Download options:**
   - Individual files: Right-click → Download
   - Pure folder: Zip karke download (terminal mein command use karein)

### Terminal Command for ZIP Download:
```bash
cd /content
zip -r final_outputs.zip final_outputs_*/
```
Phir `final_outputs.zip` file download kar lein.

---

## 📊 File Details

| File Type | Format | Size (approx) | Quality |
|-----------|--------|---------------|---------|
| Videos    | MP4    | 2-5 MB each   | 256x256, 25fps |
| Audio     | WAV    | 500KB-1MB     | 16kHz, Mono |

---

## 💡 Tips

1. **Videos combine karna hai?** 
   - Use any video editor (Shotcut, DaVinci Resolve, etc.)
   - Audio files already synchronized hain

2. **Better quality chahiye?**
   - Cell 2 mein `--size "256"` ko `"512"` se replace karein
   - Note: Higher size = more GPU memory required

3. **Faster generation?**
   - Speed slider ko increase karein (0.85+)
   - Expression scale kam karein (0.3)

---

## ❌ Troubleshooting

### Videos nahi ban rahe?
- Check karein: T4 GPU selected hai? (Runtime → Change runtime type)
- Audio files check karein: `/content/audio_temp/` mein hain?

### Audio kharab hai?
- Speed bahut slow toh nahi? (0.60 se neeche na le jayein)
- Text proper Hindi mein hai?

### Folder nahi dikh raha?
- Colab file browser refresh karein
- Terminal mein `ls /content/final_outputs_*` run karein

---

## ✅ Final Checklist

Before downloading:
- [ ] All 5 videos generated?
- [ ] Audio files present?
- [ ] Folder timestamp se named hai?
- [ ] ZIP banaya (optional)?

Happy creating! 🌙✨
