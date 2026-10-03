# Changelog

All notable changes to Opsis are recorded here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Opsis on mobile

### Fixed

- On a link with `?graphs=`, selecting a class or a graph no longer overloads
  some stores

## [0.3.0] – 2026-10-03

### Added

- **show all** to reveal the full Class list
- `?graphs=` to restrict every count, list and entity pane to a subset of named grapphs
- **copy as VoID** to copy a scoped link's graphs as a VoID description
- `?dates=off` to leave out the date column and the date sort
- **show 200 more** under an entity pane's links

### Changed

- A class or graph you click now shows as selected right away
- The entity pane now shows a statement's named graph only under **Linked from**
- The entity pane's summary now counts the links to the entity among its facts,
  and the graphs those links come from

### Fixed

- The vocabulary shown beside a class name is now right for DBpedia, vCard and
  other common vocabularies, which read `ontology` or `ns`
- The date sort no longer fails on stores that refused the query
- The entity pane now shows facts on stores without named graphs
- The entity pane now lists each of the entity's own facts once, even when it is
  in several named graphs

## [0.2.0] – 2026-09-25

### Added

- Pinned classes. Hover over a class and click the pin to put it at the top
  of the Class list, where it keeps its count under any filter. Drag pinned
  classes, or press Alt+↑ and Alt+↓, to change their order. Your pins are
  saved in your browser.
- The classes you list as `cfg:pinnedClasses` in the settings appear pinned
  for everyone who opens the graph. **Copy as Turtle** gives you your own pins
  in that form, and **reset** goes back to the list in the settings.

## [0.1.0] – 2026-09-23

First public release. 

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

[Unreleased]: https://github.com/kvistgaard/opsis/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/kvistgaard/opsis/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/kvistgaard/opsis/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/kvistgaard/opsis/releases/tag/v0.1.0
