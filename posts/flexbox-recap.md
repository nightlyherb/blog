---

title: Flexbox Recap

date: 2022-10-17

categories:
    - programming
    - frontend

tags:
    - CSS

---

# Flexbox Recap

## Terminology

-   Nouns
    -   `content`: The occupying line of content in a flexbox.
        -   Can span multiple lines.
    -   `items`: The child elements.

-   Verbs
    -   `justify`: as in "justify text".
        -   Naturally means aligning items along the main axis.
    -   `align`: align the items along the cross axis.
        -   I could not find an intuitive understanding here.

-   Verb-Noun Applications
    -   `justify-content`: Justify the child items inside the flexbox line
    -   ~~`justify-items`~~: Ignored in flexbox
    -   `align-content`: Align the lines of content (along the cross axis)
    -   `align-items`: Align the items (along the cross axis)

## Gotchas

- `flex` properties go to the child,
  but `flex-wrap` (not related) goes to the parent.
