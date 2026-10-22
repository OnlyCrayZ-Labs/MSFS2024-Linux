# Installation status — experimental milestone

A reproducible installation from a clean checkout has not been validated.
There is no supported installer or public runtime binary for this milestone.
The successful CachyOS flight used a preserved private checkpoint; it does not
establish that the proposed sanitized source revisions reproduce that runtime.

You must own a legitimate Microsoft Store / Xbox PC game license and supply
your own authorized installation and account. This project is independent of
Microsoft and Asobo. It supplies no game packages, proprietary SDKs, license
material or cloud-save synchronization.

## Required validation before an installation guide is released

1. Publish and record exact approved Xodus, Proton, Wine and xgameruntime commits;
   verify all recursive submodules can be fetched anonymously.
2. Record CachyOS version, GPU/driver, build packages and pinned toolchain/SDK
   versions. Rebuild Xodus and the entire modified Wine/Proton runtime in a
   disposable environment from those source commits.
3. Document authorized game acquisition separately from compatibility setup;
   validate required redistributables and their distribution terms.
4. Create a new test prefix and local save directory, with documented runtime,
   service configuration and manual launch steps. Keep account data private.
5. Validate authentication, setup, a flight and normal restart/local save restore;
   record exact results and failures. Xbox cloud sync remains unimplemented.

Until these steps pass, README build commands are developer starting points,
not a working end-user installation recipe. Preserve working prefixes and saves;
never replace a known working runtime while testing this experimental source.
