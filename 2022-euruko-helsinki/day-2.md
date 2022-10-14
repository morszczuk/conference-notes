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
