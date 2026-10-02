# Roadmap

## Phase 0: planning/specs

Goal: define the product, constraints, and technical direction before implementation.

Deliverables:

- product charter and clean-room policy
- architecture direction and technical assumptions
- import/export compatibility strategy
- research notes and audit summary
- initial project requirements and open design questions

## Phase 1: layout builder prototype

Goal: create the first layout-oriented editing workflow.

Deliverables:

- prop/group editor
- basic layout canvas for residential props
- channel mapping and naming tools
- project serialization for a native format
- lightweight validation of layout completeness

## Phase 2: layout-first manual sequencing

Goal: enable users to sequence a show with the layout in view.

Deliverables:

- timeline for song sections and beats
- manual effect placement by prop or group
- simple palette and state tools for colors, fades, and accents
- basic playback preview for selected groups
- scene and cue editing for common residential sequences

## Phase 3: preview/render/FSEQ export

Goal: validate the show and produce a compatible output.

Deliverables:

- preview rendering for layout and motion
- playback controls and zoomable timeline
- FSEQ export pipeline
- export validation and warnings for unsupported behavior
- initial native project file versioning and compatibility checks

## Phase 4: AI-assisted sequencing

Goal: add an editable co-sequencer experience without making AI the sole creative engine.

Deliverables:

- user-selected prop/group/time-range analysis
- AI effect proposals based on mood, energy, beat, and song structure
- editing workflow for accept/revise/reject proposals
- suggestions for common visual idioms rather than low-level effect dumps
- instruction tuning focused on residential sequencing needs

## Phase 5: xLights import, then LOR import later

Goal: expand compatibility while keeping the product independent and clean-room compliant.

Deliverables:

- xLights import support for a focused subset of projects and data
- user-visible import warnings for approximations or unsupported content
- native project compatibility mapping for migrated sequences
- later LOR import exploration once xLights path is mature
- structured import audit and pass/fail reporting

## Release posture

The roadmap is intentionally staged to favor product clarity over broad feature breadth. The first major product milestone is not a general-purpose sequencer; it is a fast, intentionally limited tool for residential pixel shows that helps new users get to a polished result quickly.
