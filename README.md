# EmojiLover

Welcome to **EmojiLover**, a simple SwiftUI app where users can choose their favorite emoji from a predefined list! This project is a fun way to explore SwiftUI concepts such as enums, states, views, and navigation.

## About the Project

In this project, I learned the following Swift and SwiftUI concepts:

- **Enums**: I used the `Emoji` enum to define a set of emojis. The `CaseIterable` protocol was implemented to easily iterate over all cases in the enum.
- **State Management**: I used the `@State` property wrapper to keep track of the user's emoji selection.
- **SwiftUI Views**: I created a custom view using SwiftUI, which displays a navigation view containing a large emoji and a segmented picker.
- **Navigation**: The app features a simple navigation bar with the title "Emoji Lovers!".
- **Picker**: The segmented picker allows users to switch between different emojis, making the UI interactive and responsive.

### Code Highlights

Here is a brief explanation of the key parts of the code:

```swift
enum Emoji: String, CaseIterable {
    case 😆, 👍🏻, 🐣, 🐱
}
```
Emoji Enum: This enum holds four different emoji cases. The CaseIterable protocol makes it easy to loop through them in the Picker.

```swift
@State var selection: Emoji = .🐣
```
State Management: The @State property allows the view to dynamically update when the selected emoji changes.

```swift
Picker("Select Emoji", selection: $selection) {
    ForEach(Emoji.allCases, id: \.self) { emoji in
        Text(emoji.rawValue)
    }
}
.pickerStyle(.segmented)
```
Picker: The picker displays all the emoji options in a segmented style, letting users choose between them.



Requirements

- Xcode 15.0 or later
- iOS 17.0 or later

1.	Clone the repository:
```bash
git clone https://github.com/alfaizuna-ios/EmojiLover.git
```

2.	Open the project in Xcode.
3.	Build and run the app on an iOS device or simulator.

What I Learned

This project helped me improve my understanding of Swift and SwiftUI, especially with:

- Handling state using @State.
- Structuring views in SwiftUI.
- Creating interactive UI components like the Picker.

I look forward to further enhancing my SwiftUI skills and building more complex projects!

 
