INTRO
* Problem. Why care? Here's what I'm offering
  * We live in a world that cares about getting quality software out quickly to the market then evolving products with emerging requirements. In our industries short lifespan, we've tried a few different ways to meet these needs. 
  * We went for wild hacking to the software crisis in 1970. We decicided to build huge artifacts to get things right at the start, and produce reams of documents about code, so it couldn't possibly ever go wrong. Certain methodoligues required 37 distinct roles to be covered on a project, like librarian, progress checker, integrator.
  * In 2001 the agile manfesito was created as a reaction to these heavyweight process, giving birth to the era of lightweight processes. 
  * We are now nearly 15 years after that point in time, we've still got a lot to learn about building the right thing, but I believe we've worked out how to build the thing right. That is what I think agile develpment is about. And what we will go over in this talk.
  
* Why trust me? (I am one of you)
  * Used to do SDLC. Agile dev since 2005. Coach for a while, then joined TW. I run CodeCraft a software craftsmanship meetup in Glasgow.

* Audience check
  * How many devs / pms do we have here?
  * Average experience in the industry.

WHAT
 * Ask Twitter!
   * Being conscious of value and responsibility. Also good communication and being able to adapt and react to change. - @mr_urf
   * "they discuss more with other colleagues about the deliverables, on 2 fronts - Out With their own work but also internal to their own work" @jennylally
   * "An agile dev is a dev who can touch their toes" - @PaulBullivant
   * an agile developer considers their actions and work against the values and principles of the Agile manifesto. - @garyfleming

WHY
* Why use agile development?
  * Economics.
  * Reduce lead time to getting work done, while increasing customer satisfaction.
  * It will make you able to react to change by increasing the points where feedback is introduced. Promoting a shared understanding 
  * It won't make you much faster, but it will be sooner. It will help you deliver at a sustainable pace, which will be slower at the start of project. But saves leaving testing, integration and deployment to the end. Which is one of the main reasons projects fail.

INTRODUCE BODY OF TALK http://c2.com/cgi/wiki?ExtremeProgrammingCorePractices
* We will focus on What practices a agile developer uses.
* I believe these can be grouped into three areas of practices:
  * Fine scaled feedback
  * Continuous Process over Batch
  * Shared Understanding
* For each area. We'll learn about some of the practices that help. For reach practive we'll hear what is is and why we do it.

AREA 1: FINE SCALED FEEDBACK
* WholeTeam http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/whole_team_7E4B7BE3.html
  * What
    * CustomerRepresentative (sets priorities, best if from that world, may be aided by an analyst), Tester (maybe), Programmer all together in one room. Optionally: Coach, manager. Ideally no specialists, generalists with special skills.
    * Share goals and delivery responsibiltiy.
    * Contrast with WarRoom
  * Why
    * Reduces miscommuncation and speeds it up
    * Progress visibility: customer gets real feedback everyday
    
