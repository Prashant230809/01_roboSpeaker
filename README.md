# Narrating program using Python
```python
from gtts import gTTS
import pygame
import time

def pronounce_word(word, lang='en', slow=False):
    # Convert text to speech and save as an mp3 file
    tts = gTTS(text=word, lang=lang, slow=slow)
    tts.save("word.mp3")
    
    # Initialize pygame mixer
    pygame.mixer.init()
    
    # Load the mp3 file
    pygame.mixer.music.load("word.mp3")
    
    # Play the mp3 file
    pygame.mixer.music.play()
    
    # Wait until the sound finishes playing
    while pygame.mixer.music.get_busy():
        time.sleep(0.1)

# Example usage
pronounce_word("hello I am Prashant")

```
