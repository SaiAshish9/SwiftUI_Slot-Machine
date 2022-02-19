```
Text("20")
       .fontWeight(.heavy)
       .foregroundColor(isActiveBet20 ? Color("ColorYellow") : Color.white)
       .modifier(BetNumberModifier())
```

```
struct BetNumberModifier: ViewModifier {
  func body(content: Content) -> some View {
    content
      .font(.system(.title, design: .rounded))
      .padding(.vertical, 5)
      .frame(width: 90)
      .shadow(color: Color("ColorTransparentBlack"), radius: 0, x: 0, y: 3)
  }
}
```

```
import SwiftUI

extension Text {
  func scoreLabelStyle() -> Text {
    self
      .foregroundColor(Color.white)
      .font(.system(size: 10, weight: .bold, design: .rounded))
  }
  
  func scoreNumberStyle() -> Text {
    self
      .foregroundColor(Color.white)
      .font(.system(.title, design: .rounded))
      .fontWeight(.heavy)
  }
}
```

```
Text("Your\nCoins".uppercased())
      .scoreLabelStyle()
      .multilineTextAlignment(.trailing)
```
