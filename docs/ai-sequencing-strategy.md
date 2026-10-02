# AI sequencing strategy

## AI as a co-sequencer

AI in Lightshow Studio should assist the user, not replace the user.

The system should help the user create and refine effects based on musical context, prop selection, and the user's creative goals. It should propose effect ideas, not silently generate a final sequence without review.

The design principle is: the user selects the area, and the AI proposes a set of editable, understandable sequence ideas.

## Example workflow

A user does the following:

- selects a prop or group
- chooses a time range in the song
- identifies the section mood or energy level
- optionally picks a color direction or visual theme

The AI then suggests:

- accent flashes
- on/off states
- fades or washes
- motion patterns such as ripple or sweep
- simple color transitions driven by the song's mood or energy

The proposal should be presented as a set of candidate effect concepts, each with the ability to review, revise, accept, or reject them.

## What the AI should not do

The AI should not:

- directly produce raw low-level xLights parameter dumps as the main workflow
- hide the creative choices behind an opaque one-click effect black box
- generate effects without context of the user's selected prop or section
- replace the user's understanding of layout and timing

## Musical awareness

The AI should understand the song at a high level, including:

- section segmentation
- beat and phrase structure
- energy changes
- mood or intensity shifts
- likely transitions between euphoric, calm, fast, and dramatic moments

This should inform the suggested effect direction without forcing the user into an overly technical or low-level interface.

## User-level abstraction

The app should speak in user-friendly terms, such as:

- color wash
- accent pulse
- slow ramp
- sparkle burst
- directional sweep
- fade to mood

The AI should work at that level, not at the raw parameter level of a vendor tool. The user sees a readable proposal for an effect concept rather than a stack of obscure commands.

## Reviewability

Every AI-generated suggestion should be editable after acceptance.

The user must be able to:

- adjust timing
- change colors
- tune intensity
- revise the selected prop or group
- choose between alternative proposals
- manually override the result without restarting from scratch

This keeps the AI in the role of a creative assistant rather than a hidden automation system.
