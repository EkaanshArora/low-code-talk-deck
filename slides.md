---
# try also 'default' to start simple
theme: geist
colorSchema: 'dark'
# background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
# class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
# info: |
#   ## Slidev Starter Template
#   Presentation slides for developers.

#   Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Low-Code for Developers

<br>

#### Building a low-code product that devs don't throw out in a week
<br><br><br><br><br>
<a href="https://twitter.com/ekaansh" target=_blank>@ekaansh</a>

---
layout: two-cols
---

<div style="display: flex; place-items: center;flex-direction:column"> 

# About me

<br>
<img src="images/me.jpeg" style="width: 45%;border-radius: 50%;"/>

### Ekaansh Arora
<img src="images/agora-logo.svg" style="width: 15%;"/>
</div>

::right::
<br> <br> <br> <br>
<div style="display: flex; place-items: center;flex-direction:column"> 

- Developer Advocate, <a style="color: rgba(221, 221, 221)" href="https://agora.io" target=_blank>Agora​</a>

- JavaScript Nerd​

- Maintainer of Agora React (Native) UIKit​

- Maker of 3D art and taylor swift metal covers

<logos-twitter /> <a href="https://twitter.com/ekaansh" target=_blank>@ekaansh</a>
<span style="margin:10px"></span>
<fa-github /> <a href="https://github.com/ekaansharora" target=_blank>@ekaansharora</a>
</div>

---
clicks: 11
---

<div v-if="$slidev.nav.currentPage===3" v-motion
    :initial="{ x: 0, y: 10, opacity: 0}"
    :enter="{ x:0, y: 0, opacity: 1, }">

# What's low code
</div>

<div v-click=1 >
  <div v-if="$slidev.nav.clicks>0" v-motion
    :initial="{ x: 0, y: 0, opacity: 0}"
    :enter="{ x:0, y: -15, opacity: 1}">
    <h4 v-click="1"> Abstractions to simplify developer experience that let you focus on things that matter<h4 v-click="2" style="display:inline">++</h4></h4>
</div>
</div>
<div v-click=2 style="display:none"></div>

<div v-if="$slidev.nav.clicks>2 && $slidev.nav.clicks<8" style="position:relative; height: 32vh;display: flex;justify-content: center;">
<div style="position:absolute; bottom:0;">

<div v-if="$slidev.nav.clicks===3">

```mermaid {scale: 0.8}

flowchart BT
CPU

```
</div>
<div v-if="$slidev.nav.clicks===4">

```mermaid {scale: 0.8}

flowchart BT
CPU --> Assembly 

```
</div>
<div v-if="$slidev.nav.clicks===5">

```mermaid {scale: 0.8}

flowchart BT
CPU --> Assembly --> id1(High Level Languages)

```
</div>
<div v-if="$slidev.nav.clicks===6">

```mermaid {scale: 0.8}

flowchart BT
CPU --> Assembly --> id1(High Level Languages) --> Frameworks

```
</div>
<div v-if="$slidev.nav.clicks===7">

```mermaid {scale: 0.8}

flowchart BT
CPU --> Assembly --> id1(High Level Languages) --> Frameworks --> id2(Low Code)

```
</div>
</div>
</div>

<div v-if="$slidev.nav.clicks===8 || $slidev.nav.clicks===9">

## Videocall = 1000s of lines of code
</div>
<div v-if="$slidev.nav.clicks===9">

```tsx
<AgoraUIKit config={config} style={style} callbacks={callbacks} />
```
</div>

<div style="display: flex; flex-direction: row; flex: 1; justify-content: space-around; align-items: center; margin-top: 100px" v-click=10>
  <img src="images/logo1.svg" style="width: 20%; height: 100%"/>
  <img src="images/logo2.png" style="width: 20%; height: 100%"/>
  <img src="images/logo3.png" style="width: 20%; height: 100%"/>
  <img src="images/logo4.svg" style="width: 20%; height: 100%"/>
</div>

<img v-if="$slidev.nav.clicks>10" v-motion
  :initial="{ x: 0, y: 0, opacity: 0}"
  :enter="{ x:0, y: -200, opacity: 1}" src="images/logo-wp.png" style="width: 30%; height: 100%; margin: auto"/>

<!--  low code is umbrella term for everything from drag drop interfaces to frameworks that you need to write code -->
---
layout: two-cols
clicks: 4
---

<div v-if="$slidev.nav.currentPage===4" v-motion
    :initial="{ x: 0, y: 10, opacity: 0}"
    :enter="{ x:0, y: 0, opacity: 1, }">

# Why Low-Code
</div>

<br>

<div v-click="1">

