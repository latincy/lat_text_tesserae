# Changelog

All notable changes to this project will be documented in this file.

## [0.4] - 2026-06-11

### Changed
- Normalized whitespace and Unicode across 661 files, with **no changes to textual content** (verified whitespace/NFC-only, zero content loss):
  - Converted CRLF and stray carriage returns to LF line endings (182 files).
  - Collapsed erroneous double spaces in text bodies to single spaces (467 files); citation tags left unchanged, as their internal spacing is systematic.
  - Removed leading/trailing blank lines and ensured a single trailing newline.
  - Applied NFC Unicode normalization to precomposed/decomposed Greek (220 files), matching the LatinCy canonical form.

### Fixed
- Repaired legacy mojibake (UTF-8 text previously decoded as Latin-1) in 58 files, recovering 924 Greek characters and restoring em-dashes — e.g. the Homeric phrase `ζείδωρος ἄρουρα` in Pliny. Repair was confined to the corrupted byte regions: all ASCII Latin text, citation tags, and structure are byte-identical, and output is NFC.

## [0.3] - 2026-06-05

### Changed
- Lowercased words that are not sentence initial or proper names across 73 verse files (Horace, Lucan, Terence, and others) with the goal of improved NLP annotations—particularly lemmatization and named entity recognition—with LatinCy pipelines and LatinCy Readers.

## [0.2] - 2026-03-31

### Changed
- Split multi-book bundled `.tess` files into one file per book. Livy (4 bundled → 35), Pliny the Elder (7 → 37), and Scriptores Historiae Augustae (4 → 21) now follow the one-file-per-book convention used by all other authors in the corpus.

## [0.1] - 2026-03-31

### Added
- Initial release of the LatinCy fork of the Tesserae Latin corpus. Updated README and metadata for use with the LatinCy NLP pipeline.
