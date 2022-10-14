# The Technical and Organizational Infrastructure of the Ruby Community - Adarsh Pandit

## Takes
- Systems are a combination of interpendant elements, but then its purpose of the system is what it does.
- The Ruby System consists of: Ruby (MRI), Rails, Gems, Bundler, Community, Learning
- When thinking about the system components, it's worth asking following questions:
  - who is doing the work?
  - how are the decision made?
  - who pays for the work?
- In Ruby (MRI), apart from the public [issue tracker](https://bugs.ruby-lang.org), there are regular dev meetings, and there are [minutes from those meetings published online](https://github.com/ruby/dev-meeting-log)

## Raw notes
Infrastructure
Thinking in Systems - Donella H. Meadows (2008)

The purpose of the system is what it does.

No system is broken. We might not like what is doing, and we're not not happy about what it does, we need to change it.

What is a system?

The system of the town is designed to get kids get safely to the school.

System of the Camino Road - bike path that goes into the car lane.

How did Finland eliminate pedestrian and cyclist deaths?

In Finland - multidiciplinary committee for every fatal accident in bicycle.
US - multidiciplinary committee for airplane crashes, but not bicycle.

Transparency and documentation, setting goals, accountability,

### Community infrastucture
[infrastructure]

Ruby Community Infrastructure:

Questions:
- who is doing the work?
- how are the decision made?
- who pays for the work?

MRI
- who is doing the work?
"I don't know". Matz mentioned, but the core team is not presented.
- how are the decision made?
Ruby Issue Tracking System - there are (regular dev meetings)

Original mission: "Programming happinnes"

- who pays for the work?
We don't know. Who supports Ruby?


MRI
- Core Team
- Contributors Team
- Issues Team

"Contributing to Ruby on Rails"

"Rails Governance"
She announced how people are moved between the teams, she talked about making the
"The Sucess of Ruby on Rails"

who pays:
- Basecamp
- GitHub
- shopify
- Heroku

Bundler:
- who is doing the work?

- how are the decision made?

- who pays for the work?
(2013 - it was volunteer run)

ruby together
All of the infrastructure used by Ruby developers today.
Bundler:
- Bundler team
- rubygems team
- comes from Ruby Central

Gems
- who is doing the work?
sole developers
- how are the decision made?
by maintainers
- who pays for the work?
not really, but GH contribution is an example

Community

Learning World

- Have regualr meetings
- Takes notes and share them
- Have an advisory board
- Make your project easy to join
- Get feedback
- Think about the future

"Matz" is to people to get involved. Matured arden, projects are stable, even boring. How they can be better?

"The scarcest resource is not ... . It is our willingness to listen to each other and learn from each other."

"Communication is a solution to solving all problems."

## Questions
How other communities do that?
Rust - "Governance" tab + Roadmap on their main webpage
python (steering-council) "RFC proposals - PEP)


## Presenting style
- clear pronounciation
- "american" style of presentation, engaged but emotionally distanced
- some controversial takes, on the verge of being controversial - but said with such confidence, that they were just stated as facts.

# From massive pull requests to trunk-based development with Ruby - Vesa Vänskä (KISKO Labs)

### Takes
- Trunk based development means you do push changes to main branch without staying on feature branch for a long time
- You do push "unfinished" changes to production, but you use techniques like feature flags to "hide" the changes
- DORA metrics is a valuable metric to use when assessing the state of your application

## Raw notes
10 lines of code = 10 issues
500 lines of code = "looks fine."

github (back in the day when he started to do branches) (2008)

GitHub Flow (GitHub made creating branches cheap).

GitHub Flow (PR flow):
[github flow images]
CreatePR
Add Commits
Review Comments
Merge PR

Trunk-based development.

What is it?
- Source-control branching & collaboration model
- Collaboration happens in trunk (aka main)
- No other long-lived branches

Branches are good, long-lived branches are no-no.

(hors to a week maximum) and flowing through Pull Request style code-review & automation before merging into the trunk.

You merge commits straight into the trunk.

Caveat: This talk is about services.

"It will never work"
- "This feature will take months to build"
- "Broken code will got to production all the time"
- "But we are not Google"
- No


### "This feature will take months to build. My branch needs to be long lived"
Feature flags.
e.g. using Flipper:
```ruby
<% if Flipper.enabled?(:widgets, current_user) %>
  <% feature %>
<% end %>
```

And then enable for specific users/beta testing.


### "Broken code will got to production all the time"
Conlution: Continuous Integration Server - a pre-requisite for the trunk. If the build is not green, it stops the process. The bareer is quite low.

Spend more time on Monitoring - getting more visibility into the system, e.g. exception handler or.
`ActiveSupport::Notification` - instrumentation API for Ruby/Rails.

### "But we are not Google"
The biggest change in his thinking.
Previously I thought that techniques are for the big teams. These techniques (trunk) are viable for any size of the team.
Productivity is a key for Ruby - and trunk fits nicely.

### CI/CD
Continuous Integration | Continous Delivery
CI - Everyone integrates all the services
CD -

Either you do the whole CI/CD or do nothin - that's a wrong misconception.

CI and its features might be enough, you don't have to dwell into CD from the beginning.

"Any improvements made anywhere besides the bottleneck are an illusion."

"The advantages of large, long-running pull requests" - DHH advocates that long PR are actually a good thing.

### DevOps survey/reports
DORA metrics

Optimising these metrics will guide you.

DORA:
 - Deployment Frequency
 - Lead Time for Changes
 - Change Failure Rate
 - Time to Restore Service

State of DevOps survey 2022 results:

- Deployment frequency: Between once per week and once per month
- Lead time to changes: Between one week and one month
- Time to restore service: Between one day and one week
- Change failure rate: 16%-30%

Start experimenting!

Additional resources:
- trunkbaseddevelopment.com

# Lightnig talks

## Talks 1 - Renato Cerqueira

### Takes
### Draft notes
AppTweak - ASO Leader

- Why to move from Sinatra?

When we started using Sinatra, we had no documentation.
Alternative was Frape (from 2010).
It has parameter validation, grape-swagger, so the documentation is created.
Grape is inspired by Sinatra, because of the inspiration.

They couldn't move all of them:
- Some of them
- Rack::Cascade to migrate only part of the endpoints.

It progressively moves endpoints one by one.


## Talks 2 - Why bother about Questions

### Takes
- Questions are so important, but we often forget about them


### Draft notes
If you were a new superhero, what special power would you have?

Read other people's mind
Give smart answers always

EM:
- get people to understand each other automatically, without intervention

Engineer:
- work more collaboratively
- understand other people, get rid of poverty


He found answers from the meeting very wholesome.

What actually happenned at the meeting that made him feel that way?


At a more fundamental is a question.

"According to Albert Einstein, asking questions is not about getting answers, is about solving problems"
"Questoins connect

"The road from ignorance to knowledge leads through asking questions."

Questions help us work towards a shared purpose.

Questions -> Geto to know your team members better -> Trust -> Psychological Safety

The questions reveled so much about the team.

## Talk 3 - Hans - Building Delightful Command-Line Apps in Ruby

### Takes
### Draft notes

Ruby Developer from Vienna, Meister.

Command line apps makes you feel like a hacker.
CLI - rails app.
Rails is successful because of its command line.
What makes CLI successful?

1. Affordances & Signifiers
2. Feedback
3. No surprises

Ruby loves CLIs.
Thor - whatisthor.com
Bundler uses Thor as well.

Thos makes it easy to provides arguments,
Termianl Apps The Easy Way
ttytoolkit.org - Piotr Murach

Widgets you can use on the terminal
Show progress that works as text.

## Talk 4 - Welcome Ruby juniors - Hana Harencarova (@hanaharencar)

### Takes
### Draft notes
There are companies looking for hires.
There are juniors in the room.

So how did I get here?

She comes from "Psychology" background, then learned R during PhD, baby, Ruby, Sei Online, second kid, "Moms Learn to Code", le wagon, GitHub -> Euruko

#### the happy path
- Look for companies you want to work for
- Companies want you to succeed
- Build on your srengths
- Find your mentors
- Keep meeting people

As a colleague....
- Rech out to them when they join
- Be ready to help
- Do pairing and mentoring sessions
- Make it clear it's okay to ask

Show juniors taht you don't know answrs and you're vulnerable.

Companies:
- Craft the job adds and make the interview a pleasurable exper
- Invest in the onboarding proccess

MINSWAN - Matz is nice so we are nice

# Ruby & JVM: A (Jruby) Love Story - Yarden Laifenfeld

## Takes
JRuby is another

## Raw notes
@yardenlaif

She is going to talk about Java on the Ruby conference :o
Software Engineer at Rookout
Background in low level C
Ruby/Java/Go/C#/Python/JavaScript/C++

Support JRuby.

(Year 2000) JRuby is a 100% Java implementation of the Ruby programming language. It is Ruby for the JVM.
(JVM) - Java Virtual Machine

In 2001 - JRuby is created.

JRuby Advantages:
- Integration with Java libraries
- Running atop the JVM
  - Threads
  - Long running applications - optimising the in the long running application, service in Ruby in 10 years.

 There are people who like writing Java, so you can integrate with Java libraries.

 ### Why JRuby.md?
 (Jordan Sissel, 2010)
 - core and stdlib ruby changes violently
 - cross-ruby date library
 - need for threads

### CRuby Advantages
- Larger Community
- More features

More people to fix bugs.
2.6 and lower.

Should you use JRuby?
I don't know, you choose.

You need to make the trade-off. Changing to JRuby, if you know Ruby, it's not difficult.
Task: Support JRuby in a debugger for productioun.

Supporting JRuby:
- Running an app
- Adding a breakpoint
- Collecting data

### Java or Ruby
We had Java debugger and Ruby debugger.

Running an app
```bash
rvm install jruby
rvm use jruby

bundle install
```

3 business days later...

`bundle config unset force_ruby_platform` - that's for CRuby, not Jruby!

It says you have to use native platforms, which are not supported by JRuby.

### Now - adding an endpoint
TracePoints
[tracepoints]

```ruby
tracepoint = Tracepoint.new(:line) do
  # ...
end
tracepoint.enable(target: method(:m1), target_line: 14)
```

An error:
`wrong number of arguments`

At this stage, you would she decided to go to Java.

### Java implementation

- -javaagent flag
- premain entrypoint
- Instrumentation API

How JVM works?
-> Code -> Compiler -> Bytecode -> JVM

`new Item()`

JVM -> Get Item class bytecode -> Class Loader -> Return Item class bytecode

You can add a transformer to change your code through the instrumenter.

JVM -> Get Item class bytecode -> Class Loader -> Return Item class bytecode -> Code Modifier ->


Adding a breakpoint

Expectation: It doesn't work.

Suddenly, the breakpoint is active.

"Something smashing the keyboard is the answer."
A few, spaced out invocations -> Class isn't loaded

JRuby Compilation Modes:
- Interpretation (line by line, no bytecode is loading)
- JIT - it will take hot points - code that is run often.
- Compilation (every class in JRuby is loaded as a Java class, it will go through the interpretation)

`compile.mode=FORCE`

### Collecting data
- class scope, self, context - many variables in the data passed from the Java

Then in self there is another set of many variables.

That allowed her to support JRuby

### What Next?
- Ruby TracePoint API
- Java Agents
- Class Loaders

@yardenlaif

## Questions?
Big learning from JRuby?
- When it was created it was 2001, so it's been a long time.

#  Andy Carroll - Keynote

## Talks

## Raw notes

These are not object shapes.

They are the same.

Welcome to Cambridge - 2018.
A room of full of people - Business of Software.
CTO of small
STEP 1 1987 - copying the keyboard
STEP 2 2007 - Rails
STEP 3 2022 - PROFIT?

## Story of Steve Shirley
Steve Shirley
Aged 5 - 1939, excelled in maths, there was no standard curriculum in '50 in UK.
Aged Post Office Research.

ICT1305

1962

Freelance Programmers - F International
It sounded

- I have no office
- i have no employees

1996 -

Remote in '60.
Flexible - 20 hours a week.
Employee Owned - shareholders strust, so programmers were receiving money.
Women.

Dame Stephanie "Steve" Shirley - OBE CH (Companion of Honour)

First women this, I couldn't drive a bus, I couldn't open a bank acount.
She had to fight the work.
Home and families responsibilities.
She started to challenge the.
"Steve" Shirley

computer - a person who makes calculations

THE POWER OF MATHS

1906,
Grace MF-ing Hopper
She joined the reserves. She was sent to Harvard.
The machine was itself.
She was going through rank and competetence

1946 - computer.

She was no means female programmers. Anyaxis.
The demo was a spectacular.
Man posing to the
ENIAC.
Giant brians were the women.

WITI had no knowledge of their works.

In 1951 she worked on the first.

A-0
A-1
A-2
MATH-MATIC
FLOW-MATIC

PDQ Coomunity (Pretty Damn Quick)

COBOL - by no means.

Programming - Software Engineering (NATO Software Engineering Conference, in 7-11 Oct, 1965)

Suzanne Fowler (2017) - Uber

Turing - The limitation game
Hidden Figures (book > movie)

It's okay for me to talk about because "I look like you".

Less of a question, more of a comment guy.
Technology doesn't have anything to do with politics guy.
Politics is just a formalization of power.

It was just a joke, don't be so sensitive guy.
"Totally in your personal space".

Don't assume - or you make an ass of u & me
Don't assume. It takes effort not to steorotype.

Fear - We are scared of getting it wrong. Two flavours of fear:
- OOPS - best to be nice, "I'm sorry that you were offended"
- Will it be harder? - pushing against the stereotype is not easy

Pay fairly. I mean it. - How to pay individuals. They know who is underpaid. Fix the apy of the folks that deserve it.
This will help with hiring too.

There is a risk that you will end up with the team consisting of the same looking guys.

Mentoring/ Sponsorship"

"Lending privilege"

Bring back

MATZ IS NICE AND SO WE ARE NICE...

Push against the easy path of how the things were.

It's difficult emotionally and practically. We can't take this on.

Another perspectives. You are welcome, I'm sorry for the extra effort you need to make.

Thanks, do better, and sorry for all the swears.

It's bailing out for world which is more open.
