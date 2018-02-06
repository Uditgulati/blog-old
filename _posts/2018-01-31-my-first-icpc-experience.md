---
layout: post
title:  "My first ICPC experience"
date:   2018-01-31
---

<p class="intro"><span class="dropcap">A</span>CM-ICPC has been a goal for me since the starting days of my Competitive Programming journey. It's a contest where the bests of bests compete against each other, so the competition is really tough(actually, not so tough :P).</p>

<p class="intro">My ICPC team name is "RootNodes" and team mates are Anurag Bansal and Amit Yadav, two of the finest coders of our college. It was the first time a team was applying from IIIT Una, so we were quite excited. We formed our team during the end of our first year but named it just a couple of weeks before registration.</p>

<p class="intro">During the initial period of our second year, we practiced a few common topics and took suggestions from our seniors who had participated in previous ICPC. Those tips were quite helpful in improving our team co-ordination.</p>

<p class="intro">We registered for 2 regionals, namely, Kolkata and Kharagpur. We wanted to go to Kolkata but also registered for Kharagpur just in case if we are unable to qualify for Kolkata.</p>

## Online Round

The online round was on 5th of November which was also the 3rd and last day of our annual cultural fest, Hill'ffair. When I first came to know that online round was on a day of hill'ffair, I was like "What the hell, I'll have to code even on the day of cultural fest :(". But, after the online round, I was ok with that as hill'ffair performances weren't as good on the last day as the previous 2 days and we already had DJ night and band performances, so that part was fulfilled. 

When the online round started, I took the first problem which wasn't an easy one but seemed to be. I thought for a while and thought of a solution and coded the solution and was ready to submit but then I properly saw the constraints and came to realise that my solution would give TLE. By that time, Amit had solved an easy problem. Then, we took an easy math problem which had precision issues. I made the solution but wasn't sure about the correctness of precision. I submitted and it gave WA. I realised that I had missed a case. I re-submitted and it again gave WA. This time I thought that there was some overflow. I made some tweaks and submitted again and again but it was no good. I then changed my code such that there was no requirement of ``long long``. It got accepted this time. I was relieved. Then came a notification that there were some issues with testing of solutions and are being re-judged. After some time it was shown that only my first solution was wrong and all other were accepted. I was like "Why?? Why me??". Codechef already had a history of fucking the online round. History repeated itself, but the main dish was about to be served.

Then we searched for the third problem and realised that there is another math problem which wasn't easy and Amit and Anurag spent the rest of contest time finding a solution but could only solve it halfway. Meanwhile, I again took the "Seemingly easy but not easy" problem and realised that there is an important observation which made the problem solvable and I coded the solution and submitted it. It got accepted. I was on cloud 9. Now, with very little time remaining, we thought of finding solution to that math problem but couldn't.

The contest ended and we were at nearly 400 position out of more than 3000 teams with 3 out of 5 problems solved. We were happy with our performance. We were sure to be qualified for onsite round. After the contest, someone at the discussion page said that someone had asked the problems on **mathexchange** and that page was shared with many participants which gave them an unfair advantage. The main dish was served.

After a couple of weeks, result came out and we qualified for both the regionals. We were delighted. As we had already discussed that we'll only go to one regional as it was our first time and budget was low too, we decided to go with kolkata.

## Onsite Round

Just few weeks after online round, we had our exams, so we didn't practice much during that time. After the exams were over, we tried a few mirror rounds of some ICPC regionals on codeforces. We also had to complete the reference notes for the regional, so most of the time was spent finding good implementations and editing them and adding them to the repo. There were a few codeforces round before the regional. I participated in all of them and did well in some and not so well in others.

Finally came the day when we had to depart for kolkata. We took our flight from Delhi to Kolkata. We reached Kolkata a day before the contest, so we spent that day exploring Kolkata. The day was spent well. The next day we reached the GNIT campus where the contest was to be held. We registered our team and were provided with some goodies which included--

*	A red kolkata regional t-shirt.
*	A black Codechef t-shirt.
*	A notepad.
*	Some stickers from Codechef.

Next up was the photo session by codechef. They took pictures of each team and also a boomarang to be upoaded on their instagram profile. Here's us smiling like idiots :P.

