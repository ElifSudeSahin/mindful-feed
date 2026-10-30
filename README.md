# MindfulFeed: Designing Social Media Interfaces That Respect User Attention

An independent HCI / Digital Wellbeing design exploration by a Computer Engineering undergraduate. It is **not** an official university research project and is not affiliated with the authors of the cited work. The designs have **not** been user-tested, and nothing here claims they are effective.

## Evaluate in 2 minutes

1. Open `index.html` in a browser (no build step, no JavaScript).
2. Read the **research question** and the four **heuristics** (H1 to H4) at the top.
3. In **Comparative prototype**, compare the two fictional feeds side by side. Scroll inside each phone screen (mouse wheel, trackpad, touch, or click the screen and use the arrow keys or Page Down). Both contain the same four followed posts. Numbered pins on each mockup match the annotations underneath.
4. Read the **Design-decision summary** table: attention-capturing pattern → mindful alternative → heuristic.
5. Skim **Limitations** at the bottom, and the **Suggested future user study** below.

Files: `index.html` (structure and content), `styles.css` (all styling, variables at the top), `README.md`.

## Problem

Many social media feeds are built to keep people scrolling. Patterns such as endlessly loading feeds and autoplay can make it hard to decide when to stop. Most digital wellbeing tools put the effort on the user (timers, lock-outs). The Digital Attention Heuristics take a complementary view: interfaces themselves should respect attention.

## Research question

How might social media feed interfaces be redesigned to support more intentional browsing and greater user control?

## Design rationale

The prototype draws on four of the eight Digital Attention Heuristics (Monge Roffarello, De Russis & Lukoff, 2025). The other four are not addressed.

| Heuristic | Short description | Response in the Mindful Feed |
|---|---|---|
| H1 Agency | Support the user's sense of agency | Clear feed end; nothing continues automatically |
| H2 Informed Usage | Give users the information needed to decide whether to start or continue a session | Session time and reminder; post counts; followed and recommended posts clearly separated and labelled |
| H3 Balance Goal-Directed and Ritualistic Use | Favor quality of time over quantity | No autoplay, endless loading, badges, streaks or like counts |
| H4 Customization | Let users understand and adapt their environment | Preferences preview (a picture of controls, not working) |

## Design-decision summary

| Attention-capturing pattern (Conventional) | Mindful alternative | Heuristic |
|---|---|---|
| Streak banner and activity badge | No streaks or badges; calm header | H1 |
| Endless loading, no end | Clear "all caught up" end | H1, H3 |
| Autoplaying video with sound | Still thumbnail, no autoplay | H3 |
| Recommended posts mixed in, tiny labels | Separate section, heading, label and border | H2 |
| No session information | Session time, reminder and post count | H2 |
| "Because you watched" strip | Removed; recommendations only in their own section | H3 |
| No visible controls | Preferences preview (non-functional) | H4 |

## Content used in the mockups

All names, posts, images and numbers are invented. Images are CSS-drawn illustrations. Neither feed imitates a real brand.

| Element | Conventional Feed | Mindful Feed |
|---|---|---|
| Followed posts | 4 (Marta, Lena, Omar, Nina), interleaved with other content | The same 4, in a row |
| Recommended posts | 1 video from Trail Notes, inline, autoplaying | The same post, once, after the feed end, separated, no autoplay |
| Extra elements | Streak banner, activity badge, trending chips, "Because you watched" strip, loading indicator | None |
| Engagement counts | Shown (invented numbers) | Hidden, as in the preferences preview |

**Documented difference:** the Conventional Feed intentionally contains extra recommended and attention-grabbing content that the Mindful Feed does not. This is part of what is being compared, not an accident of the mockups. Displayed counts in the Mindful Feed match what is shown (4 followed posts, 1 recommended post).

## Preferences preview