#### “By 2024, low-code application development will be responsible for more than 65% of application development activity.” - Gartner's report

</div>
<br>
<div v-click="2">

#### "Wordpress is still king" - me <p style="display:inline" v-click="3"> (and everyone else)</p>

</div>

<div v-click="4">

WordPress is used by **43.2%** of all websites on the internet in **2022**, an increase from **39.5%** in 2021.

</div>

::right::
<div v-click="4">
  <tweet scale="0.7" style="margin-left: 40px; width: 120%" id="1507028477345558531" />
</div>

---

# What this talk is about

<br>

<v-clicks>

- ### > Thinking Developer Experience
- ### > Low Code first design 
- ### > API patterns

</v-clicks>

---


<div v-if="$slidev.nav.currentPage===6" v-motion
    :initial="{ x: 0, y: 10, opacity: 0}"
    :enter="{ x:0, y: 0, opacity: 1, }">


# Extensibility is **#1**

<tweet id="1123554129882705923" />
</div>

<!-- all good low code tools let you write code, this avoids you hitting a road block, oh can't do this with low code. must throw away everything and then start fresh, that's the worst experience. this is what has been key for wordpress  -->

---
clicks: 4
---
<div v-if="$slidev.nav.currentPage===7" v-motion
    :initial="{ x: 0, y: 10, opacity: 0}"
    :enter="{ x:0, y: 0, opacity: 1, }" style="margin-top: -40px">

# Access low-level code
<!-- <br> -->
<!-- <br> -->

<div v-if="$slidev.nav.clicks === 0">

<img src="/images/3.png" style="width: 600px; height: 250px" />

</div> 
</div>
<div v-if="$slidev.nav.clicks === 1" style="display: flex; flex-direction: row; overflow: hidden">
<div style="width: 50%">

```ts
var canvas = document.getElementById('my_Canvas');
gl = canvas.getContext('experimental-webgl');
var vertices = 
[-0.5, 0.5, 0.0, -0.5, -0.5, 0.0, 0.5, -0.5, 0.0, 0.5, 0.5, 0.0];
indices = [3, 2, 1, 3, 1, 0];
var vertex_buffer = gl.createBuffer();
gl.bindBuffer(gl.ARRAY_BUFFER, vertex_buffer);
gl.bufferData(gl.ARRAY_BUFFER, new Float32Array(vertices), gl.STATIC_DRAW);
gl.bindBuffer(gl.ARRAY_BUFFER, null);
var Index_Buffer = gl.createBuffer();
gl.bindBuffer(gl.ELEMENT_ARRAY_BUFFER, Index_Buffer);
gl.bufferData(gl.ELEMENT_ARRAY_BUFFER, 
new Uint16Array(indices), gl.STATIC_DRAW);
gl.bindBuffer(gl.ELEMENT_ARRAY_BUFFER, null);
var vertCode = 'attribute vec3 coordinates;' +
  'void main(void) {' + ' gl_Position = vec4(coordinates, 1.0);' + '}';
var vertShader = gl.createShader(gl.VERTEX_SHADER);
gl.shaderSource(vertShader, vertCode);
gl.compileShader(vertShader);
```
</div>
<div>

```ts
var fragCode =
  'void main(void) {' + ' gl_FragColor = vec4(0.0, 1.0, 0.0, 1);' + '}';
var fragShader = gl.createShader(gl.FRAGMENT_SHADER);
gl.shaderSource(fragShader, fragCode);
gl.compileShader(fragShader);
var shaderProgram = gl.createProgram();
gl.attachShader(shaderProgram, vertShader);
gl.attachShader(shaderProgram, fragShader);
gl.linkProgram(shaderProgram);
gl.useProgram(shaderProgram);
gl.bindBuffer(gl.ARRAY_BUFFER, vertex_buffer);
gl.bindBuffer(gl.ELEMENT_ARRAY_BUFFER, Index_Buffer);
var coord = gl.getAttribLocation(shaderProgram, 'coordinates');
gl.vertexAttribPointer(coord, 3, gl.FLOAT, false, 0, 0);
gl.enableVertexAttribArray(coord);
gl.clearColor(0, 0, 0, 1);
gl.enable(gl.DEPTH_TEST);
gl.clear(gl.COLOR_BUFFER_BIT);
gl.viewport(0, 0, canvas.width, canvas.height);
gl.drawElements(gl.TRIANGLES, indices.length, gl.UNSIGNED_SHORT, 0);
```

</div>
</div>

<div v-if="$slidev.nav.clicks === 2">

