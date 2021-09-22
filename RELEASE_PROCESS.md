# RELEASE PROCESS

This document contains all the necessary information about my release process. This process is used by my current teams and would be something I would look to integrate into future  teams if possible.

### Code Freeze

A "code freeze" will be applied a few days before the release. This means that **NOTHING** will be added to the release branch.

A "code freeze" ends once the release is published.

## Release Types

**Note:** More about versioning can be found in the [VERSIONING file](./VERSIONING.md).

Releases can come in different flavors. Here's a list with the most common release types and how they're treated.

### Minor / Major Release

The minor / major release is a planned release which includes all the changes added since the last minor / major release (including bugfixes). The user should pick up the latest minor / major release only when API clients are coded to look for it.

The minor / major releases is released at a pre-defined time.

#### Versioning / Tagging

Assuming our current version is `v1.0.0`.

The minor release would be `v1.1.0`. The major release would be `v2.0.0`.

### Patch release

Patch releases should **only** include critical bug fixes and released ASAP. The user should pick up the latest patch release automatically when talking to our API.

#### Versioning / Tagging

Assuming our current version is `v1.0.0`.

The patch release would be `v1.0.1`.

### Alpha Release

Alpha releases are created to have a sneak peek into the upcoming feature set of the new release. They're also used for pre-release QA / internal usage.

Alpha releases are not scheduled and can be pushed multiple times throughout a development phase.

Alpha releases should never be installed automatically when the user connects to our API. The user should be forced to explicitly name the alpha release when connecting to our API`).

#### Versioning / Tagging

Assuming our current version is `v1.0.0`.

The alpha release would be `v1.0.0-alpha.1`. A subsequent alpha release would be `v1.0.0-alpha.2` etc.