# to include

- devtools layers panel chrome https://www.youtube.com/watch?v=6je49J67TQk&feature=youtu.be
- https://css-tricks.com/inspecting-animations-in-devtools/
- cheerful pineapple https://codepen.io/Elwend/pen/qoLqap?editors=1100
- accessible spinner https://codeburst.io/how-to-create-a-simple-css-loading-spinner-make-it-accessible-e5c83c2e464c
- inspiration: https://uxplanet.org/10-creative-loading-indicators-1a15c562b75a
- css spinners https://twibbr.com/css-spinners/
- https://keyframes.app
- http://animista.net/
- inspiration: https://icons8.com/articles/ui-animation-creative-concepts-of-animated-icons/
- https://codepen.io/avcoder/pen/qYBgBp
- https://css-tricks.com/svg-line-animation-works/

# todo

- read it

# quote Sarah

- read it

# Why keyframes?

- read it

# @keyframes animation

- review: this is an example of the structure
- Step 1 is to define the keyframes by giving it a name
- Step 2 is to assign your named keyframe to a DOM element(s) by using keyword 'animation' plus more values

# Step 1

- read it

# 1a) codepen

- All we're going to do is define the keyframes by giving it a name
- Review last week's class of transforms and transitions - make rocket move using transform/transition
- Now, let's recreate that exact thing using animation
- First step - define @keyframes (plural 's') and give it a name

# 1b) codepen

- now you want to declare the visual changes
- erase all the transform/transition code
- code Step 1 - btw, could also say from, to which is good for simple 2 states
- but most people use the percentages because you can say 25% or 50%
- just because I made a keyframe it won't work unless you use/assign it.

# 2) codepen

- So let's assign it by adding our 'launch' name -- is it working now? No because at minimum you need a duration
- code duration - now it should play
- fyi: can change
- so we just recreated it using animation -- what's the big deal? Assign break points
- code Step 2
- you can also have animation-timing-function (try a cubic-bezier)
- you can also have a delay (try a 1s delay)
- notice these are same 4 props as transition - nothing new - same as last week's material
- code Step 3, and 4

# Challenge starwars codepen

- 3 mins: recreate this fade-in and fade-out of the intro to starwars (play youtube clip)
- code it

# shorthand animation

- just like transition from last week, the short hand is put everything in one line
- order does not matter, except one -- which order matters (just like transition)?
- (use short hand notation in previous codepen example)
