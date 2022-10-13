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

# How Music Works

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

# How Music Works
