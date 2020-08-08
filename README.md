# Android-QuickNotes

### Data Binding

    Less code: By keeping code in activities and fragments small, it helps you write cleaner and more readable code.
    Fewer errors: The binding is checked at compile time.
    Faster apps: Since the binding isn’t done in onCreate, your app runs faster.
    Safer connection between views and code: Because it doesn’t bind at runtime, it’s safer to get the UI components than findViewById().
    Safer connection between views and action: Data binding is safer than relying on onClick(), which can crash if you didn’t implement the requested method.
    Easier: Since it has less code and causes fewer errors, it’s easier to test and maintain.

