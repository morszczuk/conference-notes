# Yukihiro "Matz" Matsumoto - Keynote

## TL;DR;
-

## Meeting notes

Email that Matz received.
"Ruby is too good to be a scripting language" (so Ruby is a language that is too good for 100 lines of short script)

"Scripting languages do not need OOP"
"We proved him wrong".

"No one use Ruby, they use Perl/PHP/Python. There's not killer app. You shouldn't have created Ruby, we should focus on Perl. For the sake of the human beings."
"Ruby is slow. Web age is over. AI/ML/Web3!"
Ruby is not popular in these.
"Ruby is dead. Ruby is dead every year."

"A fox that borrows the authority of a tiger."

We have trade offs, we share experiences and we build.

Being a member of a team (Python/Rust community) doesn't make them superior. We need to find values. Values end with y. (Ruby/Productivity/Community/Joy/Money).

Those companies are valued at 60 mln dollars. They are created by software written in Ruby.

Y Combinator - 50 start ups. 13/35 of them use Ruby.

We cannot avoid noises, as long we create value, we create value. We can avoid the noise and keep omving forward.
Velocity / Productivity (also ends with y). It's quick to deploy. If we can't finish quick. It solves problems.

Popularity comes and goes. We should not dangle in the wind.

2010/2020s - "Static Typing is a cool kid."
1990/2000s - "Dynamic languages are ...?"

- TypeScript
- PHP
- Python

- Should Ruby add types?

No. Myths:
MYTH 1.
- Static typing is newer
FACT 1.
FORTRAN was staticly

MYTH 2
- Static typing has advantages
FACT 1.
- Comprehensive Checks -
- Works as Documentation -
- Better IDE Support - code completion, documentation pop-ups, in addition, compilers can parse code better.
- Better Performance
FACT 2.
- Verbose - not concise
- Reduntant - (as the Community, )
- Complex (Turing Complete) - tic-tac-toe in type declaratoin
- Forceful Community (Type Police) - some library owners, you should have type declaration or it's something bad. It makes the atmosphere of the community

Do we really need type declaration?

Static typic
We don't need declaration to check
Ruby3 - Static
Type information in signature files (rbs)

ruby/gem_rbs_collection
DefinitelyTyped conterpart

pocke/rbs_rails
Sifnatures for Ruby on Rails

typeprof
Signature Generator

Abstract interpretation, it can analyse software and generate the prototype of the signature of the new application. It does simple type

steep
Signature based type analyzer

typeprof
Also works as LSP server (LSP?). To provide as code completion.

- Comprehensive Checks (typeprof/steep)
- Works as Documentation (LSP)
- Better IDE Support (typeprof/LSP)


Benefits of static typing, without declaration.
As long-term vision, tech trend comes and goes. Nezt 10-15-20, the other type of programming languages will be popular. Like Pendulum.

"Languages without Type Declaration might become popular."

I want Ruby to be one of those languages, popular in 20 years later.
Nobody knows the Future. We don't know what will come.
I foresee that type of future for programming languages. Mostly statically typed languages, without definitions, with ability for dynamic programming, with conciseness. I want that to Ruby. I try hard to make it.

I don't want to blame others (PHP/Python), but I want to make the right decision - in 15/20 years.
"Trust my forecast ;)"

Static is faster.
Doesn't have to be slow.
V*: Chromes JS VM - Is fast, because it uses runtime information and. Faster than most VM.
Vm doesn't require type declarartoin to be fast.
JIT using Runtime Type Information. The runtime information is the priority. When someone declares something is array of something, they are array of array of symbols. In static, that should be Array of Objects (because you have strings/symbols).
Runtime knows what it is ().
Using that information, runtime can be faster than statically typed.

JIT with YJIT in Rust.
YJIT for ARM64. The previous compiler (JIT), the wider team, sponsed by Shopify,
Now we have 2 JIT compilers, YJIT/MJIT.

