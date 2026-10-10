# google coding interview questions: What Google Really Asks, the Patterns Behind the Questions, and How to Prep in 6 Weeks

Google's coding interview has a reputation problem. Candidates hear "2,000+ questions in the pool" and conclude the only rational response is to grind until their hands cramp. Then they show up, get a problem they've never seen, and freeze.

The pool *is* big. But the questions inside it aren't as random as they look. Recent candidate write-ups from Google loops keep landing on the same handful of underlying techniques, and the screening round is narrower than most people assume. If you understand the shapes, the specific problems stop mattering so much.

Here's what Google actually asks, what recent candidates report getting, and where a pattern-based study plan fits.

## What Google's coding rounds actually test

Two different things get tested at two different stages, and conflating them is why people over-prepare in the wrong direction.

### The screening round is narrower than the onsite

A Google software engineer based in Hyderabad, Anu Sharma, posted a breakdown of what she says shows up in the screening round — and noted she was rejected at that stage twice, since most eliminations happen there [8]. Her list:

- **Arrays** — sliding window, two pointers, binary search, sorting, greedy
- **Strings** — palindromes, pattern matching
- **Stacks and queues** — next greater/smaller element, BFS, flood fill
- **Recursion and backtracking** — permutations and combinations, which she flags as very important

She also said to skip segment trees and tries for this round, because they rarely appear, and to spend that time on time/space complexity instead. That's a useful signal: the phone screen rewards fluency on core patterns, not exotic data structures.

### The onsite pool is much larger

Once you reach the onsite, the surface area expands. A question-repository comparison put Google's documented question pool at roughly 2,217 problems, split across 588 easy, 1,153 medium, and 476 hard [7]. Two things follow from that distribution:

1. Mediums dominate. Most of your prep time should go there.
2. There's a real hard tail — and hard problems in a Google onsite are usually a medium pattern with an ugly constraint bolted on.

That same comparison flags **dynamic programming** as the topic where Google diverges most from other big tech companies [7]. Arrays, strings, and hash tables are table stakes everywhere; DP is where Google's question set gets distinctive.

## Real Google coding interview questions from recent candidate reports

Rather than theorize, here's a sample of problems candidates have publicly reported being asked, pulled from interview write-ups. Notice how few of them require knowing something obscure.

**From a 2025 Google new-grad loop in India** [1]:
- Find the inorder predecessor and successor in a BST, with a follow-up of doing it without extra memory
- Return the largest subarray that forms a special arithmetic sequence
- Graph problem: Alice and Bob in two cities want to meet and cab-share to a destination — return minimum travel cost
- Given a file of IP addresses with locations, answer location queries for a list of IPs

**From a Google L3 loop** [2]:
- Given a graph of cities with travel times, find the smallest time to reach any city from a list of favorites (Dijkstra), with a follow-up requiring the shortest path from S to T that passes through at least one favorite city
- Given movies connected by shared genre and a rating per movie, return the K most highly rated movies related to movie A
- Given pairs of strings that differ by exactly one character, form chains and return the length of the longest one

**From another L3 onsite write-up** [4]:
- Build a double-ended queue — push/pop front and back, size, print — using only a map, with O(1) for everything except printing
- Sort houses by number within neighborhoods, with a constraint that a neighborhood can't contain the same house number twice
- Find words in a dictionary that can be formed by deleting characters from a given string, preserving order

**From a larger set of Google-marked questions** [3][5][6]:
- Find the top-K most active chat users from a message log, better than sorting all users
- Count paths in an m×n grid with only right/right-up/right-down moves, then reduce space from O(m·n) to O(m)
- Minimum cars needed to serve a list of rental bookings (interval scheduling)
- Decode a nested encoded string like `3[a2[c]]`
- Max profit on a 1D array where taking index `i` earns `arr[i]` and jumps you to `i + 1 + arr[i]`
- Count connected land components in a grid (number of islands)
- Move tokens exactly +3 cells to collect the maximum number of coins — which decomposes by index mod 3

Read that list again. Merge intervals. Dijkstra. Top-K with a heap. BFS on a graph. DP with state. String parsing with a stack. Every single one maps onto a pattern you could learn once and reuse.

