# Lightshow Studio

Lightshow Studio is a desktop sequencing tool for residential pixel light shows. It is built for people who want to create cheerful, polished shows without learning a full professional-grade lighting workstation.

The product starts from the layout: the user first defines their props, channels, and arrangement of the home or property. Then they sequence the show around that layout instead of around a raw spreadsheet of channels or an unfamiliar effect library.

This is meant to feel approachable to a new user who may be decorating a house, planning a Christmas display, or building a seasonal rhythm show. The workflow is intentionally simple: build the layout, arrange timing by song sections, add visual effects, preview the result, and export a compatible file for playback.

## Current status

This repository is an initial product charter and planning repo. It establishes the clean-room direction for the product and documents the first architecture, strategy, and research notes.

At this stage, there is no application scaffold, no dependencies, and no generated package files. The goal is to define the product direction clearly before implementation begins.

## High-level goals

- Make basic visual sequencing fast and intuitive for residential pixel displays
- Start with a layout-first workflow that matches how users think about their property
- Support AI-assisted sequencing as a co-sequencer, not a black-box replacement for the user
- Maintain compatibility with common ecosystem formats through independently written import/export code
- Keep the app focused on new users first, while leaving room for more advanced workflows later

## Product positioning

Lightshow Studio is designed for homeowners, hobbyists, and small show builders who want:

- a cleaner project layout than a spreadsheet-like effect editor
- strong visual previews before export
- fast editing for common effects such as color washes, chases, pulses, accent flashes, and motion patterns
- a guided experience that reduces the intimidation of sequencing software

## Compatibility note

This project is designed for compatibility with xLights and FSEQ workflows as import/export features only. Any compatibility code is expected to be written independently without copying xLights source code, assets, or GPL-licensed material.

## Repository intent

This repository contains the product charter, roadmap, strategy, research notes, and clean-room compliance guidance. It is not a source dump from another sequencer or a derivative of xLights/LOR code.

## Next milestones

The project will evolve through a staged roadmap:

- Phase 0: planning and specs
- Phase 1: layout builder prototype
- Phase 2: layout-first manual sequencing
- Phase 3: preview/render/FSEQ export
- Phase 4: AI-assisted sequencing
- Phase 5: xLights import, then LOR import later

See the docs folder for detailed product, technical, and research planning.
