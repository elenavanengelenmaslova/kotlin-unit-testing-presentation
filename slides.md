---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: unhappyFlow.jpeg
# apply any windi css classes to the current slide
class: 'text-center'
canvasWidth: 800
# https://sli.dev/custom/highlighters.html
highlighter: prism
# show line numbers in code blocks
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ## Introduction to Unit testing
  For beginners

# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss
---

# Introduction to Kotlin Unit Testing 

Bite size Kotlin session 3

<div class="pt-12">
    Elena van Engelen - Maslova
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/elenavanengelenmaslova/kotlin-unit-testing-presentation" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
---

# Format

Elevate your software development process by learning and applying the principles of unit testing in Kotlin, while working on your F1 Simulator application project! 🏎️️🛠️


<v-clicks>

- 🔍 **Understanding Unit Testing** - Kick-off your journey by learning what unit testing is, its importance, and how it can revolutionize your development process.

- 🧪 **First-hand Testing Experience** - Let's start on the workshop where we set up, run and debug our first unit test.

- 📚 **Take-Home Assignments** -  Continue your exploration of Kotlin's fundamental building blocks with F1 app workshop step 8 to 12, while consolidating your understanding of unit testing by applying them to the tasks at hand.

</v-clicks>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: slide-left
---

# What is Unit Testing?

Unit testing is a type of software testing where individual units or components of a software are tested. The purpose is to validate that each unit of the software code performs as expected.

<v-clicks>

* **White Box Testing**: Unit tests are written with knowledge of how the code being tested works. 

* **Isolation**: Unit tests focus on a small, isolated piece of code (a 'unit'), such as a single class or function. 

* **Automated**: Unit tests are typically written to be run automatically. 

* **Part of Development**: Unit tests are usually written by the same developers who write the code. 

</v-clicks>

---
transition: slide-left
---

# Why is it Important?

<v-clicks>

 * **Catching bugs early**: Unit testing finds problems early in the development cycle, making them cheaper and easier to fix.

 * **Simplifying integration**: It helps ensure that individual parts are working correctly before they're combined with others.

 * **Facilitating change**: Well-tested components can be modified with confidence. They provide a safety net against potential bugs from new changes.
 
 * **Improving design**: Writing tests often leads to better code design, as it forces developers to consider how their code will be used and how it interacts with other parts.

</v-clicks>

---
layout: image-right
image: testingPyramid.webp
---

# Testing Pyramid

<v-clicks>

* **Unit Testing**: Tests individual functions or methods in isolation.

* **Integration Testing**: Tests the interaction between different components of the system.

* **End-to-End Testing**: Simulates real-world user interactions and tests the entire application from start to finish.

</v-clicks>


---
preload: false
---

# Basic Unit Test Structure

```kotlin {all|3-6|8-11|13-16|all}
internal class SomeClassTest {
  
  @BeforeEach
  fun `Set up SUT`(){
    // set up generic system under test...
  }

  @Test
  fun `Given ... When ... Then ...`() {
    // test implementation
  }

  @AfterEach
  fun `Tear down SUT`(){
    // clean up ...
  }
}
```

---
layout: end
---

# "To finish first, first you have to finish." - Stirling Moss
> Just like in F1, this emphasizes the importance of having functional,
> bug-free code. Just like a race car needs to complete the race to 
> have any chance of winning, your code needs to pass its tests to 
> ensure it functions as expected.