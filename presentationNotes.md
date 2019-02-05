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

# shorthand animation

- just like transition from last week, the short hand is put everything in one line
- order does not matter, except one -- which order matters (just like transition)?
- Do 1 min codepen exercise

# Challenge starwars codepen

- 3 mins: recreate this fade-in and fade-out of the intro to starwars (play youtube clip)
- code it

# transition vs animation

- analogy of plain saw vs powersaw - so far we've seen that animation has breakpoints

# but wait.. more

- but it has more props for animation, here's the answer
- iteration-count : can define how many times does it repeat? By default it repeats 1 time, but can say 2, 3, infinite
- another one is called fill-mode, can set it to forwards, backwards, both or none.

# animation-iteration-count

- read it
- code it by adding animation-iteration-count: 2
- try 3
- try infinite
- try 1.5

# challenge codepen iphone wobble

- your challenge is to make it jiggle as if you were rearranging the icons on the iPhone
- so let's define the keyframe -- what property will make it look like it's jiggling? rotate
- 0% { transform: rotate(3deg) }
- 100% { transform: rotate(-2.5deg)}
- Do challenge 3 - explain event propagation

# animation-fill-mode

- read it
- so the question is, do you want the animation do retain its 0% value before the animation starts?
- or do you want the animation to retain its 100% value, otherwise it'll go reset back to the beginning when animation ends
