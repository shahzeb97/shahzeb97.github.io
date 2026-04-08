---
draft:
date: '2026-01-26T17:10:45-08:00'
title: 'Evaluating of the Air Canada Chessbot'
description: "Somehow even I could beat it"
summary: "A series of games I played on a flight and some commentary"
ArticleQuote: "I need a calculator - Bender B. Rodriguez"
tags: ["personal"]
categories: ["personal"]
author: "Shahzeb Mirza"
card:
  image: "ac.jpg"

showToc: true
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
---

> I need a calculator. (You are a calculator). A better one!

-Bender B. Rodriguez

{{< youtube jMG1D8XeLDA >}}

TODO: Add colours to this post


## Context

I'm on AC flight UA8433, Jan 13th, from YYZ to SFO. I have 5 hours and 49 minutes to kill. The flight departs at 6:50 PM - I am wide awake. There is a touch screen in front of me and none of the movies or shows appeal to me. I see a games section. There is a chess game. You can play with other passengers or - insteresting - with the machine.

## Setup

I wonder a few things:
* How much compute does an aeroplane have? This seems like a modern one. 
* Does every display have its own CPU inside or is there a central cluster?
* It doesn't matter either way, a 2005 nokia phone could beat me right?
* What algorithm do they use? Is it [Stockfish](https://stockfishchess.org/)?
* There are three difficulty settings, I wonder how they set this?
* The [Delta Chessbot](https://www.youtube.com/watch?v=fyCn81PVbWE) is supposedly really hard to beat.
* I wonder if modern chess engines need less compute or more? What does that pareto front of cost vs performance look like?

I should just play this thing. 

I don't think I can beat it, I should just try and get it to compete with Stockfish on my phone, through the [Lichess](https://lichess.org/) app (thank you local compute, I don't have wifi).

I can use the bisection method to see which Stockfish level the AC chessbot is equivalent to. Stockfish has 8 levels on my phone. I should start with level 4. If AC wins, go to 6, if it loses, go to 2. Continue in this way until I find the nearest level.

I'll have it play both black and white sides to have it be fair (at high levels this matters).

I'm ready for a battle of champions.

## Starting the Games

### AC (Hard) vs Stockfish (Level 4)
*AC Black, Stockfish White*
1. d4 Nc6 2. d5 Ne5 3. Nc3 Nf6 4. f4 Ng6 5. f5 Ne5 6. Nf3 Nc4 7. Qd3 Nb6 8. Bf4 Nbxd5 9. Nxd5 c6 10. Nc7+ Qxc7 11. Bxc7 Nd5 12. Bg3 Nb4 13. Qd2 Nxa2 14. Rxa2 d5 15. Nh4 g6 16. Qf4 gxf5 17. Bf2 e6 18. Bd4 f6 19. Bxf6 Rg8 20. Qc7 h6 21. Kf2 Bc5+ 22. e3 Bb6 23. Qe7# 1-0

*Stockfish wins*

*AC White, Stockfish Black*
1. d4 e6 2. e4 a6 3. Nf3 b5 4. Bg5 Be7 5. Be3 d6 6. Nc3 Nf6 7. e5 Ng4 8. Bf4 b4 9. Ne4 dxe5 10. Nxe5 Nf6 11. Nc5 O-O 12. f3 Nh5 13. Be3 Nf6 14. Bd3 a5 15. c4 bxc3 16. bxc3 h6 17. a4 Nd5 18. Bf2 Bxc5 19. dxc5 Qg5 20. Bd4 Qxg2 21. Rg1 Qb2 22. Nc4 Qxh2 23. Be5 Qxg1+ 24. Bf1 Ba6 25. Bd4 Qg6 26. Ne5 Qg3+ 27. Kd2 Qg5+ 28. Ke1 Ne3 29. Bxa6 Nxd1 30. Rxd1 Rxa6 31. Rd3 g6 32. c4 Rd8 33. c6 Qf4 34. c5 Qxd4 35. Rxd4 Rxd4 36. f4 h5 37. Nf3 Rb4 38. Ne5 Rxf4 39. Nd3 Rg4 40. Ne5 Re4+ 41. Kd1 Rxe5 42. Kc1 Rxc5+ 43. Kd1 Nxc6 44. Ke1 Rc4 45. Kd1 Rxa4 46. Ke1 f6 47. Kd1 g5 48. Ke1 e5 49. Kd1 h4 50. Ke1 h3 51. Kd1 h2 52. Ke1 Ra2 53. Kd1 h1=R# 0-1

*Stockfish wins*

> Wow, not a great showing. Maybe AC is taking it easy on the fliers.

### AC (Hard) vs Stockfish (Level 2)
*AC Black, Stockfish White*
1. e4 e5 2. d4 exd4 3. Ne2 Nf6 4. Bg5 h6 5. Bh4 g5 6. e5 gxh4 7. a4 Nd5 8. e6 dxe6 9. Ra3 Bd6 10. Qxd4 Nc6 11. Qxh8+ Bf8 12. Rf3 f5 13. Nec3 Nde7 14. Rf4 Ng6 15. Qh7 Nxf4 16. g3 Nh5 17. Nb5 hxg3 18. Nxc7+ Qxc7 19. Qxc7 gxf2+ 20. Kxf2 Bc5+ 21. Ke1 Bb6 22. Qd6 Nf6 23. Ba6 Ne4 24. Qd3 Nc5 25. Qh3 Nxa6 26. Na3 Nc5 27. Nc4 Nxa4 28. b3 Nc5 29. Rg1 Bc7 30. Rg7 Bxh2 31. Qxh2 b5 32. Qxh6 Bb7 33. Nd6+ Kd8 34. Qh8# 1-0

*Stockfish wins*

*AC White, Stockfish Black*
1. d4 Nf6 2. e3 c6 3. Nf3 g6 4. Nc3 Qc7 5. Qd3 d5 6. Ne5 c5 7. Nb5 Qb6 8. Qc3 c4 9. a4 Ne4 10. Qa3 f6 11. Nf3 e5 12. b4 a6 13. a5 Qxb5 14. dxe5 Nc6 15. exf6 Nxf6 16. Nd4 Qxb4+ 17. c3 Qxa3 18. Bxa3 Ne7 19. Bc5 Nc6 20. Bxf8 Kxf8 21. Nxc6 bxc6 22. f4 Ng4 23. h3 Nh6 24. g4 Rb8 25. g5 Nf5 26. Bg2 Kf7 27. e4 Ne7 28. exd5 Nxd5 29. Ra3 Re8+ 30. Kd1 Kg8 31. h4 Bf5 32. Bf3 Rbd8 33. Rh2 Kf8 34. Rha2 Nxf4+ 35. Kc1 Nd3+ 36. Kd1 Nb2+ 37. Kc1 Re1+ 38. Kxb2 Rb1# 0-1

*Stockfish wins*

### AC (Hard) vs Stockfish (Level 1)
*AC Black, Stockfish White*
1. Nf3 Nc6 2. a3 d5 3. e3 Nf6 4. d4 Be6 5. Bb5 a6 6. Bd3 h5 7. O-O b5 8. Nbd2 Qc8 9. Ng5 Bg4 10. Qe1 e6 11. c3 Bd6 12. h3 Bd1 13. Qxd1 Rh6 14. e4 dxe4 15. Ndxe4 Be7 16. a4 Nd5 17. Nxf7 Rh7 18. Qf3 g6 19. Neg5 Rg7 20. Re1 Bf6 21. Qxd5 Ne7 22. Nd6+ cxd6 23. Qe4 d5 24. Qf3 Nf5 25. Bf4 Nh4 26. Qxd5 bxa4 27. b3 axb3 28. Qxb3 Rb7 29. Qa4+ Qd7 30. Rxe6+ Be7 31. Qc4 Rc8 32. Qxa6 Ra7 33. Rxe7+ Kxe7 34. Qxa7 Qxa7 35. Rxa7+ Ke8 36. Rc7 Ra8 37. g4 Kd8 38. Kh2 Ra2 39. Ne6+ Ke8 40. Bb5# 1-0

*Stockfish wins*

*AC White, Stockfish Black*
1. d4 Nf6 2. e3 c5 3. dxc5 Nc6 4. Nf3 e6 5. Nc3 Be7 6. Qd3 O-O 7. e4 Qc7 8. Nb5 Qa5+ 9. Bd2 Nb4 10. Qd4 Nxc2+ 11. Kd1 Qxb5 12. Kxc2 e5 13. Bxb5 exd4 14. Kd1 Nxe4 15. Be1 Nxc5 16. Nxd4 d6 17. b4 a6 18. Bc4 Na4 19. f4 Bf6 20. Bf2 Bd7 21. Ke1 Rac8 22. Bd5 Rfe8+ 23. Be3 Rxe3+ 24. Kd2 Nb6 25. Bxb7 Nc4+ 26. Kd1 Rce8 27. Bxa6 Rc3 28. Nb5 Bg4# 0-1

*Stockfish wins*

### AC (Hard) vs Stockfish (Level 8) - Slaughterhouse
*AC White, Stockfish Black*
1. d4 d5 2. e3 Nf6 3. Nf3 c5 4. dxc5 e6 5. Qd4 a5 6. Nc3 Nc6 7. Qd3 Bxc5 8. Na4 Ba7 9. Nc3 e5 10. Nb5 e4 11. Qd1 exf3 12. Qxf3 Bb8 13. Nc3 Bg4 14. Qxg4 Nxg4 15. Nxd5 Qxd5 16. c4 Qf5 17. h3 Bg3 18. fxg3 Qf2+ 19. Kd1 O-O-O+ 20. Bd2 Rxd2+ 21. Kc1 Rd1+ 22. Kxd1 Nxe3+ 23. Kc1 Qc2# 0-1

*AC Black, Stockfish White*
1. e4 e5 2. Nf3 Nc6 3. Bc4 Nf6 4. d3 d5 5. exd5 Nxd5 6. O-O Nb6 7. Bb5 a6 8. Bxc6+ bxc6 9. Bg5 f6 10. Nxe5 fxg5 11. Re1 Bb4 12. Qh5+ g6 13. Nxg6+ Bxe1 14. Ne5+ Ke7 15. Nxc6+ Kd7 16. Nxd8 Kxd8 17. Qxg5+ Ke8 18. Qe5+ Kd7 19. Qxh8 Bb7 20. Qxh7+ Ke8 21. Qxc7 Nd5 22. Qxb7 Rd8 23. Na3 Bxf2+ 24. Kxf2 Rd7 25. Qc8+ Rd8 26. Re1+ Ne7 27. Qe6 Ra8 28. Qxe7# 1-0

*Take a wild guess*

### AC (Hard) vs Shahzeb

I don't have the PGN (portable game notation) for this one, but I won. 

The game felt easy, AC felt scattered. 

People say that when bots play at an artifically low level, they don't play poorly the way humans do. The bots apparently lower their difficulty by playing optimal moves and then every once in a while playing a very suboptimal move. Something weird and chaotic that doesn't seem like it belongs.

Humans on the other hand have a method to their madness. You can see the attack strategy in a bad human player. There's an over arching *idea*, like "They won't be able to block my queen if I pin the knight like this" or "The king will be forced to go into this corridor". But the bad human player has clear blind spots - they forget about the bishop in the corner, or the knight which can threaten them in a way that throws off the whole plan. It is coherent but incorrect.

I would like to put the AC games into an analysis software to see what the overall trends were like. My theory is there were none at all.

## Overall Rating

Sad to say, a pretty boring chess bot. Not hard to beat, and not even fun to play. Maybe when Air Canada finally gets [Starlink](starlink.com), they can not worry about the compute costs and just link to Lichess, or some server on the ground. 

Lichess takes about $800K per year to run, how many flight attendents is that?