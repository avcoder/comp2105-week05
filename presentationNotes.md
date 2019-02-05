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
- another analogy is like a CD/DVD player, repeat

# @keyframes animation

- review: this is an example of the structure
- Step 1 is to define the keyframes by giving it a name
- Step 2 is to assign your named keyframe to a DOM element(s) by using keyword 'animation' plus more values

# Step 1

- read it

# 1a) codepen

- All we're going to do is define the keyframes by giving it a name
- fyi - order doesn't matter, can place keyframes before or after element that you're targeting
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

# 5 min challenge codepen iphone wobble

- your challenge is to make it jiggle as if you were rearranging the icons on the iPhone
- so let's define the keyframe -- what property will make it look like it's jiggling? rotate
- 0% { transform: rotate(3deg) }
- 100% { transform: rotate(-2.5deg)}
- Do challenge 3 - explain event propagation

# animation-fill-mode

- read it
- so the question is, do you want the animation do retain its 0% value before the animation starts?
- or do you want the animation to retain its 100% value, otherwise it'll go reset back to the beginning when animation ends
- change 0% value to 100px instead of 0px
- by default set to none
- notice how before animation begins, it starts at very top, then when animation starts it's at 100px down
- backwards: now even before animation begins, it no longer starts at top, it starts at 0% value
- but notice, when aniation ended it reset back to the top
- that's the purpose of the other keyword: forwards
- forwards: retain your 100% value, so once it finishes animating it stays there

# backwards vs forwards

- read it
- or you could have the keyword 'both'
- so that's nice if you don't want your animations to jerk around

# 5 min Challenge clouds codepen

- read it
- what do we want to happen with the cloud? Where should the cloud start?
- -300px to left so we don't even see it
- let's see what happens if we apply drift to both clouds
- now apply a delay to 2nd cloud - what happens? the cloud appears first, then it starts animation - problem!
- use 'backwards'

```css
.fcloud01 {
  top: 100px;
  z-index: 100;
  animation: drift 30s linear;
}

.fcloud02 {
  top: 240px;
  z-index: 200;
  animation: drift 30s 5s backwards linear;
}

@keyframes drift {
  0% {
    transform: translateX(-300px);
  }
  100% {
    transform: translateX(1400px);
  }
}
```

# animation-direction

- read it
- default is normal
- try reverse, alternate (starts from begin to end to beginning), alternate-reverse (opposite of alternate)
- those are your four values

```css
animation: bobble 3s ease-out 2 1s both;
animation-direction: alternate-reverse;
```

# 5 min Challenge animation-direction codepen

```css
@keyframes switchIt {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(200px);
  }
}

animation: switchIt 1s forwards reverse;
```

- paused will make animation stop, until (through JS), you change it to running
- let's make it run via JS

# animation-play-state

```css
animation-play-state: paused;
```

```js
const happy = document.querySelector("#hexagon");
happy.addEventListener("click", () => {
  happy.style.setProperty("animation-play-state", "running");
});
```

# 5 min challenge animation-play-state codepen

- can say paused in 1 of 2 places
- here's a shortcut, if you notice your 0% does nothing, you can delete it -- ones less line of code

```css
/* STEP 2) Apply spin keyframes below using 10s linear infinite. Sticker should spin now */
animation: spin 10s linear infinite;

/* STEP 3) Set by default animation-play-state to paused */
   animation-play-state: paused;
}

/* STEP 4) On .sticker:hover, set animation-play-state to running */
 .sticker:hover {
   animation-play-state: running;
 }
/* STEP 1) Create a keyframes 'spin' so that sticker rotates 1 turn */
 @keyframes spin {
   100% { transform: rotate(1turn); }
 }
```

```js
const spinner = document.querySelector("img");
spinner.addEventListener("click", () => {
  spinner.style.setProperty("animation-play-state", "running");
});
```

# Break

# 5 min challenge starwars

```css
@keyframes logo {
  0% {
    transform: scale(5);
    opacity: 1;
  }
  100% {
    transform: scale(0.1);
    opacity: 0;
  }
}

animation: logo 10s linear;
```
