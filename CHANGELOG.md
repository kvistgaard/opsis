# Changelog

All notable changes to Opsis are recorded here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Pinned classes. The pin beside a class puts it at the top of the Class list,
  where it keeps its count under any filter. Drag pinned classes, or press
  Alt+↑ and Alt+↓, to reorder them. Your pins stay in the browser, one list
  per endpoint. A store can set pins for every viewer with
  `cfg:pinnedClasses` (nodica vocabulary 0.9.0), and **copy as Turtle** turns
  your pins into that form. **reset** returns to the store's pins.

## [0.1.0] – 2026-09-23

First public release. Opsis was developed inside a personal knowledge graph
project and now stands on its own.

### Added

- Faceted browsing of any SPARQL 1.1 endpoint from one HTML file: class and
  named-graph facets with counts, an entity list, and an entity pane with the
  entity's facts and incoming links.
- Stacked panes, off by default. Press **stack** in the header, or add
  `?panes=stacked` to the URL, and each entity opens beside the one it was
  opened from. Panes scrolled past stay as spines. The open panes are kept in
  the URL as `open=` parameters.
- A Class or Graph section appears only when it offers a choice between groups
  of entities: two values or more, most of them holding more than one entity.
- A copy button beside each IRI in the entity list and the entity pane.
- Settings read from the endpoint: dereference rules in nodica's `cfg:`
  vocabulary open `file:` IRIs in desktop applications, and `dcat:DataService`
  descriptions fill an endpoint picker.
- Search over every string value, through a `/search` sidecar when the
  endpoint offers one and a SPARQL `CONTAINS` scan when it does not.
- A date column sorted by each entity's earliest `xsd:date` or `xsd:dateTime`.
- Queries sent as the form-encoded `query=` field, which public endpoints that
  refuse a bare `application/sparql-query` body accept.
- A note in the status line when the endpoint answers with HTTP 206, cutting
  results short at its time limit.
- A live demo on the Nobel Prize linked data.
- Light and dark themes that follow the system.
- Page metadata: description, licence, Open Graph and schema.org JSON-LD.

[Unreleased]: https://github.com/kvistgaard/opsis/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/kvistgaard/opsis/releases/tag/v0.1.0
