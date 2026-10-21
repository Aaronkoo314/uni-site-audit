# Nanyang Technological University (NTU) · usability audit · 2026-10-21

Pages read: home https://www.ntu.edu.sg/ (ok, HTTP 200, 219 ms, 156 KB) ·
admissions https://www.ntu.edu.sg/admissions (ok, HTTP 200, 211 ms, 140 KB)
robots.txt: rules read; both pages are allowed.

## Heuristics

| # | Heuristic | Severity | Evidence from the HTML |
|---|---|---|---|
| 1 | Visibility of system status | 2 | `home:headings.h1_count` = 0; `admissions:headings.h1_count` = 0; `home:navigation.aria_current_count` = 0; `admissions:navigation.aria_current_count` = 0; `home:breadcrumbs.present` = true; `home:http.response_ms` = 219 |
| 2 | Match between system and the real world | 1 | `home:navigation.landmarks.0.top_level_links.1` = "Admissions" (plain visitor words in the menu); `home:navigation.landmarks.1.top_level_links.0` = "Corporate NTU" (an organisation name in the breadcrumb); `home:lang` = "en"; `admissions:title` = "Admissions | NTU Singapore" |
| 3 | User control and freedom | 2 | `home:navigation.home_links` = 2; `admissions:breadcrumbs.present` = true; `home:carousel_or_slider_hints` = 19; `admissions:carousel_or_slider_hints` = 12; `home:autoplay_media` = 0; `home:skip_link.present` = false; `admissions:skip_link.present` = false |
| 4 | Consistency and standards | 3 | `home:headings.h1_count` = 0; `admissions:headings.h1_count` = 0; `home:landmarks.main` = false; `admissions:landmarks.main` = false; `home:links.empty_text` = 6; `admissions:links.empty_text` = 1; `home:forms.inputs_without_label` = 1; `admissions:forms.inputs_without_label` = 1; `home:lang` = "en" |
| 5 | Error prevention | 2 | `home:forms.inputs_without_label` = 1; `home:forms.unlabelled_with_placeholder_only` = 1; `admissions:forms.inputs` = 38; `admissions:forms.inputs_without_label` = 1; `admissions:forms.unlabelled_with_placeholder_only` = 1 |
| 6 | Recognition rather than recall | 0 | `home:navigation.landmarks.0.top_level_link_count` = 7; `home:breadcrumbs.present` = true; `admissions:breadcrumbs.present` = true; `home:links.vague_text_total` = 0; `admissions:links.vague_text_total` = 0; `home:search.search_input` = true |
| 7 | Flexibility and efficiency of use | 1 | `home:search.search_form` = true; `admissions:search.search_form` = true; `home:skip_link.present` = false; `home:http.response_ms` = 219; `admissions:http.response_ms` = 211; `home:scripts.external` = 6; `home:meta_viewport` = "width=device-width, initial-scale=1.0" |
| 8 | Aesthetic and minimalist design | 2 | `home:navigation.landmarks.0.links` = 303; `admissions:navigation.landmarks.0.links` = 303; `home:headings.h2_count` = 4; `home:visible_word_count` = 1437; `admissions:visible_word_count` = 1627; `home:carousel_or_slider_hints` = 19; indirect evidence only |
| 9 | Help users recognise, diagnose and recover from errors | not judged | not judged from HTML: error messages appear only after something fails, and a page that loaded normally shows none; `home:forms.inputs_without_label` = 1 is the only related fact |
| 10 | Help and documentation | 0 | `home:help_faq_contact_links.0` = "Frequently Asked Questions"; `home:help_faq_contact_links.1` = "Contact Us"; `admissions:help_faq_contact_links.1` = "Contact Us"; `home:footer_contact.phone_pattern` = true; `home:footer_contact.postal_address_pattern` = true; `home:footer_contact.email_pattern` = false |

Severity: 0 no problem, 1 cosmetic, 2 minor, 3 major, 4 severe (see HEURISTICS.md). Lower is better.

## Three suggestions for the web team
1. **The page title area on every page · Consistency and standards.** Both pages have no `h1` (`home:headings.h1_count` = 0) and no `main` landmark. Please add one `h1` and wrap the main content in `main`, so that assistive tools can jump to the content.
2. **The top of each page · Flexibility and efficiency of use.** There is no skip link (`home:skip_link.present` = false). Please add a "Skip to main content" link before the 303-link menu so keyboard users do not have to tab through it.
3. **The text box in the header or page form · Error prevention.** One input has only a placeholder and no label (`forms.unlabelled_with_placeholder_only` = 1 on both pages). Please add a visible or screen-reader label, because a placeholder disappears when someone types.

## Since last week
First audit; nothing to compare yet.

## Limits
Judged from the HTML of two pages only. Visual design, colour contrast and real tasks were not judged.
These findings are prompts for a human evaluator, not verdicts.
