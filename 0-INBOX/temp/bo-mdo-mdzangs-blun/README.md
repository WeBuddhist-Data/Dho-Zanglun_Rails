# bo-mdo-mdzangs-blun — cleaning registry

Source: `1-SOURCES/Text/མཛངས་བླུན་ཞེས་བྱ་བའི་མདོ་ཡི་ཡིག་རྐྱང་ཆ་ཚང་།.txt` (never modified)

## Runs log
| Date | Source file | Script | Output | Notes |
|------|-------------|--------|--------|-------|
| 2026-11-12 | `མཛངས་བླུན་…ཆ་ཚང་།.txt` | `clean-bo-mdo-mdzangs-blun.py` | `cleaned.md` | BOM removed; 53 paragraph breaks added; text verified identical apart from whitespace/BOM |

## Issue registry
### Issue 1 — Byte-order mark
**Pattern:** U+FEFF at file start. **Frequency:** 1. **Solution:** stripped. **Status:** handled (pass 1)

### Issue 2 — Whole text on a single line
**Pattern:** 0 newlines in 518,465 characters. **Cause:** e-text export without paragraph breaks.
**Solution:** break after each section-closing `།། །།` (51 chapter colophons `…ལེའུ་སྟེ…པའོ།། །།` + 2 closing colophons) = 53 paragraphs. **Status:** handled (pass 1)

### Issue 3 — Possible typo, NOT changed (editorial)
**Context:** `ཁྱེདརྐྱག་་པ་ལ་ཟ་ཟའམ` — doubled tsheg and a missing tsheg after `ཁྱེད`. **Status:** left as is; for `[Ed: …]` note at the format step.

## Checked, none found
Page markers, running headers/footers, U+0F0C, mid-word spaces, digits/Latin text, double spaces. The 11,250 spaces after shads (`། `) are ordinary Tibetan spacing, left untouched.