```ts {all}
import * as THREE from 'three';
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
const renderer = new THREE.WebGLRenderer({canvas: document.getElementById('three'));
const geometry = new THREE.BoxGeometry(3, 3.5);
const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
const cube = new THREE.Mesh(geometry, material);
scene.add(cube);
camera.position.z = 5;
renderer.render(scene, camera);
```

</div>

<div v-if="$slidev.nav.clicks === 3">

```ts {all}
const material = new THREE.ShaderMaterial({
    uniforms: uniforms,
    vertexShader: ` your shader code goes here `,
    fragmentShader: ` your shader code goes here `
});
```
</div>

<div v-if="$slidev.nav.clicks === 4">

```ts {all}
const material = new THREE.ShaderMaterial({
    uniforms: uniforms,
    vertexShader:
       `uniform float time;
        uniform vec2 resolution;
        void main()	{
            gl_Position = vec4( position, 1.0 );
        }`,
    fragmentShader:
       `uniform float time;
        uniform vec2 resolution;
        void main()	{
            float x = mod(time + gl_FragCoord.x, 20.) < 10. ? 1. : 0.;
            float y = mod(time + gl_FragCoord.y, 20.) < 10. ? 1. : 0.;
            gl_FragColor = vec4(vec3(min(x, y)), 1.);
        }`
});
```

</div>

---

<div v-if="$slidev.nav.currentPage===8" v-motion
    :initial="{ x: 0, y: 10, opacity: 0}"
    :enter="{ x:0, y: 0, opacity: 1, }" style="margin-top: -10px">

Access low-level code

```tsx
  <AgoraUIKit rtcProps={{appId: '<Agora App ID>', channel: 'test'}} />
```

<img src="images/sc.png" style="width: 45%; margin: auto" />

<div v-click=1>

```ts
  const { client } = useContext(RtcContext)
  await client.enableVirtualBackground(config)
```
</div>
</div>

<!-- if the user needs virtual background that the uikit doesn't support we throw out the entire project unless.. -->

---

<h2 style="display:inline"> Smart defaults </h2>
<h4 v-click="1" style="display:inline">that are built to be overridden</h4>

<br>
<br>

<video loop="true" autoplay="autoplay" muted style="width: 100%; margin:auto">
  <source src="images/screen.webm" type="video/webm">
</video>

<!-- we're trying to do the users work for them, but you don't want to make decision on the user's behalf, so you add smart defaults that work out of the box but can be overridden simply-->

---
clicks: 2
---

## Granularity

<div v-if="$slidev.nav.clicks === 0">

```ts
> step a 
> step b
> step c
> step d
> step e
> step f
```

vs.

```ts
> step abcdef
```
</div>
<div v-click="1">

```ts
> step abcd
> step ef
```
</div>

<div v-click="2">
  <img style="margin: 20px auto" src="https://i.giphy.com/media/Ry1MOAeAYXvRVQLPw3/giphy.webp">
</div>

---

## Give user access to events

What if - I want to do something between step **E** and **F**?

<div v-click=1 >

```ts
> step e
event.emit("some-event-between-e-and-f") // can be blocking / non-blocking
> step f
```
</div>
<div v-click=2 >
  <div v-if="$slidev.nav.clicks>0" v-motion
    :initial="{ x: 0, y: 40, opacity: 0}"
    :enter="{ x:0, y: 20, opacity: 1, transition: { delay: 0 } }">

```ts {1|2|3|4}
> step abcd
doSomethingAfterEventD()
instance.on("some-event-between-e-and-f", doSomethingAfterEventE())
> step ef
```

  </div>
</div>

---

## Give user access to events
#### Giving data back to the user

<div v-click=1>

#### Side Effects
</div>
<div v-click=2>

```js
const ele = document.querySelector('agora-react-web-uikit');

ele.addEventListener('AgoraUIKitEndcall', (e) => {
  ele.remove()
 })
```
</div>

---

## Framework specific design

SwiftUI
```swift
image?.padding(100).resizable().scaledToFit()
```

React Library
```tsx{0|1|3}
<image padding="100" resizable scaled></image>
// vs.
<image style={{padding: "100px"}} resizable scaled></image>
```

<!-- user's already know the framework don't make them learn your syntax -->

---
clicks: 6
---

## Escape hatches

#### An “escape hatch” is an intentional leak in the abstraction layer. It allows users to “escape the abstraction” and reach out to a lower layer  - cdk8s docs

<img src="images/vb.png" v-if="$slidev.nav.clicks===1" style="width: 60%; margin:auto">

<div v-if="$slidev.nav.clicks>1 && $slidev.nav.clicks < 6">

```vb {0|1|2|3|4}
Msgbox "This is myName"
Msgbox "This is "myName""  ' This gives an error
Msgbox "This is ""myName"""
"This is \"myName\""
```
</div>
<div v-click="6">

