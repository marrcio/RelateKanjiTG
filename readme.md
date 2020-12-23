# What?
This is the Computer Engineering graduation thesis I submitted for [ITA](https://en.wikipedia.org/wiki/Instituto_Tecnol%C3%B3gico_de_Aeron%C3%A1utica), and proudly got full-marks for it :D

At its core, it describes the use of a graph ordering algorithm (page-rank with non-homogeneous restarts) applied on Japanese Kanji.

# Why?
It is interesting to look at Japanese Kanji as a graph, since its morphology is strongly connected and evident.

Take for example the Kanji for "time": 時. It is in fact formed by combining two other kanji: 日 (sun) and 寺 (Buddhist temple). Also, the right part "寺" can be divided again: in 土 (soil) and 寸 (measurement).

Another way to look at it is by the frequency of co-occurrence in words. For example, the word 学習 (study), connects these two Kanji with a strength proportional to the frequency it appears in the Japanese language.

# How?
Using all connections from either the morphological graph or the co-occurrences graph, we can model the following problem:

> A student is reading some Japanese media, and is faced with a kanji (e.g. 時), and will research it.
> In their study, they will research a bit the kanji and jump to its connections, and after some time 
> they will get bored and start reading again, until they find another interesting kanji to research.
> 
> After a long time of this navigation, how probable it is that the student will be in a certain Kanji X?

Pure page rank solves the problem without considering that each kanji has its own probability in the Japanese language. The proposed method with random restarts better models this student that is frequency biased by the frequency these kanji appear in the Japanese language.

# Useful?
Quite a lot of what's written was never put to practical use, but the ordering and the morphological graph is available at relatekanji.org.
