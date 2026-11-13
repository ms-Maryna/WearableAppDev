# Presentation and demo plan

We compare how a user scrolls through a list on Wear OS and watchOS. We run two sample apps and
explain the code behind what the audience sees.

- [Bernie](https://github.com/ms-Maryna/WearableAppDev/issues/4) introduces the two platforms and
  explains why screen size matters when browsing a list on a watch.
- [Hanna](https://github.com/ms-Maryna/WearableAppDev/issues/2)
  uses [Google’s Wear OS codelab](https://developer.android.com/codelabs/compose-for-wear-os#6) to
  show how Kotlin and Compose change the size and opacity of rows near the edge of a round screen.
- [Nikita](https://github.com/ms-Maryna/WearableAppDev/issues/3)
  uses [Apple’s Landmarks sample](https://developer.apple.com/tutorials/swiftui/creating-a-watchos-app)
  to show how to scroll a SwiftUI list with the Digital Crown and tap a row to open its details.
- [Maryna](https://github.com/ms-Maryna/WearableAppDev/issues/5) uses both demos to explain one
  similarity and one difference, then presents the team’s conclusions.

All four of us review both apps so anyone can answer questions about either demo.

## What to look for in both demos

Both apps put more items in a vertical list than the watch can show at once. Follow one item in each
demo and describe what happens as it enters the screen, reaches the middle and leaves view.

| Question for the team                        | Wear OS codelab                                                                                                                   | Apple Watch Landmarks                                                                                                                     |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| How does the user browse the list?           | Scroll through the sample components. Watch a row near the edge of the round screen.                                              | Turn the Digital Crown to find a landmark. Notice how much of each row is visible as it passes.                                           |
| Which code explains what we see?             | Find `TransformingLazyColumn` and the transformation applied to its items. Connect those lines to the change in size and opacity. | Find the SwiftUI `List` in `LandmarkList` and the view for an individual row in `LandmarkRow`. Match one row on screen to its definition. |
| What did the developers adapt for the watch? | Compare the same list before and after the codelab introduces the scroll transformation.                                          | Compare the shared list on iPhone and Apple Watch, then tap a landmark to see the watch-specific detail view.                             |