What's new in Ruby 3.2. We're about to release 3.2 in Christmas.
Ruby on WASM (web assembly).
We can run full ruby, full featured ruby in browser.

Memory allocation improvement
MaNy (N:M threading) (N threads/ M threads)
Data objects
syntax_suggest (better array information provider)
error_highlight (the better error messages)

Tools:
- RubyMine
- Solarpgraph
- Rubocop
- Sorbet/Steep

They are provided by the community.

We can do more! If you need help, ask us! The future of the language, productivity of the language, lays with the company. They can improve the productivity of the Ruby language.

We will Keep Moving Forward, providing better tooling, sttic type checkers.
We try to "Create the Better World.". "Together."

Imrpove your productivity

Talk sponsored by
Salesforce, NaCL, GitHub Sposors, Ruby Community.

Thank you




### Questions

What do you think about Sorbet?
They needed it now.
Now, use typeprof.

The big regrets of life. Are there any feature you regret introducing to Ruby?
Some features from Perl. I regret adding threads at the very beginning. At that time had one time CPU. Now we have many cores. That kind of difference problem for the implementation. If we could provide something like Raptor at the beginning. That's what he regrets.

Nice feel of ligevity?
How we support so it thrives for 100 years?
It's difficult for 5 years. The Ruby was beginnging to start with Matz hobby. But now is the effort of the community. Bookkeeping. Adding more power of the community is the key.

A point from type checking and speed. Which area Ruby should be improved?
Ruby to improve in the developer experience, e.g. when using IDEs (VS Code, RubyMine). So tools can do better code comletion and help

What is a aspect of Ruby you currently enjoy working on?
I enjoy blocks?

If ruby didn’t exist, what other language would you pick nowadays?

Is contribution to open-source the key to happinnes?
Social events are happy.
Writing programms for clients vs open source, the latter is much more enjoyable.
Maybe because of the freedom?

My C# colleagues tease me with their Visual Studio debugging capabilities. How long will it take until I can tease them back and how can I help speed this up?

What to expect from Ruby in the future?
Improving performance - always.
Improve the productivity -
Then we can enjoy the programming. We can do tries and errors to enjoy the programming.

"The joy is the most important to Ruby."

# How Music Works (AppSignal)

What we are covering yoday?
https://github.com/thijsc/how_music_works

Waves
Bouncing molecules.
Ear receives vibrates.

Pitch - one sound
Same waveform, but with with difference czestotliwosc

Timbre
One pitch, but adds a bit

Tempo - pitch, but with a pause in between.
Back in the days, music was live.

Edison - invented phonograph. He patented this.

The technology was progressing. 2 world was excellrated progress.


Music in Ruby.
The actual music looks like matehmatical function. 10 milliseconds of sound.

samples.each_slice(1024) - you combine them.

04. Amplification

We want to make it louder (the higher the peaks, the louder the sound)

Amplify the sound - multiple with the ration. If you multiply and get out of the range, you get really distorted sound. Out of the range of the image.

That's how distortion works/

05. Mixing

(taking electrical )

One in a complicated waveform.
We read all files.
And then we sum them up.

06. Compression

Sounds louder but making them less louder.

Compression with a ratio. When you go above the threshhold.

Two steps:
- Identify the peaks
- makeup gain
- compress

07. Making Sounds
Analog synthesisers.
How synthesiers work like?
- Making noise - random numbers - Ruby generated noise. (noise for)
- Square wave - a wave that's square. We're reproducing oscillator in the code ()
- Sine wave - Pure science. So we are calculating the math function.

We combine the samples into chords. Chords are different sine waves.

The next step is Fourier transform. All waves can be recreated by combining multiple waves.

08. Timbre

Not quite done!

### Questions
How do you sidechain your kicks to your bass?

Are there any common misconceptions about audio or music that annoy you?
The actual real musicians it's esoteric thing. But it's simple math.

Can we play with vocals with Ruby?
Yes.

