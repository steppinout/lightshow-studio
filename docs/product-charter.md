# Product charter

## Target user

Lightshow Studio is aimed at residential light show creators who want a fast, friendly, layout-driven way to build pixel shows without prior expertise in advanced sequencing tools.

Primary users include:

- homeowners building a Christmas or seasonal display
- hobbyists with a modest or moderate pixel layout
- small show builders who want to sequence multiple props and zones quickly
- users who want better visual planning before a show is exported

These users are often motivated by speed, simplicity, and results. They usually care more about rhythm, mood, and visually pleasing outputs than about deep low-level effect parameter tuning.

## Product principles

1. Layout first
   Users should begin by mapping their props and channels. Sequencing should be anchored to actual physical elements, not abstract channels alone.

2. Fast path for everyday motion and color effects
   Most real residential sequences are built from straightforward visual states: on, off, fade, wash, accent, pulse, and simple motion. The software must make these easy and fast.

3. New-user friendly
   The app should emphasize guided tasks, simple vocabulary, and low cognitive load. Advanced controls should exist, but should not dominate the default experience.

4. AI as co-sequencer
   AI should support ideation and editing inside a user-directed workflow, rather than replacing creative decisions or making invisible, low-level parameter changes.

5. Compatibility without copying
   Import/export code should be independently written and documented. Compatibility is an interoperability goal, not a reason to replicate GPL-licensed code or assets.

6. Good preview and validation
   Users should be able to preview the sequence in context and catch obvious issues before export.

## MVP

The first product milestone should focus on a limited but useful workflow:

- create a project and define props or groups
- build a layout with a simple visual editor for residential props
- create timeline-based sequence data for simple effect groups
- preview the sequence in a basic, local playback view
- export FSEQ without requiring a full rendering pipeline
- support simple AI-assisted effect suggestions for chosen time ranges or groups

The MVP goal is not maximum realism or full control. It is to demonstrate that the product can be fast, understandable, and visually compelling for everyday show creators.

## Explicit non-goals

The initial product should not try to be all of the following:

- a wholesale clone of xLights or another sequencer's feature model
- a complete GPL-compatible implementation of all effects from other tools
- a full general-purpose video editor or VJ system
- a tool that exposes raw low-level effect parameter manipulation as the default user experience
- a system that depends on copying other products' assets, UI text, or code
- a full MIDI or DMX console replacement in the first version

## Success criteria

The product is successful when users can do the following quickly and confidently:

- define a prop layout for a residential display
- build a simple song-based sequence without reading a manual
- apply common home-grown effect patterns that match the real needs of holiday shows
- preview the behavior in a visual timeline and playback view
- export to a compatible format for playback or rendering

## Scope statement

This project is intentionally scoped to residential pixel shows and a layout-first workflow. It is not a general-purpose theatre lighting package or a direct reimplementation of existing show-control ecosystems.
