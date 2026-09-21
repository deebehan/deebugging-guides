# The Sunday Rundown

A weekly message that tells a household what is coming up: who is out, who
does drop-off and pickup, what is on, and anything that needs money or a form.
No code, nothing to install. It runs by hand in a Claude or ChatGPT project,
from five documents about your household.

Tested end to end in Claude. See the note on ChatGPT below.

## What is here

| File | What it is | Do you edit it? |
|---|---|---|
| `prompts/1-setup-prompt.md` | Walks you through Google Family, the school calendar, a Gmail label and the weather decision. Ends with a SETUP SUMMARY. | No. Paste it into an ordinary chat. |
| `prompts/2-interview-prompt.md` | Interviews you and writes your five documents as files. | No. Paste it into an ordinary chat. |
| `templates/` | The same five documents, blank, if you would rather fill them in yourself. | Yes. Replace everything in [brackets]. |
| `project-instructions.md` | The short instructions for the project. The same for everyone. | No. |
| `rundown-template.md` | The sixth document. What goes on the page version and how a page run works. | No. |
| `rundown-skeleton.html` | The fixed look of the page. | Only the marked colour values, if you want. |

## Putting it together

1. Run the setup prompt in an ordinary chat, on a computer. Keep the SETUP
   SUMMARY it gives you.
2. Run the interview prompt in an ordinary chat. Download the five files it
   writes. (Or fill in the five in `templates/` yourself.)
3. Make a project called Sunday Rundown. Check Google Calendar and Gmail are
   connected in the app's settings.
4. Paste `project-instructions.md` into the project's instructions.
5. Add your five finished documents to the project's files. If you want the
   page version, add `rundown-template.md` and `rundown-skeleton.html` too.
6. In a new chat in the project, type: `run the Sunday`
   For the page: `run the Weekly Rundown`, check the list it shows you, then
   type: `generate the page`

Do not add a document that still has [brackets] in it. A blank makes the
system invent something to fill it. If you do not know a fact yet, write NOT
SET and say what to report instead, for example: "Usual pickup: NOT SET. Say
'pickup: not assigned' unless the calendar names someone."

## Keep the page private

The page has your children's names, their school and where they are on which
afternoon. Do not publish it or share it by public link. Download the HTML
file and drag it into your browser to read or print it.

## ChatGPT

In Claude, the Google Calendar connection reads a Google Family calendar and a
subscribed school calendar, as long as each is asked for by its exact name,
which is why sources.md names them. ChatGPT may only search your main
calendar. Before you build anything there, start a chat and type:

    List every calendar you can see, by name.

If your family and school calendars are not in the list, either keep the
events you need on your main calendar, or rely on the school emails under your
label for dates.

## When it gets something wrong

Say what was wrong. It will tell you which file the fix belongs in and give
you the corrected file. Replace the old file in the project. Do not fix that
week's message.

| The mistake | The file |
|---|---|
| It read something it should not have, or missed something | sources.md |
| It got a person, a routine or a handoff wrong | household.md |
| It made a bad call about what mattered | rules.md |
| It sounded wrong | voice.md |
| The summary was in the wrong order, or too long | digest-template.md |
| The page had a block missing, misplaced or too long | rundown-template.md |

## Licence

MIT. Use it, change it, build something else out of it. No warranty. It
writes messages about your family, so read what it writes.
