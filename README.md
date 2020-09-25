# Android-QuickNotes

### Data Binding
 Less code: By keeping code in activities and fragments small, it helps you write cleaner and more readable code.
Fewer errors: The binding is checked at compile time.
Faster apps: Since the binding isn’t done in onCreate, your app runs faster.
Safer connection between views and code: Because it doesn’t bind at runtime, it’s safer to get the UI components than findViewById().
Safer connection between views and action: Data binding is safer than relying on onClick(), which can crash if you didn’t implement the requested method.
Easier: Since it has less code and causes fewer errors, it’s easier to test and maintain.

### Room

#### Understand why Room doesn't allow object references:

Mapping relationships from a database to the respective object model is a common practice and works very well on the server side. Even when the program loads fields as they're accessed, the server still performs well.

However, on the client side, this type of lazy loading isn't feasible because it usually occurs on the UI thread, and querying information on disk in the UI thread creates significant performance problems. The UI thread typically has about 16 ms to calculate and draw an activity's updated layout, so even if a query takes only 5 ms, it's still likely that your app will run out of time to draw the frame, causing noticeable visual glitches. The query could take even more time to complete if there's a separate transaction running in parallel, or if the device is running other disk-intensive tasks. If you don't use lazy loading, however, your app fetches more data than it needs, creating memory consumption problems.

Object-relational mappings usually leave this decision to developers so that they can do whatever is best for their app's use cases. Developers usually decide to share the model between their app and the UI. This solution doesn't scale well, however, because as the UI changes over time, the shared model creates problems that are difficult for developers to anticipate and debug.