That's the actual insight, and it's the one a "solve 500 random problems" plan buries under volume.

## The problem with memorizing questions

You cannot memorize 2,217 problems. Even if you could, Google's interviewers regularly extend the question once you've written your first solution — "without using extra memory," "now assume multiple queries," "what if the input doesn't fit in memory." In the L3 write-up above, the second round pivoted from a straightforward BFS-with-heap solution to a discussion of quickselect. In another, the interviewer asked how to preprocess the dictionary when the word list is known in advance [4].

Memorized solutions collapse the moment the constraint changes. Recognized patterns adapt, because you're not recalling an answer — you're identifying which tool applies and then writing it.

The failure mode that kills prepared candidates isn't usually "couldn't code it." It's burning 15 of 45 minutes trying two approaches that were never going to fit. Pattern recognition is what compresses that to two minutes.

## Where AlgoMonster fits into Google prep

AlgoMonster (algo.monster) was built by ex-Google engineers and competitive programmers around exactly this premise: instead of shipping solutions to individual problems, it teaches the ~48 coding patterns that generate them, with code templates you adapt rather than code you memorize.

For Google prep specifically, a few pieces matter more than the rest.

**The decision flowchart.** AlgoMonster's headline tool walks you from a problem description through decision nodes — is the input sorted? are you looking for a contiguous subarray? is it a tree or a graph? — until you land on the algorithm you need. The site is explicit that you shouldn't memorize it; you use it as a reference until pattern recognition becomes automatic. For the "I don't know where to start" problem that eats interview minutes, that's the relevant training.

**Templates.** Sorting, binary search, BFS/DFS on trees and graphs, monotonic stack, fixed and flexible sliding window, topological sort, backtracking — each written out so you're not reconstructing boilerplate under time pressure. The pattern is the thinking; the template is the typing.

**Speedrun.** Once you know the patterns, Speedrun lets you move through problems quickly rather than writing full code for each. If you have three weeks left and coverage is your gap, this is the mode to live in.

**Company-specific question material.** AlgoMonster includes real questions attributed to top tech companies, refreshed monthly, per its subscribe page. Treat any company-tagged bank as a starting point rather than a guaranteed-questions list — nobody outside Google has the actual current question set.

**AI assistance.** You can select any text on the platform and have it explained, or use it to debug your code in the inline IDE. Multi-language support covers Python, Java, JavaScript, C++, Go, and others.

The curriculum is text-and-diagram based with no video. That's a deliberate choice, and it cuts both ways — there's nothing to passively watch, and nothing to rewatch either.

## AlgoMonster pricing: every plan, in one table

AlgoMonster's pricing moves around because sales are frequent. The official subscribe page currently lists these options:

