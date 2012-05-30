!SLIDE center

# Console Trickshots

### https://www.youtube.com/watch?v=4mf_yNLlgic

!SLIDE center

# Show XHR

!SLIDE center execute

    @@@ CoffeeScript
    console.log "here"

!SLIDE center execute

    @@@ CoffeeScript
    console.warn "window is now", window

!SLIDE  execute

    @@@ CoffeeScript
    window.fib = (x) ->
      if x in [0, 1]
        x
      else
        fib(x-1) + fib(x-2)

    console.time 'fib'
    console.log fib(30)
    console.timeEnd 'fib'

!SLIDE  execute

    @@@ CoffeeScript
    console.time 'fib 1'
    console.log fib(1)
    console.timeEnd 'fib 1'
    console.time 'fib 10'
    console.log fib(10)
    console.timeEnd 'fib 10'

!SLIDE execute

    @@@ CoffeeScript
    x = {foo: 'bar'}
    console.log x
    console.log typeof x

!SLIDE execute

    @@@ CoffeeScript
    body = document.body
    console.log body, typeof body

!SLIDE execute

    @@@ CoffeeScript
    console.dir document.body

!SLIDE center takeaway

 - `console.log()` with multiple arguments
 - `console.time()` for quick benchmarks
 - `console.dir()` for inspecting host objects

!SLIDE center

# `$0`

### A reference to the currently inspected element in the Elements panel.

!SLIDE execute

# I am an element

!SLIDE center

# Bonus

# In Chrome, you get `$1`, `$2`, `$3`, and `$4` for the previously selected elements.

!SLIDE

# `$$`
### Bling bling
### Shortcut for `document.querySelectorAll`


!SLIDE center

# `inspect(HTMLElement)`
### Finds and inspects the given DOM element in the Elements panel.

!SLIDE

    @@@ html
    <img
      class="test-image"
      src="..."></img>

<img class="test-image" src="http://i.imgur.com/7ZnFs.gif"></img>

!SLIDE center

# `monitorEvents(HTMLElement, type = '')`
### Quickly logs all or some DOM events on an input

!SLIDE

    @@@ html
    <input
      type="text"
      class="test-input" />

<input type="text" class="test-input" placeholder="Write some text..." style="font-size: 100%;"></input>

!SLIDE center takeaway

 - Use `$0` in the console as a reference to the currently inspected element
 - Use `$$` in the console to select elements on the page (if you don't have jQuery I guess)
 - Use `inspect()` to highlight an element you have a reference to in the Elements panel
 - Use `monitorEvents()` to log all events on an element to the console

!SLIDE

# `Object.keys(object)`
### Returns a list of all the keys an object has in an array
### Also available as `keys()` in the console

!SLIDE execute

    @@@ CoffeeScript
    keys = Object.keys
      foo: 'bar'
      baz: 'qux'

    console.log keys

!SLIDE

# `copy(object)`
### Copies that object's string representation to your clipboard!

<textarea rows="20" cols="70"></textarea>

!SLIDE center takeaway

 - Use `keys` in the console to quickly get the list of keys in an object
 - Use `copy` in the console to copy something to your clipboard... also `pbpaste`.
