# French Notes Workflow

This file records the standing requirements for organizing the notes in this folder.
It should be updated after every meaningful change so future sessions can continue with the same rules and format.

## Folder Structure

- `pdf/`: original source PDFs
- `md/`: Markdown note files
- `docs/`: GitHub Pages publish directory

## Main Files

- `md/french_notes_vocab.md`: vocabulary notes
- `md/french_notes_grammar.md`: grammar notes
- `md/french_notes_exercises.md`: exercises and answers
- `docs/index.html`: GitHub Pages entry page
- `docs/french_notes_vocab_list.html`: vocabulary list HTML
- `docs/french_notes_vocab.html`: vocabulary HTML
- `docs/french_notes_grammar.html`: grammar HTML
- `docs/french_notes_exercises.html`: exercises HTML

## Standing User Requirements

### General Rules

- Ask first when anything is unclear instead of deciding silently.
- Do not change the user’s note content on your own.
- If handwriting or OCR is unclear:
  - either ask the user,
  - or mark it as a possible reading and collect it in a confirmation section.
- Keep the original note content as intact as possible.
- After every later update, also update this `README.md` if the workflow, structure, or formatting rules changed.

### Vocabulary File Rules

- Keep vocabulary separate from grammar and exercises.
- Preserve long explanations, distinctions, and examples.
- Preserve fixed collocations and short phrase notes when they appear in the original notes.
- Do not compress entries into word-only lists.
- `~` means synonym or near-synonym.
- Group near-synonyms clearly when they were presented together in the notes.

### Grammar File Rules

- Keep grammar in a separate file.
- Move structural points, pronoun rules, comparison rules, participles, and similar content here.
- Do not mix exercise content into the grammar file unless it is clearly grammar explanation.

### Exercises File Rules

- Keep exercises in a separate file.
- For each question, include:
  - full question text,
  - all options,
  - answers in a separate answer section.
- If an answer mark is unclear, label it as unclear instead of correcting it.
- If a question is not visible in the extracted source, state that clearly instead of inventing content.
- If the user later provides corrected answers, update the exercise files with the user-confirmed answers.
- If the user confirms that a missing question number was intentionally omitted because it duplicated another question, remove the placeholder instead of keeping a fake entry.

## HTML Rules

- HTML is the main preview format.
- `docs/` is now the only website directory to maintain.
- Keep the HTML pages cross-linked.
- Keep the vocabulary list page and the vocabulary detail page cross-linked.
- `docs/index.html` should remain the easiest starting point.
- Keep `notes.css` inside `docs/`.

### HTML Linking Rules

- Exercise-page vocabulary terms can link to the vocabulary page.
- Linked vocabulary terms in the exercises page should use a distinct highlight color.
- Do not highlight the full question block with a background color.
- Cross-page jumps should open as direct positioning, without slow smooth-scroll animation.
- Cross-page jump targets should flash temporarily when opened, and should not keep flashing after a refresh.
- For exercise-to-vocabulary jumps, the temporary flash should highlight the target term itself rather than the whole block.
- Exercise-to-vocabulary jumps should target the most specific matching item available, not just the broader section heading.
- Vocabulary entries can link back to exercises through `Related exercises`.
- If a vocabulary item appears in multiple exercises, list all related question numbers.
- Vocabulary entry titles in HTML should display like normal headings instead of inline code pills.
- Vocabulary sub-entry labels like `Retourner`, `Tourner`, `Rembourser` should use a distinct emphasis color in HTML.
- Words and example sentences in HTML should not use the blue code background.
- In vocabulary HTML, term labels, sense lines, and example sentences should use different text colors.
- In vocabulary HTML, numbered senses should render as grouped sense blocks, with examples visually attached to the matching sense instead of appearing as flat sibling items.
- In vocabulary HTML display, grouped heading titles should use `/` by default; use `~` only when the grouped items are really synonyms or near-synonyms.
- In the vocabulary detail page, the long grouped vocabulary list/TOC should be placed at the end of the page rather than at the top.
- Single vocabulary items should stay as plain single titles; use `/` only when one list entry intentionally groups multiple words or expressions together.
- The vocabulary list should be a separate HTML page from the detailed vocabulary page.
- The vocabulary list page should keep the grouped list structure and link each item to the detailed vocabulary page.
- In the vocabulary list page, slash-separated display entries should be split into separate list items; phrase-internal words should not be split apart.
- In the vocabulary list page, alphabetical grouping should be based on the actual visible item text after splitting, not on the original grouped heading.
- The vocabulary list page should include a top alphabet navigation bar linking to each letter section.
- The alphabet navigation bar in the vocabulary list page should appear before the other page navigation links.

### GitHub Pages Rules

- `docs/` is the publish directory for GitHub Pages.
- `docs/` is also the working website directory.
- The published site should include a `robots.txt` that asks search engines not to index the site.
- The published HTML pages should include a `noindex` meta tag.
- This reduces discoverability but does not make the site private.

## Future Additions

- More dates will be added later.
- When new date PDFs are added:
  - place the original PDFs in `pdf/`,
  - update the Markdown files,
  - update the HTML files directly inside `docs/`,
  - keep the same separation and formatting rules,
  - update this `README.md` if any new convention is introduced.

## Current State Summary

- Source PDFs have already been moved into `pdf/`.
- Markdown notes have already been moved into `md/`.
- `docs/` is the website directory used both for local preview and GitHub Pages deployment.
- Exercise-page linked terms currently use a distinct orange highlight style.
- HTML jumps now use direct positioning instead of slow smooth scrolling.
- Jump targets now flash temporarily once after navigation, then stop flashing after refresh.
- Vocabulary HTML currently shows `Related exercises` links for mapped entries.
- 07.30 has been integrated into the Markdown files and HTML files.
- Fixed collocations that were missing from the split vocabulary file have started to be restored and should keep being checked when new content is added.

## GitHub Pages Upload

- Easiest setup:
  - use repository `Clorrrrrris/Francais-notes`
  - upload the contents of `docs/`
  - in GitHub repository settings, open `Pages`
  - set source to `Deploy from a branch`
  - choose branch `main` and folder `/docs`
- GitHub will give you a URL like:
  - `https://clorrrrrris.github.io/Francais-notes/`
- Current deployable files are already prepared in `docs/`:
  - `index.html`
  - `french_notes_index.html`
  - `french_notes_vocab.html`
  - `french_notes_vocab_list.html`
  - `french_notes_grammar.html`
  - `french_notes_exercises.html`
  - `notes.css`
  - `robots.txt`
- For later updates:
  - update `md/`
  - update `docs/`
  - push the new files to GitHub
