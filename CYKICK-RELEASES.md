# Cykick desktop releases

Cykick is being added to the Desktop distribution channel under
[calliopeai/cykick#53](https://github.com/calliopeai/cykick/issues/53).
This repository owns release assets and discovery; Cykick owns the runtime,
installer, supported platforms and qualification.

Publish stable desktop releases with tags `cykick-v<version>`. Attach the tested
installer/archive assets and a nonempty `SHA256SUMS` file covering those assets.
The existing release workflow adds the product to `latest.json` and the README
version table after publication. Drafts and prereleases are excluded. Before the
first release, no Cykick catalog entry or download row is emitted. Publishing
without an installer/archive and checksums fails the catalog update and retains
the previous catalog; this presence check does not certify the files' contents.

The installer pipeline must independently verify checksums, signing/notarization,
first launch, update, rollback and supported OS/architecture behavior before
publishing. Include exact engine and CLI versions in the release notes. Do not
label a container image, source archive or dashboard shell as a qualified desktop
installer. Native containers remain a separate release channel.

Website download data and Kasm dispatch must be enabled with their tested product
integration. The existing Kasm notifier intentionally ignores `cykick` until
[calliopeai/cykick#54](https://github.com/calliopeai/cykick/issues/54) provides that
image and consumer. No Kasm rebuild is dispatched by this catalog addition.
