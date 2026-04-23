# Willow--The-rhythm-game
This is a horror survival based rhythm game. 

Here are some **features** of the rhythm game

__Intro/Manual screen__ — the "The Willow is not a game about perfection" screen that fires on first ever chapter entry

__Three story interludes__ — one per chapter, narrative lore screens before you enter each chapter for the first time
Archive Hub — the full investigation home base with story log, fragment grid, endings shelf, progress bar, case file, interrogation, secret file, chapter nav, re-readable intros

__False Memory System__ — the first time you play a song it runs normally. The second listen, a hidden layer active badge appears in gold, the scene flower changes to 🥀, and the story reveal shows an extra hidden detail. Third listen: memory corrupted in red, the scene shows 🕸, the whole scene briefly desaturates, and the story text warns you that what you're reading may be fabricated by the archive.Same song played differently each listen (base → hidden → corrupted layer)

__Truth vs Performance__ — a new banner appears on every results screen above the story reveal, telling you what your grade actually means narratively: S/A = "FAKE MEMORY — you performed too cleanly, the archive fed you a constructed/fake narrative." B = "REAL CLUE — your imperfect recall cracked its surface." C = "CONFUSED SIGNAL — one of these details is false." F = "CONSUMED — your session is now part of the archive."

__Corruption Events (Dread/Abyss only)__ — three types fire randomly mid-song: notes go completely invisible for 2.5 seconds, controls invert (D↔K, F↔J) for 3 seconds with a banner warning, or audio pitch violently warps and snaps back.

__9 Investigation Fragment__ — collectible clue nodes unlocked by grade, building the full murder board
Three Endings — each with different unlock conditions and choice moments (End I: complete all chapters; End II: S/A on final song; End III: S on all 9)

__Memory Integrity System__ — a second vertical bar on the right side of gameplay (gold vine). Playing too perfectly in a streak of 7+ drains it — the archive feeds you false memories. Hitting Good recovers it. At the end of a song, if integrity is below 30% you get a warning that your recovered evidence may be fabricated. Above 80% with a long perfect streak, it warns you the archive may be constructing what you see.

__Interrogation System__ — in the Archive Hub, "Interrogate the Archive" opens a fullscreen overlay. Three different questions depending on how many songs you've completed. Each has four choices — correct ones unlock fragments and the archive shudders, wrong ones can fire a brief jumpscare flash.

__Secret File ████████.wav__ — visible in the Archive Hub but locked. Clicking it while locked makes it pulse red. Unlocks after you get B or better on 3 songs AND die at least once — revealing Dr. Vael's (who is a suspect) final encrypted log entry.


**UI BASED CHANGES**

__Idle Silence Detector__ — if you don't press anything for 7 seconds during gameplay, a whisper fades in at the centre of the screen: "why did you stop singing?", "she never stopped. why did you?", "silence is the loudest thing you can give it." It resets every time you tap a key.

__Fake Crash__ — on Abyss difficulty on the 3rd+ listen, instead of the normal death screen the game appears to freeze with a crash message: "the willow has stopped responding" and a fake loading bar. After 3.8 seconds it flashes white, then cuts to death. Personalised with your song title and miss ratio/

__UI Button Drift__ — in horror mode, the home screen buttons slowly, subtly drift in random directions via CSS animation. Different delays per button so they move independently.

__Contradiction Detection System__ — fires after B+ on 3 specific songs, a puzzle where you mark which statement logically contradicts the others

__Consumed F-grade echo__ — when you die, your session fingerprint is stored and plays back as distorted audio in your next game

__Background Shadow Character__ — a silhouette appears at the edge of the scene during gameplay and disappears before you can focus on it

__Directional Whisper__ — stereo-panned whispers to left/right ear with Web Audio, visible text on screen edge

__Ghost Button__ — random horror messages appear floating on screen in horror mode

__Don't Play Easter Egg__ — idle on home screen for 20 seconds to unlock a hidden mode

__Arrow keys + WASD both work__ — both mapped simultaneously

__Visual Rhythm Cues__ — as each note reaches ~55% of its fall, a flower emoji blooms at a randomised position in the scene (🌸🌷🌺🌼). Horror notes spawn 💀🕸🩸 instead. The 🌸 character at the bottom of the scene nods slightly on every cue. No text, no UI — just visual beats.

__Button Text Mutations__ — hovering any button in horror mode has a 45% chance of briefly showing an alternate text: "Again" → "Once more?", "leave" → "Stay", "Exit" → "don't go". Reverts on mouseleave.

__Upload Format Guide__ — the upload zone now shows coloured pills: ✓ MP3/WAV/OGG, ⚠ M4A, ✗ FLAC — with inline guidance about renaming files (no spaces, lowercase), converting M4A to MP3, and the exact GitHub Pages folder structure.

__Heartbeat Sync__ — the ♥ indicator in the top-right of gameplay pulses at a BPM calculated from your HP. Full health = calm 60 BPM. Critical HP = 200 BPM panic rhythm. It's subtle — just a small ticking glyph.

__Case File__ — live investigation panel in the Archive Hub showing Victim, Suspects (colour-coded), and redacted Method/Motive that fill in as you progress and complete interrogations.

__Mic Whisper__ — requests mic permission silently on first gameplay. If it detects a loud sound (peak above threshold), it flashes a message like "i heard that." or "the archive recorded that." at the bottom of screen. Fails gracefully if mic is denied.

GitHub Pages audio — loadPlay() now supports a path field on any song object (e.g. path: './audio/song.m4a'). Add that field to the song data alongside your /audio/ folder in the repo and it loads on click. Console prints a clear diagnostic if the path is wrong.
