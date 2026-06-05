# Changelog

All notable changes to this project will be documented in this file.

## [0.3] - 2026-06-05

### Changed
- Lowercased words that are not sentence initial or proper names across 73 verse files (Horace, Lucan, Terence, and others) with the goal of improved NLP annotations—particularly lemmatization and named entity recognition—with LatinCy pipelines and LatinCy Readers.

## [0.2] - 2026-03-31

### Changed
- Split multi-book bundled `.tess` files into one file per book. Livy (4 bundled → 35), Pliny the Elder (7 → 37), and Scriptores Historiae Augustae (4 → 21) now follow the one-file-per-book convention used by all other authors in the corpus.

## [0.1] - 2026-03-31

### Added
- Initial release of the LatinCy fork of the Tesserae Latin corpus. Updated README and metadata for use with the LatinCy NLP pipeline.
