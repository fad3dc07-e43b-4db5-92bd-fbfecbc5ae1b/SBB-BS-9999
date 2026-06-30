# sbb-9999-example

This repository represents a governed architectural example.

- The asset code is `sbb-9999-example`.
- The repository is not tied to a specific format or tool.
- Designers can model in ArchiMate or other equivalent design languages.
- `Open Exchange` is the current interchange format, not the repository design language.
- `artifact/source/` holds the editable design source or a working example.
- `artifact/exchange/` holds the versioned interchange artifact.
- The current artifact lives at `artifact/exchange/design.openexchange.xml`.
- Validation runs through a declarative engine centralized in `CALinter`.
- GitHub Actions publishes the validation report after each push.
- The governance repository publishes a rules manifest and the design repo only consumes it.
- The active rule covers Archi/ArchiMate compatibility for `artifact/source/design.archimate`.
- Future versions may add metamodel validation, architecture rules, traceability, semantics, owners, domains, and tag-based versioning.

## Expected Design Scaffold

The design repository is expected to contain at least the following structure:

```txt
/
├── artifact/
│   ├── source/
│   │   └── design.archimate
│   └── exchange/
│       └── design.openexchange.xml
├── README.md
└── .github/
    └── workflows/
        └── ci.yml
```

## Expected Flow

```txt
Architectural asset
→ versioned artifact
→ lightweight local workflow
→ centralized validation
→ controlled Pull Request
→ merge a main
→ version tag
```
