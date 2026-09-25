---
theme: refactoring
title: Refactoring Without Tools  TODO
kata: tennis
difficulty: 1
author: reasun
tags:  refactoring c
---

## Notizen von Peter

* refactoring with and without tools   * add precondition: identifying paragraphs
  * hat andere objectives
  * neu 2. connect: which tools?
  * concrete: ask which tools they have -> homework
  * motivation no tools
  * plug book
  * dann demo extract method manually (statt abfragen)
  * Conclusion: safe? (test nicht extra besprochen)

# Refactoring without tools  TODO

Do you know what tools you have available? You don't always have the ones you'd like to have, and they don't always work totally reliably. How do you handle that?

## Prerequisite

[Identify Paragraphs]({% link _learning_hours/refactoring/identify_paragraphs.md %})

## Learning Goals

* Learn how to refactor even when tools are not available or not working
* Know and apply the rule to be no more than 1-3 steps away from working code
* Get to know the IDE's refactoring tools

## Session Outline

* 5 min connect: what can go wrong?     TODO - longer?
* 10 min concept: Steps of Extract Function
* 30 min do: pairs refactor Tennis1
* 5 min reflect: what difference do fast, good tests make?

### Connect 1

Ask the group - What can go wrong when refactoring? How do you know if your refactoring was safe? Gather comments from the whole group and note them in a shared document or whiteboard.

This is a [Three Facts]({% link _activities/connect/three_facts.md %}) connect.

Hopefully people will know that refactoring can be dangerous and the compiler and tests can protect you from mistakes.

### Connect 2

Ask the group - What refactoring tools are you using? Collect comments from the whole group and put them into a shared document or whiteboard. Hopefully they know some of the tools available to them.

Next ask them to find out which tools their IDE supports. Let them write down the results in a shared document or whiteboard.

This is a [Web Hunt]({% link _activities/connect/webhunt.md %}) connect.

Hopefully people will realise that their IDE is much more powerful than they thought.

#### Homework

Ask each member of the group to pick a tool they don't use often enough (or haven't used before) and make an effort to use it more often in the coming week(s). If you have another session with them, ask them how it was going in the next session.

### Concept - Refactoring steps

Ask the group - Why would you want to refactor without tools?

Introduce them to the Golden Rule: Never be more than 1-3 steps away from working code. This means that you can undo your changes back to a working state in one to three steps, but also that you will reach a new, working state in one to three steps.

Reference Martin Fowler's Refactoring book to bring across the notion of proven step-by-step recipes for refactorings.

Demo an example refactoring, e.g. the steps to Extract Method (or Extract Function, depending on your language):

1. Copy the block of code into the clipboard (copy, not cut).
1. Create a new, empty void method with no arguments. Give it a nonsensical name like 'foo' or 'applesauce'.
1. Paste the code from the clipboard into that method.
1. Figure out what the return type should be and change the method to return it.
1. Figure out what the arguments should be and change the method to use them.
1. After having worked with the code, you should have an idea what the code does. Rename the method to reflect this.
1. Compile and test.
1. Replace the original paragraph with a call to the method.
1. Compile and test.

### Concrete

Work on a refactoring exercise that needs the refactoring you have demoed, for example Tennis. Have people use the steps you showed them earlier.

Choose an exercise that already has good, fast tests.

### Conclusions

Ask people to think about whether what they did was safe. How did it feel to have fast, reliable tests? Would you work differently if you didn't have them? How would using refactoring tools change your answers?
