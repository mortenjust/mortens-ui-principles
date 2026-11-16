## UI principles

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
12. Respond visually to interactions in under 50 ms. If the operation cannot finish that quickly, immediately indicate that the request was received. Show loaders for general flows. Show placeholders if you're waiting for items. 
14. Click targets can be larger than their visible contents when useful, without becoming excessive or overlapping other controls.
15. In SwiftUI, give buttons with transparent areas a contentShape so their entire intended area receives clicks. Put padding inside the label before applying the shape.
16. Before writing any code, inspect the closest existing control in the product. Reuse its wording, layout, interaction, and DRY code when it makes sense.
17. After writing code, before considering this done, check this list of UI principles again.
18. Never add elements, buttons, labels, sub-headings, texts, controls, or any other elements I did not ask for.
19. If you insist on breaking this rule, use a subagent to prepare a pitch for me (be brief and visual).
20. Never use all caps for headings, labels, or any other UI text unless explicitly asked. Use normal sentence case.
21. If I'm asking for a technically impossible outcome, find the best possible fallback, build it, and pitch me with screenshots or other relevant artifacts.
22. Never lead the user down a path that will always or frequently end with an error message because you think that's what I want. That is never what I want.
23. Always include a press/active state for a custom button or tab/segmented control. Without it, the button feels unresponsive and broken. If there is a selected state (as in a tab), don't make the press state the same as selected state.
24. Break any of these rules sooner than do anything outright barbaric.

## Text in UI

1. Match the app's voice and vocabulary. Build reference lists if needed.
2. Use words that are familiar to the app's users.
3. Omit needless words.
4. Read out loud to check flow.
5. Put the most important info first.
6. Use the active voice.
7. Don't be cute.
8. Don't be clever.
9. Don't say "Click here". Describe the action.
10. Be consistent.
11. Actions and flows are different. When starting a flow, say something like "Get started", then "Continue" or "Next", and "Done" at the final step.
12. Try not to say "Your" and "My" (e.g. "Projects" instead of "Your projects"). "Unable to load" instead of "We couldn't load".
13. Don't say "click" when the user is on a phone. Don't say tap on a desktop.
14. Empty states: provide clear next steps, either with UI or text.
15. Errors: Don't say oops or darn. Be specific. In general, try to design the UI to minimize and avoid errors.
16. Settings: Short and practical labels. Explain only when ambiguous or unexpected.

## Tooltips

1. When you add a control, add a tooltip.
2. Start the explanation with a verb. "Play animation", "Add animation after the last".
3. Don't repeat the control's text.
4. Max 60 to 75 characters, sentence case.
5. Sentence fragments and omitted articles are OK.
6. If you need more characters, maybe the UI is too complex.
7. Omit ending punctuation.
8. Make the tooltip context-sensitive if needed.
9. Use native tooltips in Swift. Shadcn on web. Standard timing.
10. If the control has a keyboard shortcut and if the control doesn't mention it, mention it in the tooltip. "Play animation (⌘P)"
