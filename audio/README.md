# Audio clips

When the speaker is revealed, the game plays `audio/<file>.mp3` for that speaker. The mapping from speaker to file and subtitle is `VOICE_CLIPS` in `index.html`.

If a file is missing or can't play, the game shows the subtitle with a short "audio unavailable" note, so no file is mandatory.

## Files expected

| File | Speaker | Subtitle (what the clip must say) |
|---|---|---|
| `netanyahu.mp3` | בנימין נתניהו | ניחשתם נכון? בזכותי. ניחשתם לא נכון? אשמת התקשורת. |
| `lapid.mp3` | יאיר לפיד | אני יודע בדיוק מה אתם חושבים עכשיו. כתבתי על זה פעם טור. |
| `gantz.mp3` | בני גנץ | שקלתי, התייעצתי, התלבטתי... והחלטתי שזו הייתה שאלה מצוינת. |
| `ben-gvir.mp3` | איתמר בן גביר | מה, באמת לא זיהיתם? אני הכי מוכר בארץ! |
| `golan.mp3` | יאיר גולן | גם בחידון אני ממליץ: לא לוותר, ולענות נכון בפעם הבאה. |
| `zelekha.mp3` | ירון זליכה | בדקתי את המספרים: הניקוד שלכם יקר בארבעים אחוז מבאירופה. |
| `winter.mp3` | עופר וינטר | מי שעונה נכון, מקבל. מי שעונה נכון הרבה, מקבל הרבה יותר. |
| `bennett.mp3` | נפתלי בנט | בדיוק כמו בהייטק: מנסים, נכשלים מהר, ועוברים לשאלה הבאה. |
| `levin.mp3` | יריב לוין | התשובה שלכם התקבלה. ערעור לא יתקבל. |
| `hendel.mp3` | יועז הנדל | במילואים למדנו: גם אם טעית, ממשיכים קדימה. |

## Technical specs

- MP3, mono, 44.1 kHz, 64–96 kbps.
- Up to about 8 seconds and 100 KB per clip, so the files load quickly on GitHub Pages.
- File names must match exactly, because GitHub Pages is case-sensitive.

## Permission rules

**Synthetic voices (`synthetic: true`)**
- All the lines above are invented jokes. They may only be produced with a voice model you have rights to use for this purpose: a licensed, consented voice, or a voice actor doing an obvious impersonation.
- The game shows the "🤖 פרודיה שנוצרה ב-AI" label for these clips. Don't turn it off.

**Real recordings (`synthetic: false`)**
- Use only a clip you have rights to: your own recording, a licensed one, or one whose terms allow reuse.
- Set the subtitle to the exact words spoken, not to the joke above.
- Note the source next to the entry in `VOICE_CLIPS`.

**Not allowed**
- Ripped broadcast audio from channels 11, 12, 13 or 14 without a license.
- Clones made from a politician's voice without their consent.

## Adding a speaker

Add an entry to `VOICE_CLIPS`. The key must equal the `speaker` value used in `questionPool`.
