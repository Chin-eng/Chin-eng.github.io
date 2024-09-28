---
layout: single
sidebar: default
title: "CSE 421: Introduction to Algorithms"
toc: true 
quarter: FALL
year: 2024
description: Techniques for design of efficient algorithms. Methods for showing lower bounds on computational complexity.
---


### Week 1
## Lecture 1: Intro, Stable Matching (Sep 25th, Wednesday)

We discussed about course syllabus and introductions to the class in the first 25 minutes. Then we proceeded to talk about Stable and Unstable Matching. Stable Matching is defined as no pair of people both prefer to be each other rather than their assigned partner. Unstable Matching is defined as assignment with no unstable pairs. 

Example: Matching Medical Residents to Hospitals: Design self reinforcing admission process between hospitals and students given the preferences

For a matching M, an unmatched pair from a different groups p → r is unstable if p prefers r and r prefers p. (the point is they could ignore the official assignment and go to their desired preferences)

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/cse421/week1/stableMatch1.png" alt="" class="full">

No, because if we pair (X, C) and (Z, A), A’s first preference is Y but Y is already paired with B (Y, B) (since Y’s first preference is B). Thus, when we try to pair Z to A, A’s second preference is X so I would prefer X over Z, which makes the pairs unstable because Z prefers to be with A and X prefers to be with C. 

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/cse421/week1/stableMatch2.png" alt="" class="full">
Yes, because X’s first choice is A, and A’s first choice is Y but Y’s first choice is B so we have a match (X, A). The same is true for (Y, B) since Y’s first choice is B and B’s first choice is X but X’s first choice is X. Also, we have a pair (Z, C) since C’s first choice is X and second choice is Y but X and Y do not prefer C as their first choice. Thus, since no pairs prefer to be with other pairs, we have a stable match. 

Then we talked about Propose and Reject Algorithm, which guarantees to find a stable matching. Members of one group P makes proposals, the other group receives proposals. 

Members of one group P makes proposals, the other group R receives proposals

Then we talked about Propose and Reject Algorithm, which guarantees to find a stable matching. Members of one group P makes proposals, the other group receives proposals. 

Members of one group P makes proposals, the other group R receives proposals

Proof of correctness: Termination: The Gale-Shapely algorithm terminates after n^2 iterations

Proof of correctness: Perfection: Once a member R is matched, they never become free, so they only trade up. So, everyone gets matched

Proof of correctness: Stability: No unstable pairs in the final Gale-Shapley matching M. 

Gale-Shapley guarantees to find a stable match

## Section 1: Stable Matching, Induction Review (Sep 26, Thursday)

<!-- <img src="{{ site.url }}{{ site.baseurl }}/assets/images/cse421/week1/section1.png" alt="" class="full"> -->
 We discussed stable and unstable matches as well as Gale-Shapely algorithm, and walked through few section problems. 

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/cse421/week1/section1.png" alt="" class="full">

## Lecture 2: Stable Matching, Overview (Sep 27, Friday)

The lecture started with homework 1 introduction, Ed Stem discussion, and office hours starting today, as well as some review with stable matching problems from lecture 1 and Gale Shapley algorithm. Gale Shapley guarantees to find a stable matching. However, this algorithm is very useful in for the proposal side but it is not that great for the receiver side. We proved proposer optimal and receiver pessimality through proof by contradiction during lecture.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/cse421/week1/lecture2.png" alt="" class="full">

### Week 2