<img src="{{ '/assets/img/team.jpg' | prepend: site.baseurl }}" alt=""> 

There was practice round a day before the actual contest which was of an hour and was just to get students aquainted with the programming environment and correct any login related issues. As the practice round was going on, there was an invigilator roaming around in back sweater. He looked familiar and later I realised that he looks just like triveni. And after the contest, I came to know that he actually was him and he had set the problems. When I started doing CP, I used to read his blogs and was fascinated by his skills in CP. Seeing him in person was really a great experience.

Then came the D-Day. We woke up a couple of hours before contest and had our breakfast. The contest started at 10 AM. We were at our computer half an hour before the start of contest. The lab we were in had nearly 7-8 other teams. I could recognise a couple of faces as I had stalked a lot of profiles of Codechef :P. Also, one guy from the team sitting just in front of us was a div 1 coder on codeforces and guess what, I had also stalked his profile many times.

So, the contest started and we were presented with 11 problems on the codechef site. There was also a hard copy of problems. We quickly searched for the easy problems and found a couple of them. Our strategy was not to make any silly mistakes in easy problems as that could through us down in the ranklist. So, what we did was that 2 guys will solve same problem independently and if their solution is same, then we'll assume it to be correct. So, following this approach, we solved the first 3 problems with ease. Next up was a sorting problem with some observation which luckily I cracked quickly. We now had 4 problems solved within an hour. So far, we were doing great. We then analyzed the leaderboard and realised that next problem was a geometry problem. 

So, the fifth problem was a 3D-geometry problem. We realised that if we are able to solve it, we will definitely end up at a good rank. So, all 3 of us were trying our best to recall all the possible plane and line related stuff from class 12th. We penned down the plane and line equations, but those weren't of any use. I then realised that the problem could be solved using vector algebra. I with Anurag recollected stuff like dot product and cross product. We then coded a solution and that somehow gave correct output for sample cases. I submitted it and it gave WA. By that time, 3 hours of contest had passed and only 2 hours were left. I don't know how time flew away while solving that 5th problem. So, now we had one WA on the problem. I thought that it is some precision error. So, I thought of using ``long double`` instead of ``double``, but that didn't work out as we didn't know the format directive for ``long double``. We then switched to python, but that also gave WA. I then had a look at submission history of the problem and saw that all solutions were in C++. So, it wasn't a precision fault, the fault was in the approach which I found after analysing the approach deeply. I fixed it somehow and prayed for this solution to get accepted. So, we submitted it in Python and it got Accepted. Finally, fifth problem was done. After the contest, I saw that we were the only to solve that problem in Pyhton :P.

After 5th problem was done, only half an hour was left. Next problem was a DP which wasn't possibly solvable in remaining time. So, we shifted to another problem which was a very good problem. After thinking for a while, I came up with an approch making using of binary search. We could have started implementing it but the time was up.

The contest was over and it was time for prize distribution after Lunch. IIT Delhi came first and IIT Patna runner up. We were ranked 25th out of 168 teams, which in my opinion was great for first time participation. After that was a speech by Anup Kalbalia(head of Codechef). He is a good speaker but he only talked about how Codechef is helping improve the coding culture in India. Meanwhile, Me and Anurag were watching El Clasico. Anup's speech just started after the end of 1st half. So, we shifted our focus from the match to him. Funny thing was that match was going 0-0 during 1st half and ended at 3-0 after 2nd half with Barca winning. That day I left no chance to spite my "Real fan" friend :P.

Lastly was problem discussion and triveni was the one explaining solutions. He explained the first 5 problems and aproach was exactly same as ours. After that, he explained the DP problem which went all over my head. Then, he explained that binary search problem and my approach was nearly same as mine. Just that if I had one more hour, I would have solved that one too.

Next, we had dinner and then spent the night at park street as it was Christmas and that place was filled with people. That night was well spent. The next day we took flight back to Delhi.

To conclude, the contest went far better than what I expected and our perfomance was very good for first time participation. We'll be hoping to get an even better rank next time and hopefully **World Final** ;).

To view the ranklist or problemset, visit this [link](http://icpckolkata.in/).