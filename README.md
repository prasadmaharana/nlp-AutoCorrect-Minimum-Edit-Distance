# Autocorrect with Minimum Edit Distance

This project implements a simple **autocorrect** system based on **minimum edit distance**, originally developed by [Peter Norvig](http://norvig.com/spell-correct.html). It corrects misspelled words by finding the most probable correction from a given corpus.

## Features

- Suggests the most likely correct spelling for a given input word.
- Uses edit distance operations: insertions, deletions, transpositions, and substitutions.
- Based on a probability model derived from word frequencies in a training corpus.

## How It Works

1. A large text corpus is used to build a frequency dictionary of known words.
2. For a given input word, the algorithm generates possible corrections that are:
   - One edit away (`edits1`)
   - Two edits away (`edits2`, optional for wider search)
3. The most probable known word among the generated candidates is returned as the correction.
