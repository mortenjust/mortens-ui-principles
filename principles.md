# UI principles

Follow these principles when changing a user interface:

1. Never add labels or explanation text that was not explicitly requested. Preserve accessibility names without adding visible text.
2. Before designing a control, look for similar controls in the product.
3. Match the product's existing style, layout, and interaction experience.
4. Reuse existing components and view code whenever possible to maintain consistency.
5. Keep related controls and information together.
6. Animate only when movement gives needed context, such as preventing a confusing teleport.
7. Apply Occam's Razor to every UI element: does it belong here, would removing it break the experience, and is there a more direct way to do its job?
8. Keep removing elements until nothing else can be removed without breaking the experience.
9. Never use jargon. Choose words anyone can understand.
10. Minimize language. Much of the worldwide audience does not speak English natively.
11. Show rather than tell.
12. Respond to interactions in under 50 ms. If the operation cannot finish that quickly, immediately indicate that the request was received.
13. Click targets can be larger than their visible contents when useful, without becoming excessive or overlapping other controls.
14. In SwiftUI, give buttons with transparent areas a contentShape so their entire intended area receives clicks. Put padding inside the label before applying the shape.
15. Before writing any code, inspect the closest existing control in the product. Reuse its wording, layout, interaction, and DRY code when it makes sense
16. After writing code, before considering this done, check this list of UI principles again.

Inspect the relevant existing UI and components before adding anything. Apply the principles to the requested scope, then verify actual interaction and hit targets. Remove unsolicited copy and redundant controls rather than explaining around an interaction problem.

## Additional shared rules

17. When you add a control, add a tooltip
18. Start the explanation with a verb. “Play animation”, “Add animation after the last”
19. Don’t repeat the control’s text
max 60 to 75 chars, sentence case
20. Sentence fragments and omitted articles are ok
21. If you need more chars, maybe the UI is too complex
22. Omit ending punctuation
23. Make the tooltip context-sensitive if needed
24. Use native tooltips in Swift. Shadcn on web. Standard timing.
25. If the control has a keyboard shortcut and if the control doesn’t mention it, mention in tooltip. “Play animation (⌘P)”
26. Break any of these rules sooner than do anything outright Jira
27. Never add elements, buttons, labels, sub-headings, texts, controls, or any other elements I did not ask for. If you feel I'm about to miss out on something very important, use a subagent to prepare a pitch for me (I'm busy, reading your pitch on the phone, so be brief and visual)
