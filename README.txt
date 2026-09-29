A.Irama demo site
=================

Pages
  index.html          Landing page: overview, ensemble mapping, three listeners, composition, findings
  subject01.html      EEG Sonification Map, Subject 01 (EEGMMI S001R01)
  subject02.html      EEG Sonification Map, Subject 02 (EEGMMI S002R01)
  subject03.html      EEG Sonification Map, Subject 03 (EEGMMI S003R01)
  ai-conductor.html   The learning agent: one simulated session as time-lapse audio
  composition.html    Stage map for "Three Minds, One Stage" (full-screen button for projection)

Assets (keep in the same folder as the pages)
  subject01.mp3  subject02.mp3  subject03.mp3  composition.mp3  agent_session.mp3
  portrait.jpg
  AIrama_From_Brainwaves_to_Composition.pdf   (linked from the composition section)

Everything is self-contained. The only external requests are Google Fonts;
without internet the pages fall back to system fonts and still work.

Run locally
  Double-clicking index.html works in most browsers. If audio will not play,
  serve the folder instead:  python -m http.server 8000   then open http://localhost:8000

Publish
  Netlify:       drag the whole folder onto https://app.netlify.com/drop
  GitHub Pages:  push the folder to a repository, Settings > Pages > deploy from branch
  Any web host:  upload all files to one directory

Editing
  Each page is one HTML file with its CSS, JavaScript and EEG data inline.
  Text is plain HTML near the top of each file; the data are in a <script> block
  near the bottom (a JSON object), so edit text without touching that block.
