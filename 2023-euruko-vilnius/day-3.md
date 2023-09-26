# Hana Harencarova - Seamless Releases with Feature Flags: Insights from GitHub's Experience - Keynote
@hanaharencar


GitHub uses flipper

How to test feature flags:
- tests for both FF on and off
- Local/Codespaces testing
- CI (all feature flags on)
- Review lab testing
- Testing in canary during the deploy


Shipping is happenning gradually (team/private beta/public beta/dark-shipping)

Observability of the feature flags - custom logs for the features.

Default setup - a new way to enable GitHub code scanning.

### Feature flags at scale.
In Github, they were used in:
- Monolith
- Microservices
- Caching
- Preloading

Performance:
- Caching (memcache)

Tens of thousand
Too many calls to featurue flags.

Big features
Features that you need to enable for many users.

Flipper has the concept of Gates.

For big features, they don't cache feature flags for individual users, to limit the number of requests (and memory cached).


# City Pitches
### Tuzla
### Copenhagen
### Manchester
### Verona
### Warsaw
### Helsinki
### Kyiv
Ruby Meditation


### Verona
### Copenhagen
### Helsinki
### Manchester
### Tuzla
### Warsaw

# Matias
MATIAS KORHONEN
“Doing terrible things with ruby.wasm"

WASI
Web assembly

# Tom de Bruijn - Crafting elegant code with Ruby DSLs
What is a DSL?
Domain Specific Language
Domains: Getter & setter domain, gem domain

Are DSL good?
Make reading and writing code easier

Puma has the DSL class.

