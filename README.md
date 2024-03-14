- 👋 Hi, I’m @Janugaz
-from moviepy.editor import *
from gtts import gTTS
import os

def text_to_speech(text, language='en'):
    tts = gTTS(text=text, lang=language)
    tts.save("output.mp3")

def generate_video(text):
    clip = TextClip(text, fontsize=70, color='white', bg_color='black').set_duration(5)
    clip = clip.set_pos('center')
    clip = clip.set_audio(AudioFileClip("output.mp3"))
    clip.write_videofile("output.mp4", fps=24)

def main():
    input_text = input("Enter the text you want to convert to video: ")
    text_to_speech(input_text)
    generate_video(input_text)
    os.remove("output.mp3")

if __name__ == "__main__":
    main() 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Janugaz/Janugaz is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
