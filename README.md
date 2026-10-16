# The Roaring Twenties: Interactive Economic Museum

A playable, source-based history museum built as a lightweight website. The website is complete and runs without installing Node.js, React, or any packages. Everything needed for the core exhibits is included locally.

## Start the game

1. Unzip the project folder.
2. Double-click **index.html** and open it in Chrome, Edge, Firefox, or Safari.
3. Choose **ENTER THE MUSEUM**.
4. Enter Gallery 01 and begin exploring.

For local development with a web server, open a terminal inside the project folder and run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

You can host the entire folder on GitHub Pages, Netlify, or another static website service. No build step is necessary. To publish, upload the contents of the folder with `index.html` at the site root.

## How to play

- **W, A, S, D** or **arrow keys**: move the student character.
- **E** or **Enter**: interact with the nearest exhibit or door.
- **Mouse/touch**: click directly on a display or door.
- **On-screen arrow buttons**: movement on a smaller touch screen.
- **Escape**: close a panel.
- **Rooms directory and sidebar**: navigate without moving your character.

Gallery 01 is available immediately. Complete its three-question MCQ assessment with at least two correct answers to unlock Gallery 02. Complete all five economic galleries to unlock the Historical Connections room. The museum saves visited exhibits and passed quizzes in browser local storage.

## Museum galleries

1. America's Postwar Economic Struggles
2. The Economic Boom: Henry Ford and Mass Production
3. The Consumer Revolution and the Bull Market
4. The Uneven Boom: Cities, Suburbs, and Rural America
5. Two Economies: Urban Prosperity and Rural Hardship
6. Historical Connections: Essential Questions and EFFACTs

Each of the first five galleries contains five exhibit stations, a student narration transcript, and a three-question MCQ assessment. Interactive activities include an assembly-line challenge, installment-cost calculator, stock margin simulator, crop revenue calculator, economic cause-and-effect displays, and contextual decision exercises.

Gallery 06 contains four essential-question responses and ten EFFACT cards connected to the main economic topics.

## How to add your student recordings

The student recordings for all five main galleries are included in this project, assigned to their correct galleries, and available in the `audio` folder. The files are named:

```
audio/gallery-01.mp3
audio/gallery-02.mp3
audio/gallery-03.mp3
audio/gallery-04.mp3
audio/gallery-05.mp3
```

The narration panel now displays a play/pause button, timeline, and elapsed/total time directly above the transcript. It loads the matching file from the `audio` folder without a separate server check, so correctly named MP3 files work both from an extracted local folder and on a hosted website. If the file is missing, the player shows a short unavailable message and the transcript remains readable.

**Important:** The accompanying `Roaring_Twenties_Play.html` includes all five gallery recordings embedded inside the HTML, so it can play narration by itself without an adjacent `audio` folder. The ZIP project uses separate MP3 files in `audio/`, which is recommended for website hosting. The sixth gallery has no narration file.

Example structure:

```text
roaring-twenties-museum/
  index.html
  audio/
    gallery-01.mp3
    gallery-02.mp3
    gallery-03.mp3
    gallery-04.mp3
    gallery-05.mp3
  README.md
  SOURCES.md
  NARRATION_SCRIPTS.md
```

The transcript for each room is editable inside `index.html`, in the `narrations` data. A convenient copy is also in `NARRATION_SCRIPTS.md`.

## How to customize

| File | What it controls |
| --- | --- |
| `index.html` | Complete playable website. Its `<style>` section contains the responsive design, the first inline `<script>` contains the exhibit and quiz data, and the second inline `<script>` runs the game. |
| `audio/` | Optional student-recorded gallery narration |
| `SOURCES.md` | Full research and multimedia source list |
| `NARRATION_SCRIPTS.md` | Printable copies of the five transcripts |

No visible museum text should contain em dashes. Keep the writing clear and readable for a high school audience.

## Latest desktop layout

The museum uses a fixed **1100:610 drawing ratio**. The game scales proportionally so the rooms and player retain their original shape on wide or tall computer monitors. A heading above the game identifies the current gallery. Six large labeled cards in the lobby display gallery titles and clear OPEN, LOCKED, or COMPLETED badges. The original student instructions and the left sidebar remain available; the right dashboard has been removed.

## Classroom review before presenting

- All five narration recordings are included. Test playback on the device and browser you will use for the presentation.
- Confirm the teacher's **exact wording** for essential questions C1, C2, and D1. The museum uses accurate museum-specific guiding versions because the precise syllabus wording was not available when built. Essential question A2 uses the original provided wording.
- Check that every external primary source, video and audio link opens on the school's network. Historical media is hosted by its original institution and needs a connection.
- Add your team member names and the teacher's preferred citation formatting if required.
- Have another student complete the full visitor route on the computer used for presenting.

## Accessibility and factual notes

- The character is optional: visitors can click exhibits and use the Rooms directory.
- Transcripts remain available without recordings.
- Historical sources are linked from the exhibit where they are discussed and collected in the Reference Room.
- Calculator values and mini-game scenarios are labeled as teaching examples, not archival statistics.
- The assembly-line image discussed in Gallery 02 is from around 1913, not from the 1920s. It documents the technology that fueled the later boom.
- The phrase *Red Summer* generally refers to 1919 racial violence, not the major strikes that occurred that year.
- The primary purpose of the museum is to explain both 1920s prosperity and the uneven distribution of its benefits.

## Technology and privacy

The project is plain HTML, CSS, and JavaScript, including a Canvas-rendered museum world. It has no backend and does not collect personal information. Only browser local storage is used for visitor progress. Google Fonts may be requested when online; standard fallback fonts display when offline. No analytics or tracking code is included.