The preferences panel in the Mindful Feed (feed order, recommended posts, session reminder, like counts) is drawn with CSS to resemble real controls. It is a **non-interactive prototype**: it ignores clicks, is hidden from assistive technology as decoration, and states each current value in plain text. No setting works.

## Scrolling behaviour

Both phone mockups have the same fixed height (up to about 720px on desktop, shorter on small screens). The phone frame and its top bar stay still; only the screen inside scrolls, using a plain CSS `overflow-y: auto` area. It works with a mouse wheel, trackpad, touch and keyboard. The screen is focusable (`tabindex="0"`) and labelled as a region, so keyboard users can tab to it and scroll with the arrow keys or Page Down. The numbered annotation lists stay outside the scroll areas.

- **Conventional Feed:** scroll down to the illustrative "Loading more posts…" message. Nothing loads; it is fixed text.
- **Mindful Feed:** scroll through the four followed posts to "You're all caught up", then the separately labelled recommended post and the preferences preview.

Scrolling is the only thing that works. Session timing, preferences and infinite loading are non-functional.

## Accessibility notes

Semantic landmarks and headings, a skip link, visible focus styles (including on the focusable scroll areas), scrollable tables with labels, responsive layout, and text labels in addition to colour (for example "Following" and "Recommended" labels plus different border styles). Colours were chosen with contrast in mind but have not been formally audited. Some low-contrast text in the Conventional mockup (tiny labels, the faded post) is intentional, to illustrate low-emphasis and continuation cues.

## Limitations

- **No user testing.** Effectiveness is unvalidated. No claims are made about reduced screen time, better wellbeing or user preference.
- **Mostly static prototype.** The feeds scroll inside fixed phone screens, but session timing, preferences and infinite loading are non-functional. The session timer, streak and "Loading more posts…" message are fixed text, and the length of the scroll does not reflect real browsing behaviour.
- **Fictional, simplified example.** The Conventional Feed is not a model of any real product.
- **Different content.** The Conventional Feed has extra content by design (see above), so the comparison is of two designs, not a controlled experiment.
- **Illustrated images.** CSS illustrations are less realistic than photographs.
- **Limited scope.** One screen and four of eight heuristics.
- **Possible trade-offs.** A clear feed end may frustrate users who want more content, and session information could itself become a distraction. These are open design questions.

## Suggested future user study

A small within-subjects study could compare the two designs once they are made interactive (for example in a prototyping tool).

- **Participants:** adult regular social media users (sample size to be determined, ideally with a power analysis).
- **Conditions:** Conventional Feed vs. Mindful Feed, order counterbalanced. Use the same core posts in both, and decide in advance how recommended content is matched.
- **Tasks:** a goal-directed task (find a specific post from a followed account) and an open-ended browsing task.
- **Possible measures:** self-reported sense of control and satisfaction; time spent and posts viewed; accuracy in identifying followed vs. recommended posts; whether participants notice and can estimate session length; short interviews about when and why they stopped.
- **Hypotheses (to be tested, not assumed):** the Mindful Feed may improve awareness of session length and content source. Effects on browsing time and satisfaction are open questions.
- **Ethics:** obtain approval from an appropriate ethics board or supervisor before recruiting participants.

## References

- Monge Roffarello, A., De Russis, L., & Lukoff, K. (2025). The Digital Attention Heuristics: Supporting the User's Attention by Design. *ACM Transactions on Computer-Human Interaction*, 32(4), 1-41. https://doi.org/10.1145/3725215
- Monge Roffarello, A., Lukoff, K., & De Russis, L. (2023). Defining and Identifying Attention Capture Deceptive Designs in Digital Interfaces. *Proceedings of the 2023 CHI Conference on Human Factors in Computing Systems (CHI '23)*. ACM.
- e-Lite group, Politecnico di Torino. Digital Attention Heuristics project page: https://elite.polito.it/research/initiatives/digital-attention-heuristics

*Please verify these references against the original publications before submitting.*
