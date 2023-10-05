<h1>xdotool</h1>

`xdotool` allows you to mimic keyboard input, manipulate mouse actions, adjust window positions and sizes, and more.

<h2>Installation</h2>

* Debian and Ubuntu: `apt-get install xdotool`

<h2>Usage</h2>

I used this library to automatically resize a window and place it in the desired position on the screen.

<h3>Searching for a window ID</h3>

```
xdotool search --onlyvisible --name <window_name>
```

<h3>Set the window size</h3>

```
xdotool windowsize <window_id> <width> <height>
```

<h3>Move the window</h3>

```
xdotool windowmove <window_id> <x> <y>
```

<h2>Tips</h2>

* `xdotool` allows you to chain several commands together.
```
xdootool search --onlyvisible --name <window_name> windowmove <x> <y>
```