| Plan | What you get | Price | Billing cycle | Get it |
| --- | --- | --- | --- | --- |
| **Free** | Limited access to a subset of patterns and problems — enough to test whether the text-and-diagram format works for you | $0 | — | [Start with the free tier](https://algo.monster?fpr=li69) |
| **Pro — Monthly** | All patterns, lessons and problems; unlimited AI assistant; unlimited Speedrun; company-tagged questions; member discount on live bootcamps | $18.99/mo ($0.64/day) | Monthly, cancel anytime | [Compare the monthly plan](https://algo.monster?fpr=li69) |
| **Pro — Yearly** | Everything in Pro, 12 months of full access, billed annually | $99/year (~$8.25/mo, $0.28/day) — list price shown as $198 | Annual | [Check the current yearly price](https://algo.monster?fpr=li69) |
| **Pro — Lifetime** | Everything in Annual plus lifetime updates on all current and future content, one payment | $189 billed once — list price shown as $378 | One-time | [See the lifetime deal](https://algo.monster?fpr=li69) |

A note on accuracy: third-party reviews floating around say AlgoMonster has no monthly option at all, and some quote a lifetime price in the $450+ range. Those numbers don't match what the official subscribe page currently displays. Promotional pricing is common enough that the only figure you should trust is the one on the checkout page at the moment you buy — 👉 [open the subscribe page](https://algo.monster?fpr=li69) and read the number there rather than planning around a screenshot from a review.

One more thing worth mentioning because it's easy to miss: a Pro subscription also unlocks AlgoMonster's other courses at no extra cost, including CS fundamentals, System Design, an AI coding interview course, and a "build an LLM from scratch" course. The site says new courses get added to the existing subscription rather than sold separately.

## Which plan actually makes sense

The math depends on how many Google attempts you expect to make.

**If your loop is in the next two months:** Pro Yearly is the straightforward pick. At ~$99 for a year, you're paying roughly what LeetCode Premium costs for eight months, and you get a curriculum with a defined endpoint instead of a 3,000-problem open world.

**If you're planning to interview repeatedly:** Pro Lifetime at $189 breaks even against two years of yearly renewals. Engineers who change jobs every two to three years and re-prep each time are the profile this is built for. One payment and you stop thinking about it.

**If you're not sure the format works for you:** use the free tier first. Text and diagrams, no video. Some people read faster than they watch. Others bounce off it hard. That's a personal thing you can settle in an afternoon, and it's cheaper than discovering it after paying.

**If you need one specific pattern fixed:** the monthly plan at $18.99 covers a single focused push. It's the most expensive way to buy a year of access and the cheapest way to buy six weeks.

## What AlgoMonster won't do for you

Google's loop has rounds AlgoMonster doesn't seriously cover, and pretending otherwise sets you up badly.

**System design.** There's some system design content included, but it's introductory. Target L5 or above and you'll need a dedicated resource — expect 20–40 hours of separate prep on distributed systems, consistency models, and scaling tradeoffs.

**Behavioral and Googlyness.** AlgoMonster includes light behavioral material. Google's Googlyness round is its own skill, and candidates report it varying wildly depending on interviewer — one write-up described a friendly discussion, another called it "a quiz with pre-meditated questions" [1].

**Live interview pressure.** Every problem is solved at your own pace with nobody watching. The follow-up questions are where strong-looking candidates still fall apart. Practice talking through your reasoning out loud, to a person, on a timer. Mock interviews with a real human are the only real fix here.

**Problem volume.** AlgoMonster's bank is far smaller than LeetCode's. Its bet is that pattern recognition plus a curated set beats raw volume. For most candidates that's true for *learning*; it's not a substitute for *speed practice*. The common advice in review threads is to learn the patterns on AlgoMonster and then build volume on LeetCode — the two solve different problems.

## A realistic six-week plan for a Google loop

Week 1–2: work through the flowchart and the core pattern categories — two pointers, sliding window, binary search, hashing, stacks. One pattern per session, then two or three practice problems for each. Write out the template from memory before you look at it.

Week 3–4: trees, graphs, BFS/DFS, topological sort, heaps, interval problems. This is where the bulk of Google's medium pool lives. Start using Speedrun on patterns you've already covered to protect the earlier material from decay.

Week 5: dynamic programming, seriously. Memoization, then iteration, then space optimization — the grid-path question above is a good template for that progression. Google leans on DP harder than most companies [7].

Week 6: mixed practice under time pressure. 45-minute sessions, unfamiliar problems, narrating your approach out loud. Then review the decision flowchart and your templates rather than learning anything new. Add two or three mock interviews with a real person if you can arrange them.

Time budget: 1–2 hours a day for the pattern work, more in week 6. That's the window AlgoMonster's curriculum is designed around, and it's also roughly how long a dedicated Google prep push takes most people.

## The short version

Google's coding questions look infinite and behave the same way about forty times over. Arrays with two pointers or a sliding window. Graphs with Dijkstra or BFS. Heaps for top-K. DP with a state you have to define carefully. String parsing with a stack. Interval scheduling with a sort.

Learn the shapes and the follow-up questions stop being ambushes. If you want a structured version of that with templates, a decision flowchart, and company-tagged questions, 👉 [start with AlgoMonster's free tier](https://algo.monster?fpr=li69) and see whether the reading-based format suits you. If it does, the 👉 [yearly plan](https://algo.monster?fpr=li69) covers a normal job-search cycle, and the 👉 [lifetime plan](https://algo.monster?fpr=li69) covers the next several. If you're on a tighter deadline, the 👉 [monthly option](https://algo.monster?fpr=li69) is enough for one focused push.

Then go find a human to interview you. That part no platform does for you.
