In this series, I am going through the book "A Philosophy of Software Design" by John Ousterhout. I will summarize what I consider to be important and try to apply it to different areas of my own experience.

# Chapter 2
## Complexity Defined
Laying the groundwork before talking about concrete strategies. What is complexity and why is it the most important aspect of programming to work on?

Ousterhout defines complexity as "anything about the structure of a system that makes it hard to understand and modify."
* Hard to **understand**
* Hard to **modify**

### Causes and Symptoms
Ousterhout goes on to define the 3 symptoms and 2 causes of complexity in software.
#### Symptoms
1. "Change Amplification" (To make one change, many aspects must be modified)
2. "Cognitive Load" (A developer has to keep many things in mind to make a change successfully)
3. "Unknown Unknowns" (It is unclear what changes are necessary to fix a problem)
#### Causes
1. "Dependencies" (Changing one element requires changing many other elements in the code)
2. "Obscurity" (Areas that are important/necessary to change are not obvious)

