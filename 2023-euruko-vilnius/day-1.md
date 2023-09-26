# Steven Baker - Reflections on a Reluctant Revolution -Keynote

Uncle Bob told him to release the tool.

Describer, Describr.
"Specification, not verification."
RSpec - released in 2005

Jim Wireck?
"I love rspec, and I want to use it in flexmack".
Brian Marick/Martin Fowler
Why people use it in production - I still don't.
I thought that was just test.
"Not on my list."
> 75% choose rspec as default - I still don't know why.
Minitest Mock.
He took credit for creating rspec.
It was a teaching tool.
David Chelimsky (lead maintainer for a decade).
Ward Cunningham.
I emailed them and said "what's up".
"The rspec wouldn't exist if not Ruby".

"Create. Share. Repeat."
@srbaker



# Carla - No passwords no problems.

@CarlaStabile
webauthn
passkeys

passwords

authentication factos:
- knowledge  - something you know
- possesion - something you have
- inherence - something you are

WebAuthn - Web Authentication API
browser-based API that allows servers to register and authenticate users using public-key cryptography

Devise <-> Browser: CTAP2
Browser <-> Server: WebAuthn
FIDO2 (Fido allience)

`navigtor.credentials.create`
`navigtor.credentials.get`

browser-based => JS
webauthn (ruby gem) (WebAuthn Relying Party)
transports (usb/ble/nfc)

passkeys: synced or device-bound
webauthn.me
passkeys.dev



# Hiroshi Shibata - How resolve Gem dependencies in your code?

Hiroshi - ANDPAD
RubyKaigi - Okinawa - May 2024

What's dependency resolution?

RubyGems is a package manager of the Ruby language.
rubygems.org - host of gems

gemspec - file defines config, which is then crated to Gem::Specification class.

Gem.loaded_specs - shows Gem::Specification class
Gem::Specification#dependencies - method that define parts of your application.

### Default gemds
Default gems  - stdgems.org


### Resolving dependencies
Resolution
Resolver Engine
Resolver

Bundler.setup and Bundler.require are most important parts of Bunlder (defind in runtime.rb)



# Unconference Part 1

## Adrian Marin
@adrianthedev

Avo -

## Chikahiro Tokoro - Generate anonymised database with MasKING
2. setup replica and database trigger
3. Proxy connection and interrupt SQL on the fly
4. Read database and create anonymised database (through database client)


/kibitan/masking -> MySQL/MariaDB

## Sinatra
Rack is used inside

(HTMX)

## Johny Shields - Ruby Threads and so can you
TableCheck
(Cybergizer)

Producer - Consumer Pattern

Multi-Stage Pattern
(FTP to Amazon S3)
