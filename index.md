# Tony's Learning Journal for Teaching Code
A dedicated journal for teaching programming and learning teaching fundamentals in general.

### Navigation
- Home
- [Breakdowns](breakdowns/index.md)
- [Gists](gists/index.md)

---

## June 9, 2023
### [Create Beautiful Presentations With Svelte](https://www.youtube.com/watch?v=67lqa5kTQkA)
    - [Companion article](https://joyofcode.xyz/beautiful-presentations-with-svelte)

No sample code, but the [companion article](https://joyofcode.xyz/beautiful-presentations-with-svelte) has an excellent breakdown of the project. In fact, I'm not even going to watch the video; hopefully the article is enough?

The project includes TailwindCSS. Normally, I don't like opinionated dependencies in tutorials, but a utility library is probably the best way to quickly style up something in RevealJS.

**Session Notes**
- `pnpm` isn't installed on this system. That's embarrassing. It took awhile to decide how to install but went with Brew.
- I stopped mid-session and I'm continuing on a machine that does not have `pnpm` installed. I'll probably continue using it in the future and found this [SO for changing switching versions](https://stackoverflow.com/questions/72132590/how-do-you-switch-between-pnpm-versions) which suggests installing using Node Corepack.
- Received a 404 error on @fontsource when running this command but it worked with I installed the fonts individually:
    ```bash
    pnpm i reveal.js @types/reveal.js @fontsource/manrop @fontsource/jetbrains-mono
    ```
- First try at blindly copy/pasting the code in the article created a lot of errors. Namely, `code.svelte` doesn't exist in his examples and there are multiple versions of `presentation.svelte` as the article continues. Going to start over from in initial install and walk through the vide and article side-by-side...
- Following the video was a much better idea. This is a great project that gives me everything I need (?) for my [Slides project](https://github.com/orgs/browsertherapy/projects/8)
- Most exciting is the ability to easily mix and match regular HTML and markdown slides. I can still pound out some quick md-only content and then go back and refactor it into more refined HTML using the fancy Reveal features.

**Next steps/questions:**
1. Create a dynamic `/slides` endpoint(s) for slide content
2. Figure out how to organize markdown imports vs HTML content
3. Is there a way to generalize content that can is slide vs article agnostic? For example, can I use the same content for my slides that can also feed a finished blog article?
4. How do I begin porting my existing content to the new system? Can I build a 5-slide series that can be inserted into a larger slide deck? Can one slide series feed multiple slide decks?
5. What's the best way to build common layout components like side-by-side comparisons (Good/Bad. Before/After, etc)?

---

## May 29, 2023
### New slide format?

![Code on the left, slide on the right](assets/images/journal/split-screen-presentation-theme.png)

_Source_: [How to make code more testable, by factoring out and abstracting side effects](https://www.youtube.com/watch?v=XVZpi7VJ_ws)

**Unicorn**: a markdown blog that is flexible enough for an educator to throw some code in one component and a relative slide url in another. The wrapper component places them side-by-side.

### Slide transitions using Svelte movement?
Could svelte be used as a replacement for slide transitions in ReavealJS?

**Slide 1**: File access module

![File access module shown](assets/images/journal/slide1-file-access-module.png)

**Slide 2**: Placeholder module

![Placeholder module shown](assets/images/journal/slide2-module-placeholder.png)

**Slide 3**: Trololo module

![Trololo module shown](assets/images/journal/slide3-trololo-module.png)

Possible to use Svelte transitions to handle differences in DOM-manipulation triggered by RevealJS?
- list item fades
- diagram (above) swapping
- entire slide swipes

### Further nerding
- [SvelteKit Page Transitions](https://joyofcode.xyz/sveltekit-page-transitions)
- An existing [slide presentation project](https://www.reddit.com/r/sveltejs/comments/sv2g2j/svelteslides_a_tool_to_generate_presentations/) from the beta days
    - Uses [Vizzu](https://vizzuhq.com/) for dat visualizations. Noice.
- Rich Harris demo of new [View Transition API implementation](https://www.youtube.com/watch?v=MJHO6FSioPI&t=1333s)
    - [Relevant SK pull request](https://github.com/sveltejs/kit/pull/9605)

---


## April 7th, 2023
Great reference from Rashid! He says this site was a game changer for learning the basics.
- [Mimo.org](https://mimo.org/)

---

## March 7, 2023
### Teaching Loops
Teaching loops is very difficult. I found this article by a 40+ year old junior insightful:
- [JavaScript The Early Lessons: For Vs forEach Vs For Of. Loops & Iteration, Which One Is Better?](https://medium.com/@trig79/javascript-the-early-lessons-for-vs-foreach-vs-for-of-loops-iteration-which-one-is-better-b557f385045)

He has almost convinced me to teach `for...of` instead of `forEach`. Almost. 

---

## January 12, 2023
### Exit Tickets!
- Breakdown: [Use exit tickets in your lessons - Everything you need to know](breakdowns/exit-tickets)

---

## December 10 , 2022
### Theo - ping.gg
- Top-shelf dev advice
- High-end topics
- Uses [Excalidraw](https://excalidraw.com/) as a drawing tool. Seems cool!
- **Great Breakdown of databases**
    - [Did I pick the right database?](https://www.youtube.com/watch?v=cC6HFd1zcbo)
- **Tailwind as a Design System**
    - [I Was Wrong About Tailwind...](https://www.youtube.com/watch?v=ZuLn42merAg)

---

## December 2, 2022
**Full stack documentation**
- [JSNation 2022 with Rich Harris](https://www.youtube.com/watch?v=RwBolXX9Pis)

    ![Full Stack Documentation as a Battenberg cake](assets/images/journal/full-stack-documentation.png)

    - [learn.svelte.dev](https://learn.svelte.dev/): an interactive browser-based learning platform for Svelte.

---

## September 29, 2022
I noticed some interesting search results while researching some ideas for having students build a game on the command line:

**Search phrase**: "best way to teach js"
**Top result**:
[The 5 Best Ways to Learn JavaScript Fast in 2022 (For Beginners)](https://techbootcamps.utexas.edu/blog/best-ways-to-learn-javascript/)
1. Self-Guided Websites and Courses.
2. Books.
3. Coding Boot Camps.
4. Meetups and Networking Events.
5. Starting Your Own Projects.

It doesn't look like there's a lot of content out there for teachers? Maybe zooming out will lead to better results? Spoiler alert: the answer is a definite yes!

**Search phrase**: "the best way to teach programming"
**Top result**:
[Ten quick tips for teaching programming](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006023)
1. **Remember that there is no geek gene.**<br>
    Competence at programming is not innate but is rather a learned skill that can be acquired and improved with practice.
2. **Use peer instruction.**<br>
    In simplified form, peer instruction proceeds in several phases:
    1. The instructor gives learners a brief introduction to the topic
    2. The instructor then gives learners a multiple choice question that probes for misconceptions rather than simple factual recall. The ideal questions are those for which 40%–60% of students are likely to get the right answer the first time.
    3. Learners then vote on the answer to the question individually, thus formalising their initial prediction.
    4. Next, learners are given several minutes to discuss those answers with one another in small groups (typically 2–4 students), and they then reconvene and vote again.
    5. Then, the instructor can act on the latest answers. If all the learners have the right answer, the instructor can move on. If some of the wrong answers remain popular after group discussion, the instructor can address those specific misconceptions directly or engage in class-wide discussion.
3. **Use live coding.**<br>
    Rather than using slides, instructors should create programs in front of their learners.
    - Don't go too slowly;
    - Start with a partial skeleton that includes the boilerplate (preferred) or having it on hand to copy and paste when needed;
    - Instructors may give students starter code that relies solely on concepts they have already mastered and then extend it or modify it with live coding;
    - Ensure that learners have reference material available after lectures, such as a textbook, but recognize that students of all ages increasingly turn to question and answer sites such as Stack Overflow for information.
4. **Have students make predictions.**<br>
    The key to making demonstrations more effective is to make learners predict the outcome of the demonstration before performing it.
    - Crucially, their prediction should be in some way recorded or public, e.g., by a show of hands, by holding up cue cards marked with A, B, C, or D, or by talking to their neighbour;
    - Instructors should be careful not to punish or criticise students who predicted wrongly but rather to use those incorrect predictions as a spur to further exploration and explanation.
5. **Use pair programming.**
    - One person (called the driver) does the typing, while the other (called the navigator) offers comments and suggestions. 
    - The two switch roles several times per hour.
    - It's important to put everyone in pairs, not just the learners who may be struggling, so that no one feels singled out.
6. **Use worked examples with labelled subgoals.**<br>
    Students perform better when worked examples are broken down into steps (or subgoals) that are given names (or labels):
    ![Screencap of a subgoal labelling example](assets/images/journal/subgoal-labelling.png)
7. **Stick to one language.**<br>
    Courses should stick to one language until learners have progressed far enough with it to be able to distinguish the forest from the trees.
8. **Use authentic tasks.**<br>
    Learners find authentic tasks more engaging than abstracted examples. A classic question in computing (and mathematics) education is whether problems are better with context (e.g., find the highest student grade) or without (e.g., find the maximum of a list of numbers). Bouvier et al. examined this with a multiuniversity study and found no difference between the two. They suggest that since it makes no difference, other considerations (such as motivation) should be given priority.
9. **Remember that novices are not experts**<br>
    Novices may need to spend time thinking about an algorithm on paper (something expert programmers rarely need, as they have usually memorized most common algorithmic patterns). They may need to construct examples in guided steps. They may struggle to debug. Debugging usually involves contrasting what is happening to what should be happening, but a novice's grasp on what should be happening is usually fragile.
10. **Don't just code.**<br>
    A growing number of educators are including Parsons Problems in their pedagogic repertoire. Rather than writing programs from scratch, learners are given the lines of code they need to solve a problem, but in jumbled order. Reordering them to solve the problem correctly allows them to concentrate on mastering control flow without having to devote mental energy to recalling syntax or the specifics of library functions.

Probably the best "paper" I've found on how to teach code.

---

## July 19, 2022
Some thoughts about Fall semester with two schools. One has traditional assessments and the other definitely not. But what are the common Learning Outcomes?

### As a barely junior developer, I want to be able to...
1. Follow instructions, so that I can:
    - Install third party libraries, packages and frameworks by following the developer documentation.
    - Incentivise my employer(s) to write more/better devops guides.
2. Effectively perform online searches, so that I can:
    - Solve my problem before asking for help.
    - Find alternatives to proposed tools.
3. To know when to ask for help, so that I can:
    - Not get trolled in an online help forum.
        - (Be respectful of other people's time.)
    - Show proof of work and receive feedback/street cred.
    - Accurately assess my own learning progress.
    - Finally crush this nemesis bug!
    - Just move on to the next problem (after a break).

---

## July 4, 2022
- [How I Would Learn To Code (If I Could Start Over)](https://www.youtube.com/watch?v=k9WqpQp8VSU)
    - Chapter markers provided(ish)
    - This guy's is great! 
        - TODO: Explore his other videos 
    - His list is a great breakdown of the high-level learning outcomes that any curriculum should have.
    - Breakdown:
        1. Mindset
            1. Adopt a coding mindset.
                - How can [some problem] be solved with code?
                - Learn humility.
            2. Learn how to problem solve.
                > "Coding is just a tool for problem solving. The hard part is problem solving."
        2. Coding
            1. Learn one language deeply.
            2. Learn scripting.
                - bash/python/node/etc.
            3. Create a personal project.
                - Partictpate in a hackathon.
            4. Practice for interviews.
        3. Developer environment
            1. Learn the terminal.
            2. Learn your way around an editor.
            3. Learn Git and become familiar with version control.

---

## June 26, 2022
Breakdown: [Upgrade Your Stream Deck: 9 Advanced Tips For Streamers](https://www.youtube.com/watch?v=HA7tA4lRBpE) by Gaming Careers
- Launching and Arranging Applications
    - [Windows Mover](https://apps.elgato.com/plugins/com.barraider.windowsmover) isn't available on Mac :(
- Audio Routing
    - [Audio Switcher](https://apps.elgato.com/plugins/com.fredemmott.audiooutputswitch) available for Mac!
    - [Sound Deck](https://apps.elgato.com/plugins/com.geekyeggo.sounddeck) isn't available on Mac :(
- Testing Stream Connection
    - [Speed Test](https://apps.elgato.com/plugins/com.barraider.speedtest) isn't available on Mac :(
- Timers and Counters
    - [Stream Countdown Timer](https://apps.elgato.com/plugins/com.barraider.streamcountdowntimer) isn't available on Mac :(
    - [Stream Counter](https://apps.elgato.com/plugins/com.barraider.streamcounter) isn't available on Mac :(
- Flashback Recording
    - "Flashback Recording" Plugin doesn't seem to exist?
- Raids
    - "Live Streamers" Plugin doesn't seem to exist?
- Camera
    - [Cam Control](https://apps.elgato.com/plugins/com.barraider.webcam) isn't available on Mac :(
- Extra Keys
    - Stream Deck has an option to couple a button to a hotkey.
- Multi Actions
    - Stream Deck allows you to couple multi-actions to a single button press.

---

## June 25, 2022
New Breakdowns:
- [OBS Studio - Advanced Mic Settings (Noise Removal, Compressor, Noise Gate)](breakdowns/twitch-sound-filters.md) by Gaming Careers
- [How To Show Chat Messages On Stream](breakdowns/twitch-featured-chat.md) ("Featured Chat") by Gaming Careers

---

## June 17, 2022
Going to test some Twitch stream settings today.
- First attempt: copying the settings from [Best OBS Studio Settings for M1 Mac Users](https://www.youtube.com/watch?v=_f8SYE6BbjM)
    - And... it seemed to work just fine! I even [earned an achievement](https://dashboard.twitch.tv/u/browsertherapy/achievements).
- I thought my 1920x1200 Dell monitor would be useful for the extra screen real estate but it's just as much a pain as I remember from the last time I setup OBS. It reminds me of why I bought the proper 1080p BenQ monitor. I'll swap those tomorrow.

### Installation/configuration Guides
**User Story**: As new Mac buyer and JAM Stack coder, I want a quick reference for the software I'll need to install as a developer because I've totally forgotten what I did the last time I bought a computer.

Convergent guides for:
- installation
    - is it already installed?
- configuration 
    - what's the bare minimum I need to do to not embarrass myself later?
    - what are some of the options I need for my current situation?
- quality of life
    - I'm starting to feel the grind and it's getting in the way of coding. Got any tips?

**The things**:
1. Double-click and forget
    - Zoom
    - Discord
    - Firefox
    - Chrome
    - Dev browsers
        - Postman
        - FF Dev
        - Chrome
    - VS Code
    - Git?
2. homebrew and nvm
3. iTerm with Oh My Zsh!
4. VS Code config

---

## June 15, 2022
Install log:
1. Firefox
    - Lastpass extension
2. Zoom
3. Focusrite Control (Scarlett 2i2)
4. LogiTune (Brio camera)
    - Might not be the best option? Alternative could be G Hub.
    - Tried G Hub but it doesn't offer any more settings.
5. Stream Deck software
6. Wacom Desktop Center

**Question**: Is the current version of OBS (27.2.4) still running in Rosetta?
- According to [this video](https://www.youtube.com/watch?v=Z1XX7I4ygqk) you can tell the difference between ARM64 and Intel using the Activity Monitor
- OBS (27.2.4)
    - **Does NOT** run natively on ARM64. There's an experimental ARM64 build based on 27.2.0.
    - it doesn't look like the Stream Deck OBS plugin will work with the ARM64 build.
- Streamlabs (1.9.1): 
    - **Does NOT** run natively on ARM64. No sign of future support so far.
- Twitch Studio (0.108.12):
    - **DOES** run natively on ARM64! It's still in beta and I have no idea how it compares. 
- Side note: The InceptionU network does 475Mbps up and down!

---

## June 14, 2022
### M1 Mac Mini Setup!
Physical setup and peripherals:
- Dell display: 1920 x 1200
- BenQ display: 1440 x 2560 (portrait)
- Logitech Brio webcam
- Elgato Stream Deck
- Focusrite Scarlett 2i2
- Wacom Intuos tablet (7.9" x 6.3")

### Streaming Research
Some questions that need to be answered for the Twitch Stream
- [OBS](https://obsproject.com/) or [Streamlabs](https://streamlabs.com/)? [Twitch Studio](https://www.twitch.tv/broadcast/studio)?
    - What settings?
    - How to properly set up Profiles and Scene Collections
- [Loopback](https://rogueamoeba.com/loopback/) or [SWB Audio App](https://shinywhitebox.com/swb-audio-app)?

**Findings**
- [Profiles & Scene Collections](https://www.youtube.com/watch?v=LIFaXZkk_-Q) (6:24) by EposVox
    - Great summary of the two features.
    - Seems like good content: [his OBS Masterclass Playlist](https://www.youtube.com/playlist?list=PLzo7l8HTJNK-IKzM_zDicTd2u20Ab2pAl)
- [How to Stream on Twitch OBS Studio Tutorial on M1 Max Macbook](https://www.youtube.com/watch?v=PMT2WEL5-gw) (10:36) by Blendlogic Tech
    - Pretty concise
    - His goals are to stream and record 1080p @ 60fps
    - Uses Blackhole for audio sharing
- [Installing ARM64 OBS Studio on M1 Apple Silicone Natively](https://www.youtube.com/watch?v=Z1XX7I4ygqk)
    - This is surprising to me: OBS is still running on Rosetta after a year and a half.
    - I'm assuming Streamlabs and Twitch Studio are also running Rosetta?

---

## June 12, 2022
### Mac Mini Setup for Streaming
**Streaming software**
- [OBS](https://obsproject.com/) or [Streamlabs](https://streamlabs.com/)?
- [Loopback](https://rogueamoeba.com/loopback/) or [SWB Audio App](https://shinywhitebox.com/swb-audio-app)?
- [Zoom](https://zoom.us/)

**Coding Software**
- VS Code
    - Live Server
    - GistPad
    - Open in Default Browser
    - GitLens
    - Code Spell Checker
- iTerm
- Oh My ZSH!
- Homebrew
- nvm
- Git
- Browsers
    - Firefox
    - Chrome
- Postman

**Messaging**
- Slack
- Discord
- Teams

**Quality of Life**
- Rectangle
- Lastpass
    - Firefox Extension
    - Chrome Extension

---

## May 8, 2022
**Assumption**: A beginner will need a more convergent learning path until they can use their imagination.

**Theory**: Providing a list of recommended starter projects will aid in learning.

**Questions**:
- How do we measure project effectiveness in learning?
- Are projects the best format for early learning?
- Does this apply equally to children vs ya vs adults?
- How small should the projects be?
- When do you introduce fat arrow? Function statements or expressions?
    - Refactoring exercises: 
        - Finished code is given with `function` expressions. Goal: refactor using arrows.

## Goal
Create sample projects geared toward board games. Projects that:
- can highlight a core learning topic
    - dice 
        - `number`
        - `array`
        - `Math` object
- is visual and can naturally introduce design elements
    - dice
        - html entities
        - font icons
        - svg
        - animation
- could make sense as a component in a larger project
    - dice roller: digital dice tower
        - separation of concerns

## Project examples
- dice 
    - roller
    - builder
    - games/components/apps
        - iphone substitute if you forgot your dice
        - 
- deck
    - shuffler
    - builder
    - games/components/apps
        - memory game
        - war
        - discards
        - a card you stick on your head, game
- counter
    - health
    - inventory
    - wallet
- backpack
    - items!

---

## April 6, 2022
Lean Canvas Ideas
- Potential customer segments
    1. Students
        - Professionals upgrading their skills
        - Service industry looking for a new covid-safe career
        - Entrepreneurs wanting to build their own app
    2. Teachers
        - Coder who wants a backup career
        - Old-school teachers who want to learn new tech
    3. Potential employers
        - Companies looking for cheap devs
- Problems: Professionals upgrading their skills
    1. Pre-bootcamp: It takes $10,000+ to find out if you even like coding
    2. Post-bootcamp: Hard to stick with the coding habit
    3. During-bootcamp: Difficult to find relevant tutorials
- Solution: pre-bootcamp
- Moving to Milanote

---

## April 23, 2022
Research: Game design/development as a tool for teaching programming.
- Most of the "[game development javascript](https://www.google.com/search?q=game+development+javascript)" results for articles and videos are unsatisfying. They are either:
    - are too advanced for JS beginners (game engines/frameworks)
    - focus on video game-like experiences and jump straight to `canvas` (would like to start with node/cli game to start)
    - don't talk about the fundamental mechanics and theory behind games.
- Refining my searches to "game mechanics" helped but results were still more advanced. 
- "[solo game mechanics](https://www.google.com/search?q=solo+game+mechanics)" produced the most promising results thus far:
    - [10 BEST Solo Board Game MECHANICS in 2021](https://www.youtube.com/watch?v=S5VdJtj151g) (from least to best)
        - Dice rolling
        - Flowcharts or procedural AI
        - Dummy Opponents (automa); playing for points
        - Tile/Worker placement
        - Card drafting
        - Event deck (action queue)
        - Grid movement
        - Puzzle solving and hand management
        - Deck, bag and pool building
        - The narrative
    - [The mistake every new game developer makes](https://www.youtube.com/watch?v=ZMbIvmv25u0)
        - tdlr; start with a prototype to:
            - test your game ideas
            - generate new ideas
        - He used Unity to create quick and buggy prototypes to test variations on a side scroller with a magnetic game character.


---

## Feb 20, 2022
Goal: Research - Syntax highlighting for specific lines in blog posts, lesson plans and slides.
- PrismJS has a [line highlighting](https://prismjs.com/plugins/line-highlight/) plugin.
    - This probably wouldn't work with the Content module when using markdown. Probably wouldn't without some way to add data-attrs. Remark doesn't seem to want to work so maybe adding `pre` and `code` manually to the md would work?
- RevealJS apparently has the ability to [highlight lines](https://revealjs.com/code/#line-numbers-%26-highlights) within a block and also [step-thru highlights](https://revealjs.com/code/#step-by-step-highlights).
    - Again, not sure how this would work with the markdown plugin. Probs just add the `pre` and `code` blocks manually. Ugh. 

---

## Feb 6, 2022
- Wrote break down of [Goals, Objectives, and Learning Outcomes](goals-objectives-learning-outomes.md)

---

## Feb 5, 2022
Goal: Build a list of Achievement rubrics based on the Outcomes, not the requirements of the assessment.
- Found these two great videos in the last week or so
    - [How to Create Rubrics for Assignments](https://www.youtube.com/watch?v=Fr48veTtVpM)
    - [Goals, Objectives, and Learning Outcomes](https://www.youtube.com/watch?v=g_Xm5IljYKQ)

---

## Feb 3, 2022
- Re-ordered JS section of the [Gist list](gists/index.md)

---

## Feb 1, 2022
- Compiled a [list of my Gists](gists/index.md) because I'm tired of searching randomly on the website. This way I have a birds-eye view of content I can throw into a lesson at the last minute (with a little refactor, update, cleanup).
    - TODO: 
        - reorder by complexity and category
        - find sequences like the github stuff
- R&D: Are Net Ninjas repo branches a good idea?

### Rubrics
- [How to create rubrics for assignments](https://www.youtube.com/watch?v=Fr48veTtVpM) by the U of A!
    - [The AAC Rubric Wordsmith](https://www.aac.ab.ca/wp-content/uploads/Rubrics/BBRp18-23.pdf)
        - Great Rubric cheat sheet but a PDF?
    - This is very compatible with brightspace
- This got me to thinking about formative vs summative assessments
    - Found [this article]((https://www.gre.ac.uk/learning-teaching/assessment/assessment/design/formative-vs-summative)) with a nice font.
- A Learning journal is definitely a formative assessment
    - formative assessments are usually for few or no marks
    - for coding courses, I think 20% over the span of the course is fair IF they have to code the journal and push to Git.


---

## Jan 26, 2022
- Breakdowns in prep for incoming Lab Facilitators
    - [What is Pedagogy? - 4 Essential Learning Theories](breakdowns/what-is-pedagogy.md)  
    - [Adult Learning Theory](breakdowns/adult-learning-theory.md)
    - [How to teach programming](breakdowns/how-to-teach-programming.md) by Felienne Hermans

---

## Jan 15, 2022
### Keeping a learning journal (but for code)
- Currently marking a Git assignment for starting a markdown learning journal and was inspired to create a new journal dedicated to learning how to teach.
- Found some great videos on the subject:
    - [How learning journals can help students grow](https://bigthink.com/the-present/learning-journals/)
        - [And the breakdown!](/breakdowns/how-learning-journals-can-help-students-grow.md)
    - I found other videos on journaling about learning to code but they're lock up in the Shield Youtube plugin. I'll have to find them again. Very irritating.
    - Search terms I think I used in Youtube Search on the Shield:
        - "programming journal"
            - [5 Productivity Tools For Programming](https://www.youtube.com/watch?v=s8wQz6EVUzw) by Kalle Hallden
                - Git number 5!
                - TODO: breakdown
        - "markdown journal"
            - [Writing Notes in Markdown: A Primer](https://www.youtube.com/watch?v=NnCy7wJRgP0)
                - Great intro to markdown
                - TODO: prep, breakdown
                - are his slides written in markdown?
                - [@10:02](https://youtu.be/NnCy7wJRgP0?t=602): How does this benefit your note-taking
                    - He's assuming Obsidian. 
    - Couldn't find much so moved on to google search on Morty:
        - "keeping a programming journal"
            - [The power of keeping a coding journal](http://thomasburette.com/blog/2014/06/25/the-power-of-keeping-a-coding-journal/)
                - from 2014 but it's still relevant
                - great visual hierarchy at the start but it breaks down as it continues.
                - TODO: breakdown, visual hierarchy example, prep?

### Dated journal entries
Quantifying some objectives and criteria for a Coding Journal
- accepted locations
    - As an entry in your dedicated `coding-journal` repo.
    - In the README of a remote repo (project, assignment, etc) under the heading "Code Journal"
- General content categories. An entry can contain a combination of the following.
    1. class notes
        - video timestamp markers for important information
        - instructor/classmate quotes
        - observations
        - helpful/useful links pasted in the Chat
        - questions for later
        - reminders for Lab Time
        - TODOs
    2. self-assessment
        - Bring your receipts: What metrics are you basing your performance on?
            - the search terms you're using
            - GitHub activity
            - number of labs completed in class
            - amount of time spent coding
            - number of pair-coding sessions attempted
        - What concrete and precise goals have you set for yourself?
            - "I want to set aside a half-hour every day, dedicated to coding"
            - "I want to get a great search result with phrase that's 3 words or less"
            - "I want to push a commit every day"
            - "I want to review the Prep before every class"
            - "I want to attempt one tutorial every Lab Time this week"
        - Are you meeting the expectations you've set for yourself?
        - What steps can you take to learn more effectively?
        - What topics covered in class has interested you the most?
        - What are today's wins?
    3. Lab/tutorial/exercise attempts
        - What's the objective?
        - Does anything need to be planned out?
        - Numbered steps you've taken to complete the objective
        - Observations
        - Obstacles encountered
        - Links to starting and finishing commits
        - Reflection: was the objective achieved? Why or why not?
    4. Attributions
        - Have any classmates helped you?
        - Helpful/useful links and resources
            - Articles, videos, etc
            - Stack Overflow answers
            - Documentation references
        - What sites and content creators have you found most helpful?
    5. Research sessions
        - What questions do you want to answer?
        - What search terms are you using?

### Content breakdowns
Not sure if this fits under a coding journal? It definitely doesn't have to be a dated entry. Might be better off as an assignment or achievement (cleric badge?).

A breakdown is a summary/synopsis of a single article, video, podcast, etc:
- What are the key concepts?
- Useful quotes
- Sample code and snippets 
- Video chapter markers and timestamps
- Related and useful links
- Examples:
    - [How learning journals can help students grow](/breakdowns/how-learning-journals-can-help-students-grow.md)

---