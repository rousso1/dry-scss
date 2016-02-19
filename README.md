# Easily write concise, DRY, maintainable and scalable SCSS code in a large repo. — Edit
# *WORK IN PROGRESS*

---

Table of contents:
  * [Motivation](#motivation)
  * [The main problems with CSS at scale](#the-main-problems-with-css-at-scale)
  * [The Solution](#the-solution)
  * [A comparison table to other css solutions](#popular-existing-solutions)
  * [Conclusion](#conclusion)

---

## Motivation
CSS (and SCSS) tends to get messy. 
In a small project with just a few contributors, one can probably just read through the whole css code, hack in desired changes, and chances are not much will break. It doesn't matter if the css is ugly - as long as it just works. A glimpse at the output in the browser will tell you if things are working.
<br>
A large scale front-end project, with dozens of contributors, thousands of files, components, abstractions and a huge number of possible UI states - requires a different strategy. In this case, the CSS code should be readable and easy for refactoring. And in many cases the person who is about to make changes is not the person who originally wrote the code.
<br>

---

## The main problems with CSS at scale 
   * CSS is all at the global namespace (just like javascript)
   * Refactoring is complex; Hard to eliminate dead code (unreachable selectors)
   * Hard to know the visual output just by looking at the code.
   * Bloated stylesheets may lead to performance problems.
   * Its hard to write scoped CSS.
   
--- 

## The Solution
1. The architecture of scss in your project
2. 7 Guidelines to rule them all
3. root-selectors-helpers.scss library to enhance expression ability
4. A well configured SCSS linter.
5. A grunt task to enforce namespacing.

---

## Popular Existing Solutions
  * BEM
  * OOCSS
  * SMACSS
  * SUITCSS
  * Atomic
  * Css Modules - extra precompiling needed, can't integrate into existing project
  
Main problems:
* Hard to integrate into an existing project which grew over time, expenssive refactors needed
* Templating system not be compatible with modules naming systems
* Extra syntax is introduced, need to learn and teach developers new stuff
* integrate 3rd-party css? forget it
* Extra semantics which intend to put things into order, are forigen to the project, and nobody cares about it when they dont last as the project grow


---

## Conclusion


