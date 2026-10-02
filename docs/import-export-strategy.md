# Import/export strategy

## Native project format

The app should maintain a native project file designed for the product itself rather than a direct mirror of another tool's packet structure.

The native format should support:

- prop and group definitions
- visual layout and channel mapping
- song sections and timing data
- effect objects at the user-meaningful level
- preview metadata and warnings
- compatibility notes from imported files

The format should be explicit, versioned, and editable by design. It should not be a hidden binary dump of a vendor-dependent implementation.

## xLights import

xLights compatibility is an important product goal, but it is treated as import compatibility only.

The app should support a defined subset of data, such as:

- prop groups and channel assignments
- basic layout metadata
- common sequences or effect structures that can be reasonably approximated
- timing section and song-level information

The importer should avoid blindly translating all vendor-specific semantics. Instead, it should map imported content into the product's native model and convert unsupported or ambiguous logic into explicit warnings.

## LOR future import

LOR support should be planned later, after the project has established a stable native model and a reliable xLights import path.

The strategy is:

- first ship a focused xLights import path
- validate the native data model with real-world residential workflows
- only then explore LOR import support in a separate, clearly scoped later phase

This order reduces risk and keeps the product aligned with the initial target user.

## FSEQ export

FSEQ export is a central compatibility feature for the app.

This export path should generate a sequence file that is compatible with downstream playback or rendering tools, while preserving the product's own semantics through a deliberate translation layer.

The export process should:

- convert the user-authored sequence into a rendered or discretized timeline
- emit FSEQ in a standards-based, tool-friendly format
- flag any content that could not be faithfully represented in the export

## Unsupported feature handling

The app should teach users about unsupported or approximate content through a structured status model.

Recommended categories:

- native/editable
  Content created and preserved in the app's native project model. The user can edit it directly.

- approximate
  Content imported from another format that is translated into a similar effect or structure, but not a perfect match.

- baked
  Content that has been converted into a final rendered form and is no longer easily editable in a semantic way.

- unsupported
  A feature or effect that cannot be represented by the app's current model and must be handled as a warning or fallback.

- ignored
  A feature present in an imported file that is intentionally not imported because it is outside the product's current scope or is not relevant to the residential workflow.

## User-facing import warnings

The importer should show a clear summary for every import:

- what succeeded
- what was mapped approximately
- what was ignored
- what remains unsupported
- what the user should review before export

This keeps the product honest and avoids hidden mismatches between the imported file and the user's understanding of the sequence.

## Design principle

Import/export should never be a reason to knowingly copy another tool's code or behavior. It should be a transparent interoperability layer with clear, user-visible tradeoffs.