How are overtones created and/or visualized?
Overtone - that creates a little tone above the usual one.

How would you apply attack/release time to your compressor?
Attack/release check if things are over the threshold?

How would you write tests for that?
(laughter)

# Mel Kaulfuss - Applying SRE Principles CI/CD (Buildkite)

She Flew the furthest (25 hours). She is Australian.

First line in Ruby, RailsGirls, 2015.

## Notes
Overview:
- Issues

Story
Part 1 - The Drama
There's always drama in the software
- Monolith
- Gargantial
- micro_services

It's not about the destination, people you meet along the way.

I prepare the changes and I merged it.
My build failed.
Test failed.
Test is not related to the change I made.

"I like boring deploys."

Failing test? Run it again.
"Oh that? That never worked."

How long users spend hitting retry.
Users in Buildkite:
- 9413 days clicking the button
- 1 day ->

[flaky tests]

Part 2 - The Recovery
SRE - Site Reliability Engineering.
Began at Google.
Book - Site eliability Engineering by google. It's a lizard.

SRE is part of Devops.

DevOps principles:
- Remove silos
- Understand accidents are normal
- Embrace gradual change
- Understand Tooling & Culture are interrelated (Human systems are important to a good system)
- Measurement is critical to success

SRE principles:
- work towards automating or eliminating repetition (especially when it )
- System deisgn with a bias toward availability, latency & efficiency
- Observability
- Avoid more reliabilty more strickly than necessary

Defining what is "necessary" fir the company.

"One does not simply 100% reliability"

"Feeks real bad! But is it really real bad?"

Part 3 - The Future
"it is difficulty to do your job well wthout clearly defining well."

SLOs/SLIs/Error Budgets

SLI - Service Level Indicator
Service Level Objective - defines an acceptable level of unreliability
Error Budget -

Stop being reactive and start being proactive.

Get together and start building a picture.
#TO DO [questions]

" What is the system?
- from the picture

Error Budget = 1 - your SLO

Exapmle SLO/SLI/EB

SLO
Test suite reliability should be greater than 87%

SLI
Test Suite reliability

Error Budget
77 x test runs:
- Reliability score < 87%
- In a 4 week period

You can use buildkite metrics to use any CI/CD you want.

We have access to metrics.

- TL;DR;
  - start using metrics for your tests
  - So it's okay to have failing pipeline **wWITHIN** the error budget
  - test suite reliability so low


"SLOs are powerful weapon to wield against micromanagers, meddlers, etc."

### Questions
How do you differentiate between tests that fail because the code is wrong and flaky tests and other infrastructure problems?
It was usually the work.

You mentioned CI “reliability score”. How do you define that score?

###
(Great vibe, she made us feel "welcome" in he presentation, great sense of humour, slow pace but with a lot of "details")


# Jemma Issroff - Implementing Object Shapes in CRuby (Shopify)

## Takes
- Concept of the Shape as the way to improve the performance of the Ruby language
-
## Draft notes
She was working on Implementing Object Shapes in CRuby (with).

1. What are object shapes?
2. How are object shapes implemented?

(Ruby Object) "shapes".
shapes - name of this technique. There from the SmallTalk.

Shape - represents object's properties (e.g. instance variables).
Ruby is a dynamic programming language, that's why the shape will change.

#TODO [post image]

Post class with two attributes.

User (name)

Admin - same properties.

Two objects can have the same shape.

(when we create)

Root shape:
- ID: 0
- ivars: []

Shape #1:
ID: 1
ivars: [@title]

Shape #2:
ID: 2
ivars: [@title, :@author]


**Two instances of the same class can have different shapes.**

So it's like a path.

"It's a tree".
Shape of an object transitions with new properties (frozen status).

_frozen_ creates a shape.

2. How are object shapes implemented?

How do we identify the shapes?
Shape IDs.

How many shapes can we have?
Ruby runs on 64 bit machines. Use 32 bits for shape IDs (4.2 bullion shapes).

