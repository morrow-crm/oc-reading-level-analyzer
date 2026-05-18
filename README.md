# OC Reading Level Analyzer

A free, browser-based tool that estimates the reading level of a passage using eight established readability formulas.

## What it does

Paste a passage of text — or drop in a `.txt`, `.docx`, or `.pdf` file — and the tool reports a consensus U.S. grade level along with a formula-by-formula breakdown and the underlying text statistics (word count, sentence count, words per sentence, syllables per word, share of complex words).

The consensus number is the median of the seven grade-level formulas, shown with the min–max range across formulas so you can see how much they disagree.

## How to use it

- **Live site:** once GitHub Pages is enabled, the tool is available at the published URL.
- **Locally:** open `index.html` in any modern browser. No install, no build step, no server required.

To analyze a reading:

1. Paste the text into the box, or drop a `.txt`, `.docx`, or `.pdf` file onto the drop zone.
2. Click **Analyze reading**.
3. Read the consensus grade level, the per-formula table, and the text statistics.

## Readability formulas used

The tool reports results from eight formulas:

1. Flesch–Kincaid Grade Level
2. Gunning Fog Index
3. SMOG Index
4. Coleman–Liau Index
5. Automated Readability Index
6. Linsear Write
7. FORCAST
8. Flesch Reading Ease

The consensus grade level is the median of the first seven. Flesch Reading Ease is a 0–100 ease score (higher is easier) and is shown separately.

## A note on Lexile

Lexile is a proprietary measure and cannot be computed from an open formula, so it is not included here. Dale–Chall and Spache are also omitted because they require word-familiarity lists that are not freely redistributable. Syllable counts use a standard heuristic and are approximate.

These formulas measure surface features only — sentence length, word length, and syllable counts — not concept load or background-knowledge demands. A passage of short words and short sentences about an abstract idea will still score "easy." Treat the consensus as a sensible range, not a precise verdict.

## Privacy

All analysis happens in your browser. Nothing is uploaded, stored, or sent anywhere. The `.docx` and `.pdf` parsers (mammoth.js and pdf.js) are loaded from a CDN but run entirely client-side; the document you analyze never leaves your machine.

## Project status

This is **Phase 1** of a free, browser-based reading fluency tool for developmental composition classes at Olympic College, intended to replace a commercial program that became too expensive for students. Later phases will add student logins, audio-recorded oral reading, fluency scoring, an instructor gradebook, and possible Canvas LMS integration.
