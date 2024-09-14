https://chatgpt.com/share/0f57ae26-38be-48af-ba83-0c8f83492309

> Learning more about [[Nix's language]] each day.

```
from pynput import keyboard

def on_activate():
    print('Global hotkey activated!')

def for_canonical(f):
    return lambda k: f(l.canonical(k))

hotkey = keyboard.HotKey(
    keyboard.HotKey.parse('<ctrl>+<alt>+h'),
    on_activate)
with keyboard.Listener(
        on_press=for_canonical(hotkey.press),
        on_release=for_canonical(hotkey.release)) as l:
    l.join()

########

This will create a hotkey, and then use a listener to update its state. Once all the specified keys are pressed simultaneously, `on_activate` will be invoked.

Note that keys are passed through `pynput.keyboard.Listener.canonical` before being passed to the `HotKey` instance. This is to remove any modifier state from the key events, and to normalise modifiers with more than one physical button.

The method `pynput.keyboard.HotKey.parse` is a convenience function to transform shortcut strings to key collections. Please see its documentation for more information.
```

- [ ] I'm getting "`l` is not defined", but idk· why since it's a lambda. I can't really test since I don't have a proper coding environment. I think the next thing to do is to set up a VSC· Python playground.