```jsx
<div dangerouslySetInnerHTML={{__html: '<p>Hello World!</p>'}}></div>
```
</div>

<!-- removing guard rails and letting the user do things that would otherwise be impossible, this might lead to  -->

---
clicks: 5
---
## Taxonomy

<tweet v-if="$slidev.nav.clicks===0" id="1522312354653945857" />

<div v-click=1>

`dangerouslySetInnerHTML`
</div>

<div v-click=2>

```swift {0|1-2|4-5|7-8|10-11|13-14}
x.append(y) //Nonmutating
let	z = x.appending(y) //Mutating

y.formUnion(z) //Mutating
x = y.union(z) //Nonmutating

array.remove(0) ⛔️
array.removeAt(0) ✅

view.removeElement(cancelButton) ⛔️
allViews.remove(cancelButton) ✅
```
</div>
<div v-click=5>

#### opinion: if in doubt, be as explicit as you can
</div>

---

## Docs, docs, docs
<v-clicks>

- \*looks at code\*
- i wonder who wrote this trash
- `git blame`
- EkaanshArora, 2 weeks ago

#### We has met the enemy, and it is us. — Walt Kelly


<img src=images/manual.png style="width: 70%;margin: auto">
</v-clicks>


---

## Handle errors

<tweet v-if="$slidev.nav.clicks===0" id="1535987671868137472" scale="0.7" />
<v-clicks>

- #### > Descriptive error messages, error codes, error description ELI5
- #### > Handle user errors
- #### > Use patterns to show functions that can error

</v-clicks>

<div v-click="4" v-if="$slidev.nav.clicks>3 && $slidev.nav.clicks<6" >

```ts {1-5|7}
try {
  data = methodThatCanError(badConfig)
} catch (e) {
  print(e)
}
...
let data = methodThatCanError(badConfig)
```
</div>
<div v-click="6">

```ts
let {data, error} = methodThatCanError(badConfig)
if (!error) print(data)
```
</div>

---
clicks: 7
---

## Use syntax to avoid user error

<div v-click-hide=3>
<div v-click=0>

#### enums

```cpp {1,2|4|4-8}
string today = "wednesday";
strcmp(today, "Wednesday"); //false
...
enum week { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };
int main()
{
  week today = Wednesday; //prints 4
}
```
</div>
</div>


<div v-click=3 style="margin: -240px 0">

#### getter

```ts {1-3|5-6|7-13|8,15-16}
const object = {}
object.time = new Date().getTime()
return object; 

let myTime = object.time
object.time = 0 //overwritten :(

...

const object = {}
const time = new Date().getTime()
object.getTime = () => time
return object;

let myTime = object.getTime()
object.getTime = 0 // doesn't make sense anymore + type error
```
</div>

---
clicks: 3
---
# Bonus

<h4 style="display:inline"> Pre built UI <span style="display:inline"> - respect platform standards</span></h4>
<div v-if="$slidev.nav.clicks===1">
<br>
<img  src="images/ios.png" style="width: 50%;margin:auto">
<h4 style="text-align: center">  Design for all platforms: web, desktop & mobile </h4>
</div>
<div v-click=2>

#### Keep your dependencies lean
</div>
<div v-click=3>
<h4 style="display:inline"> i18n? use icons: <span style="dispaly: inline">👋 username </span></h4>
</div>

---

<tweet id=1534914416050855936 /> 

---

<div style="display:flex;flex-direction: column; align-items: center">
<br>
<br>
<br>

# Thanks for your time!
<br>

#### Make cool things to inspire cooler things
<!-- #### Learn stupid things to build stupidder things -->
<br>

<logos-twitter /> <a href="https://twitter.com/ekaansh" target=_blank>@ekaansh</a>

</div>

---

# Refereces

- [Agora Web UIKit](https://github.com/AgoraIO-Community/Web-React-UIKit/)
- [Gartner Report](https://cyclr.com/blog/low-code-is-revolutionising-the-software-industry#:~:text=With%20Gartner%20suggesting%20that%20%E2%80%9Cby,such%20as%20citizen%20developers%2Fintegrators.)
- [Swyx Twitter](https://twitter.com/swyx)
- [cdk8s](https://cdk8s.io/)
- [Swift Docs](https://swift.org/documentation/api-design-guidelines/)
- [xkcd comic](https://xkcd.com/)
- [Giphy gif](https://giphy.com/)

<!-- 
## Framework specific design

```go
package main
import ("fmt")
func main() {
  fmt.Print("hi mom")
}
```

```ts
console.log('hi mom')
```-->
