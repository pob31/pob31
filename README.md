# Pierre-Olivier Boulant

Freelance theatre sound and video engineer. The software here is my experience of
running shows, written down as code. Since late 2025 I have been writing it with
Claude, Anthropic's AI model, so these projects also show how I learned to work that
way: first a port, then a project from scratch, then a full show controller, with
quick prototypes alongside.

## Three projects, one progression

### [WFS-DIY](https://github.com/pob31/WFS-DIY): porting (November 2025 to October 2026)

A Wave Field Synthesis processor for sound reinforcement, ported to C++ and JUCE from
my Max/MSP version ([wfs-diy.net](https://wfs-diy.net)). This was my first project
with Claude, and the guidance was light at first: the architecture notes, the PRD and
the code audits were added along the way. It now has WFS and reverb renderers on the
GPU (CUDA, HIP and Metal), binaural monitoring with head tracking, DAW plugins, an MCP
server and nine interface languages. It premiered on 29 September 2026 with
Arthur Nauzyciel's [*Scènes de la vie conjugale*](https://www.t-n-b.fr/scenes-de-la-vie-conjugale) at the Théâtre National de Bretagne
in Rennes. It does everything I wanted it to do, and it is close to its final 1.0
release.

*1,391 commits · ~208,000 lines of C++ · v1.0 beta 64, nearing release*

**What it taught me:** what a model does when it is left to fill in the gaps.

### [S21_HiJack](https://github.com/pob31/S21_HiJack): starting from scratch (February to June 2026)

Middleware for DiGiCo's S21 and S31 consoles. It adds what the desk does not have:
snapshots and a cue list with fades and one-level undo, macros, channel palettes,
ganging, personal monitor mixes on phones and in a browser, and links to QLab and
Go.dot. I wrote a 650-line JUCE prototype by hand in 2021. In 2026 I rewrote it from
scratch in Rust with Claude, in a few one-week rounds, with a plan, phases and audits. It is due to premiere on 15 December 2026 with
[*Coup Fatal*](https://www.comedie.ch/fr/coup-fatal-2026) at the Comédie de Genève.

*445 commits · ~94,000 lines of Rust, plus Kotlin and Swift monitor apps · v0.3.1*

**What it taught me:** how to set up a project from nothing so that the model can
carry it.

### [Go.dot](https://github.com/pob31/go.dot): show control (August to October 2026)

A show controller for theatre, dance and live music. It runs a cue list of sound and
video, holds live bindings during a show, and conducts WFS-DIY and S21_HiJack. The
specification is law: twelve constraints that come from running shows, an owner for
every decision, agents reviewing agents' work, and tests in two languages on three
operating systems.

*Two months · 1,182 commits · ~645,000 lines, 247,000 of them tests · Windows, macOS
and Linux.* Its Android remote,
[go.dot-remote](https://github.com/pob31/go.dot-remote), is another 24,000 lines of
Kotlin written in ten days.

**What it taught me:** what show experience and that method can do together, on
newer models. The full story is in
[How Go.dot was built](https://github.com/pob31/go.dot/blob/main/docs/how-go-dot-was-built.md).

## Prototypes

Not everything needs that method. Some tools start as quick builds with little or no
specification, where the process itself is simple and the work is adjusting it until
it holds up against reality.

### [Choufleur](https://github.com/pob31/choufleur_prompt): a script GPS for technicians (August 2026)

It listens to the actors' microphones, follows the play in the script with offline
speech recognition, and nudges each operator before their cues. It never triggers
anything itself. It is still a prototype, but it has already followed two full
performances of *Hécube, pas Hécube* at the Comédie-Française, end to end, against
the operator's own script.

*209 commits · ~33,000 lines of Rust and Python, mostly written in one month*

## Also here

- [spatcore](https://github.com/pob31/spatcore): the common base of my spatial sound processors
- [XOA](https://github.com/pob31/XOA): a tenth-order Ambisonics processor (under construction)
- [Tight-WFS](https://github.com/pob31/Tight-WFS): WFS for dense loudspeaker arrays
- [WFS-DIY-Android-Remote](https://github.com/pob31/WFS-DIY-Android-Remote): touch control for WFS-DIY
- [headtracker_v1](https://github.com/pob31/headtracker_v1): a head tracker for binaural listening
- [Le_Pixophone](https://github.com/pob31/Le_Pixophone): a video performance from still pictures and a live camera, ported from Pure Data

---

Line counts measure volume, not value. What counts is what has run in front of an
audience: WFS-DIY and Choufleur have, S21_HiJack will in December, and Go.dot is on
its way.
