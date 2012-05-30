!SLIDE center

# Script Debugging

!SLIDE incremental

# The Sources Panel

 - script
 - file drawer
 - sidebar debugging stuff
 - Workers

!SLIDE

# Keyboard Shortcuts

 - `⌘O`: Open File
 - `⇧⌘O`: Go to Symbol

!SLIDE

# `debugger`

!SLIDE huge

# `debugger`

!SLIDE center really-serify big transition=fadeZoom

# debugger

!SLIDE execute

 - Call stack
 - Scope variables
 - evaluate expressions

<br/>

    @@@ CoffeeScript
    foo = (x) ->
      if x == 0
        debugger
        return 0
      foo(x-1)

    foo(10)

!SLIDE execute

    @@@ CoffeeScript
    for num in [1..10]
      num

    # 3000 lines later
    foo = ->
      for num in [0..11]
        true

    bar = (x) ->
      num = x
      foo()
      num

    console.log bar(7)

!SLIDE execute

    @@@ CoffeeScript
    for num in [1..10]
      num

    foo = ->
      for num in [0..11]
        true

    bar = (x) ->
      num = x
      foo()
      debugger
      num

    console.log bar(7)

!SLIDE

# Debugger Keyboard Shortcuts

!SLIDE incremental

 - `⌘/`: Continue ("unbreak"), "continue" in rdb
 - `⌘'`: Step over, "next" or "n" in rdb
 - `⌘;`: Step into, "step" or "s" in rdb
 - `⇧⌘;`: Step out of, "up" or "u" in rdb
 - `^,`: View higher call frame (the one that called this one)
 - `^.`: View lower call frame (the one this one called)

!SLIDE

# Evaluate Selection

 - `^⇧E`: Evaluate current selection in console

!SLIDE execute

# Breakpoints

    @@@ CoffeeScript
    console.log(
      jQuery.parseJSON '{"foo": "bar"}'
    )

!SLIDE execute

# Conditional Breakpoints

    @@@ CoffeeScript
    console.log(
      jQuery.parseJSON ''
    )

!SLIDE center takeaway

 - Use `debugger` to add breakpoints to code
 - Use the stack inspector to look at what is going on
 - Use the console to evaluate stuff
 - Use condition breakpoints to manage loop mayhem

!SLIDE

# More information

# [https://developers.google.com/chrome-developer-tools/docs/scripts](https://developers.google.com/chrome-developer-tools/docs/scripts)