32 bit machines - Use 16 bits for shape IDs (65k shapes)

RailsBench: ~10k shapes.
Shopify monolith: ~40k shapes.

What information is encoded within a shape?
In C
```c
struct rb_shape {
  struct rb_id_table * edges // - values are the shape IDs
  //
  attr_index_t iv_conut // how many instance variables this shape has
  unint type // (root shape, ivar shape - they took instance transition, frozen shape - always leaf nodes, no more transitions, undef shape - two ivar transitions. it's)
  shape_id // shape ID
}
```

undef_shape

```ruby
class Post
attr_accessor :title
end

first_post = Post.new
```

What are the benefits of object shapes?
1. Increased cache hits
2. Decreased code complexity
3. Beneficial for JITs
4. Performance

1. Increased cache hits

Changed caching on instance variables reads
How it works in Ruby 3.1?

How variable is set?
Each instance has it's own instance variable array.
Each class has the table.

Name Index
@title 0
@author 1

first_post instance variable
id variable
0  "a"
1 "b"

hash lookup to do the variable.

Class is cache key.
@title - Post: Index 0
@author - Post: Index 1

```ruby
first_post = Post.new
class FrontPagePost < Post; end
```

With how the objects change.
We get rid of the map variable name <->

So we remove the map and use variables_count, and we use shape ID as the cache key.

Shape ID is cache Key.

index is iv_count - 1

Increased cache hits!

2. Decreased code complexity

2.1 Reduced frozen checks in ivar.

Check if object is frozen.

By definition, if the object is frozen, it cannot be cached.

2.2. Removed undef sets in object allocations

Object -> Instance variables.
`obj.instance_variable_set(:@a, "a")`

`obj.instance_variables #=? [:@a]`
`undef != nil`

`undef != nil`

Object.new - Performance and complexity cost of setting undefs.

We have "undef" shape. We're iterating up the tree. We don't need to pre-populate.

3. Beneficial for JIT

YJIT Generated Assembly
Instance variable get.

With object shapes - Fewer instructions, comparisons and memory reads

4. Performance

1. RailsBench
Shapes is faster, and more

2. Microbenchmarks
[comparison]

Shapes is faster in some other.
vm_ivar_init_subclass

class B < A

b.set_ivars
c.set_ivars

Note: The cases when we set the subclass and use the same.

@Jemmalssroff
RubyConf Mini
WNB.rb


# Security Doesn’t Have To Be a Nightmare - Wiktoria Dlach
## Takes
- CIA Triad - Cofidentiality, Interference, Availability
- Think about security faster in the development loop
- DAST/SAST - Dynamic application security testing and Static application security testing

## Draft notes
Low hanging fruits:
### Sanitize the input
### Validate the data
No credentials in your repo - but for testing is okay... no, it's not okay.
Then you add a new another resource,

### Let the machines work for you
DAST/SAST
You can get instant feedback if you integrate the tool.

Something that blew her mind. It will spark fire in your mind.
There is no "one" security.
There is so much, that it can be too overwhelming.
3-5 acronyms per day.

There is an infinte amount of threats but...
all of them can be assoigned to 1 of 3 categories.

1. Confidentiality
2. Interference
3. Availability

The CIA Triad

Confidentiality:
- Who can see this resource?


Integrity:
- Who can create. Update and remove a resource?
- Is there a way to see a malicious actor deleting all resources?


Availability:
- is this endpoint rate-limited?
- What happens when external product is down?
- How much time does a database migration take?

### Shift Security Left
When you look at the software process (6 phases) - shift the security to the left.

Move fast and break things is over.

## Questions
How do you apply the CIA triad to a big and old codebase?

How do I remove credentials from the git history of an active project with about a dozen people currently working on it? Send help.
Huge effort - you have to have consensus. Then you choose the correct provider for the secret provider. Then you move away from these credentials.

Decetify(DAST)
Polaris (SAST)
