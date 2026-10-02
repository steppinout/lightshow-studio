# Architecture

## Direction

The product should be structured as a desktop-first application with a clear separation between layout editing, sequencing logic, preview/rendering, and export functions.

The preferred architecture for initial planning is:

- Tauri for desktop shell and native packaging
- React + TypeScript for the user interface
- Rust for the desktop backend and core project logic

This is a good default because it offers a strong balance between a modern desktop experience, local-first performance, and a safer boundary between UI and the sequencing engine.

However, the stack is not final. The design should remain flexible enough to adopt another desktop framework or a different backend if the product requirements evolve.

## Proposed high-level structure

### UI layer

The UI should focus on tasks rather than raw technical controls.

Likely responsibilities:

- project management and layout editor
- timeline and song section overview
- prop/group selection and naming
- effect editing panels and presets
- preview window and playback controls
- AI suggestions panel and review workflow
- import/export status and warning surfaces

### Core application layer

This layer handles project data and sequencing semantics.

Likely responsibilities:

- project model
- layout model and channel mapping
- sequencing timeline and effect objects
- playback state and rendering requests
- AI prompt orchestration and editing review
- validation and warnings for unsupported features

### Backend and system layer

The backend is responsible for local resource management and export operations.

Likely responsibilities:

- native project serialization
- render jobs for preview or exported sequences
- FSEQ export and compatibility conversion
- import parsing for supported formats
- file I/O and project validation

## Data model direction

The project format should be explicit and human-maintainable.

A native project model may include:

- project metadata
- layout definition
- groups and props
- channels and mapping metadata
- timeline sections and beats
- effects and scenes
- imported compatibility metadata
- warnings and status for approximations

The model should support a distinction between user-authored native content and converted compatibility data. This is important for future import/export and for transparent handling of unsupported features.

## Why desktop-first

A desktop app offers important benefits:

- local file projects and local previews
- better performance for interactive timeline editing
- straightforward handling of large sequencing files
- native desktop interactions for layout editing and project management

The app should be optimized for a local workstation environment rather than assuming a browser-only or cloud-first workflow.

## Architectural principles

- separate the layout model from the effect model
- keep the user-facing sequencing language intuitive and not tied to raw vendor syntax
- surface compatibility warnings early and clearly
- design export logic as a deliberate conversion layer rather than a direct embed of vendor formats
- keep the app modular enough to support AI features later without making them the core of the first version

## Decision status

The team may use Tauri + React + Rust for the first implementation plan, but the architecture should be revalidated against actual product needs and technical constraints before coding begins.
