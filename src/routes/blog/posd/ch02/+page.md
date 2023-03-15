<a href='/blog/posd'>Back</a>

In this series, I am going through the book "A Philosophy of Software Design" by John Ousterhout. I will summarize what I consider to be important and try to apply it to different areas of my own experience.

# Chapter 2
## Complexity Defined
Laying the groundwork before talking about concrete strategies. What is complexity and why is it the most important aspect of programming to work on?

### What is Complexity?
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

I worked as a solo developer for the last 4+ years. It has been nice to start reading through this as I have caused a lot of these problems myself!

* Creating dependencies: This comes out of laziness as well as under-estimating change amplification and cognitive load. If I'm the main (or only!) developer touching the code base, it is relatively easy to keep a lot of important things sorted out in my mind. This won't be true in a couple of months, of course! And worse, when someone else needs to work on a code base, the cognitive load required is unacceptable. Change amplification is similar--it is straightforward to just keep going down the same path, sticking to the same pattern, but this will have a bad effect overall.
* Creating obscurity: As a solo developer, this sneaks in just like problems with cognitive load. **I** have the requirements organized in my head, but that is not at all clear by looking at the code. At the very least, this should be documented in comments, but I have failed to do this more than I'd like to admit.
* Developer take-away: Even when I'm the only one (or feel like I'm the only one) working through a problem, I should *always* code as if someone will take everything over tomorrow.

## Complexity in other fields
Expanding upon this, I found it pretty easy to find parallels in other aspects of my life.
### Music Making
Making music--and in particular, mixing music--is the process of taking many different streams of audio and combining them into (usually) two streams: Left and Right. This is simple addition. It doesn't always feel like that when I'm staring at a screen full of tracks in my DAW. It is arguably impossible to remove change amplification from this process. If I change the sound of one instrument, I inherently change the final, mixed-down waveform of all the instruments.

If I put all of my eggs into one basket (say, the vocals) early on, I can make the singers voice sound *perfect*! But wait, as soon as I start changing the drums, the bass guitar, and the rhythm guitar, I've affected how the voice interacts with everything else. I went in so deep, that as soon as I change a little bit of the snare drum, I have to go back and fix the vocals again.

Mixing is kind of like a game of tug-of-war. You change one thing, everything else changes, too. I don't think there is a right answer, just like there isn't in programming.

There are two methods that come immediately to mind, though:
1. Don't go too deep too soon. Slowly mold the audio little by little and always keeping the big picture in mind. A lot of really good mix engineers *refuse* to mix solo'd tracks (i.e. only one track at a time). Instead, they keep the whole sound in mind as they adjust a single instrument.
2. Make big changes and don't go back on them! Walk forward in one direction and don't let change amplification get in the way. There is something to be said for a bold method like this, too.