* TestDrivenDevelopment via UnitTests & AcceptanceTests http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/test_driven_development_DACEB1AF.html
  *  What: 
    * The practice of writing the code you wished you had, before writing the implementation.
    * This can be via programmer facing tests like unit tests and acceptance tests written in a business langauge rather than code.
  *  Why:  
    * UseItBeforeYouBuildIt. 
    * You start by writing a failing test case that you wish worked from a callers perspective. This makes a big difference.
    * YAGNI (do you need to add a player name? Assume you don't need something until you do.)
    * Minimum amount of code to implement a feature succesfully.
    * Design before build. 
    * Worked Example of Noughts and Crosses perhaps.
    
* PairProgramming http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/pair_programming_954480F4.html
  * What
    * All code is written by 2 programmers sitting side by side who are in constant conversation about the design, testing and code.
    * Techniques available to encourage sharing the time on the keyboard.
  * Why
    * Programming isn't about speed of typing. Otherwise we'd hire an army of typists. IT's a thinking activity with the code being a manifestation of the conversations resulting from that thinking.
    * It's about analysising trade offs and deciding what course to take. It's no always obvious at first, but conversation often teases it out.
    * Constant code review. Change the design before the work is 'done'    
    * Share knowledge throughtout the team
    
AREA 2: CONTINUOUS PROCESS OVER BATCH

* ContinuousIntegration http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/continuous_integration_80DF5104.html
  * What
    * Every commit that goes into VCS has tests run against it to make sure it compiles and works as expected. If it doesn't then the team are immedaiately informed.
    *  To support this you need to be commiting to your master branch mutliple times a day.
    *  Leaving code on a branch or on a devs machine for days doesn't cut it.
  * Why
    * Simplfied & faster integrations: Integration problems are much easier to resolve nearer to when the change happened that made them fail.
    * Improved Feedback: Latest version fo the code is available for the customer to see
    * Always shippable: The latest version is always available to release.

* RefactorMercilessly http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/refactoring_xp_programming_6368BEEC.html
  * What
    * Refactoring is the practice of improving the design of a system without changing its behavior
    * Devs consciously choose between refactoring and adding new functionality on a minute-by-minute basis. Trivail renames, or larget introducing new classes.
    * Automated tests provide the safety blanket which allows devs to do this continuously.
  * Why
    * If your system becomes brittle and inflexible, your developers will have to spend more time and money to add features or fix bugs. As the design continues to deteriorate, fixing one bug creates two more.  It's a battle against entropy; from cleaning as you go to design debt.
    * Allows the design to emerge over time.
    * Reduces cost of change.

* SmallReleases http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/small_releases_782AF220.html
  * What
    * Much like integrating late, releasing late means you take a long time to figure out if your software works
    * Let's say you have a production bug every 1000 lines of code. If you release 10k lines of code each time, you have many bugs, which will work together to cause harder to debug issues.
    * At a caompny which had a webstore taking thousands of orders a day, we were releasing once a a day. Our biggest incident was when we waited 5 days to release. We made it a policy to release once a day, regardless of how much was in it to avoid more incidents.
  * Why
    * Good feedback on if it is what your customers want
    * Signigicantly reduced risk of releases going wrong
    * Raises the quality consiciousness of the group. Sofware needs to be good enough to ship.

AREA 3: SHARED UNDERSTANDING

* SimpleDesign (DoSimpleThings, YouArentGonnaNeedIt, OnceAndOnlyOnce, SimplifyVigorously) http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/simple_design_63BCA71E.html
  * What
    * YAGNI: Never add a feature before you need. In case you might not need it.
    * Incremental: Not as much design up front. Takes courage to jump in without a formalized step.     
    * Don't generalize until it's needed in three places.
    * It's always faster and cheaper to replace complex code now, before you waste a lot more time on it.
    * Simple is somewhat ambigious. But not in XP. 4 Rules: Runs tests, no duplicate code, intent is clear, no dead code.
  * Why
    * Small initial investment: you can add a framework later if needed
    * Maintainable:  simple code is easy to change, it stops the rot.
    * Agility: faster to change the system when the customer requirements change

* CollectiveCodeOwnership http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/collective_ownership_DE6F39EE.html
  * What
    * Any member of the team can change any piece of code in the system at any time. change can be new feautre, bug fix or refactoring.
    * Used with pair programming and TDD, collective code ownership is an effective way to spread the knowledge of the system across the entire team. It encourages new ideas.
  * Why
    * No one is a bottle neck for changes.
    * Any non trivial program cannot be kept in one persons head. If you have to ask that person every time they will be wrong.
    * More reliable. If one person leaves the project you won't be as affected.

* CodingStandard or CodingConventions http://epf.eclipse.org/wikis/xp/xp/guidances/concepts/coding_standard_140001B7.html
  * What
    * 10 devs, all their ideas were expressed in the codebase. 
    * Collective code ownership requires that a standard is used.
    * Just use a published standard. Sun made this horrendus for Java and put the commuinity of this appraoch, but there are now a load of sane defaults that someone else has argued over. Let those arguments happen at the standards level, not on your team.
  * Why
    * Easier to read each others code
    * Refacotring support: consistentlu shaped code is easier to change

HOW TO APPLY THIS
* As a manager:
  * Start by getting the team on board. Agile is supposed to make it easier for developers. If it isn't then something is wrong
  * Go slow, management stuff affects the team much more
  * Add standups. get talking about major issues. Bring isolated architects in. 
  * Get infra in order: VCS, Unit tests, Build automation.
  * Get rythmns in order
  * Think about what practices you'd like to add
  * Use brown bags to discuss
* As a developer:
  * Bit of a challenge. You have to lead by example rather than decree.
  * Start unit testing. They'll see that you don't have to stay late since your code isn't full of bugs.
  * Start CI and then let others know when there is an issue.
  * They'll start coming to you. But you have to go first, especailly since you are looking to change things.
  * Use brown bads to dicuss

RECAP SLIDE (three topics, three practices in each)

CONCLUSION
* People pay us to produce software that's early to market, of high quality that meets or exceeds customer expectiations. We are still learning how to figure out exactly what to build. But weve known for a while how to build it. That is what agile development has discovered and taught us.
* Thank you.
