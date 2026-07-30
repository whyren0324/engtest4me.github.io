# English Test 4 Me

[English](README.md) | [繁體中文](README.zh-TW.md)

A lightweight, no-login browser exercise that selects 20 random entries from an
800-word junior-high English vocabulary list.

[Open the live website](https://whyren0324.github.io/engtest4me.github.io/)

## Problem

Static vocabulary lists are useful as references, but they make it easy to read
in the same order and memorise position instead of meaning. A learner may also
need to manage a spreadsheet or install a larger study application just to run
a short practice session.

English Test 4 Me turns the existing CSV list into a small browser-based drill:

- randomly selects up to 20 words for each session;
- displays the English word, K.K. phonetics, part of speech, Chinese meaning,
  example sentence, and translation;
- highlights the target word inside the example sentence; and
- runs entirely as a static website with no account or server-side database.

## Demo

Select **800 words** to generate a new 20-word set:

![English Test 4 Me demo](docs/demo.gif)

[Launch the interactive demo](https://whyren0324.github.io/engtest4me.github.io/)

## Before / After

| Before: static vocabulary data | After: browser practice |
|---|---|
| Open and scan rows in a CSV file | Select one button to generate a 20-word set |
| Review words in the same order | Receive a different random selection each time |
| Match words, phonetics, meanings, and examples manually | See all six fields in one table |
| Use a local spreadsheet or document | Practice in any modern browser without signing in |

## Installation

### Learners

There is nothing to install. Open the
[live website](https://whyren0324.github.io/engtest4me.github.io/) in a modern
browser.

### Local development

Because the page loads `800.csv` with `fetch`, serve the repository over HTTP
instead of opening `index.html` directly:

```powershell
git clone https://github.com/whyren0324/engtest4me.github.io.git
cd engtest4me.github.io
python -m http.server 8000
```

Then open <http://localhost:8000/>.

## Usage

1. Open the website.
2. Select **800 words**.
3. Review the 20 randomly selected vocabulary entries.
4. Reload the page or select **800 words** again for another set.

The current interface shows all answers immediately; quiz-style answer hiding is
a future enhancement.

## Roadmap

- Add a real question-and-answer mode that can hide meanings or example answers.
- Track progress within the browser without requiring an account.
- Add filters for part of speech, difficulty, and number of questions.
- Improve mobile layout, accessibility, and keyboard navigation.
- Support additional vocabulary sets while retaining source attribution.

Roadmap items are planned directions, not committed release dates.

## Todo

- [ ] Replace comma splitting with a CSV parser that handles quoted commas.
- [ ] Add an empty-data and malformed-row message inside the page.
- [ ] Add a loading and disabled-button state while the CSV is fetched.
- [ ] Improve the table layout for mobile screens.
- [ ] Document the vocabulary dataset's exact source and reuse terms.
- [ ] Add automated checks for CSV row shape and required columns.

## Data

The current exercise reads `800.csv`. Each accepted row contains six fields:

1. English word
2. K.K. phonetics
3. Part of speech
4. Chinese meaning
5. Example sentence
6. Example translation

The original README described the data as an advanced junior-high 800-word list.
The exact publisher, source URL, and reuse terms still need to be documented
before broader redistribution.

## License

No project licence has been declared yet. Until a licence is added, the source
remains available for viewing on GitHub but is not automatically granted an
open-source reuse licence.
