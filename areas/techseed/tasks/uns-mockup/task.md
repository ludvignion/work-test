# Visual mock-up for UNS structures

Area: techseed
Created: 2026-09-23

## Ask
A colleague finds it hard to show the client the consequences of different UNS structures in a neat and simple way. The UNS follows a simple tree structure, but it is difficult to get an overview of. The goal is a visual mock-up that shows a UNS structure and can also present alternative UNS structures, so the colleague can use it with the client. Two options are being considered: a horizontal tree that looks more like an information model, where hovering over a box shows its metadata, or a graph component.

Input: fake data only.
Output: a visual mock-up of a UNS structure that can present alternatives for it.
Constraints: it is a mock-up, so it uses fake data only. The look and feel should be premium and modern, like Runway, Warp or Cohere.

## Spec
Purpose: a colleague presents this live to a client to show how different UNS alternatives change where data lives and how it is reached.
Done looks like:
- The HTML file opens offline and shows the tree view of the ISA-95 alternative.
- Hovering over any box shows name, level, topic path, data type, unit, source system, update rate, and child count.
- Switching alternatives morphs the view, and a pinned tag's topic path updates visibly.
- The side panel shows depth, node count, average children per node, and the wildcard match count for each alternative.
- The tree/graph toggle works in all 3 alternatives.
- The dark/light toggle works, and text is readable in both themes.
- The Artifact link opens the same page.
Decided:
- stated: UNS means a Unified Namespace with ISA-95 levels (Enterprise, Site, Area, Line, Cell) and tags as leaves.
- stated: alternatives use the same set of tags and differ only in the order or depth of their levels; they are named and shown one at a time.
- stated: 3 alternatives: ISA-95 strict, functional-first, and flat.
- stated: the colleague presents the mock-up live, so it needs no onboarding text.
- stated: both a horizontal tree view and a graph view, with a toggle.
- stated: the graph view has parent-child edges only, with nodes sized by the number of tags under them.
- stated: switching alternatives animates the nodes from one arrangement to the other, in a single pane.
- stated: the consequences shown are a pinned tag's topic path (main effect), plus a side panel with shape metrics (depth, node count, average children per node) and what one wildcard subscription matches.
- stated: fake data is medium sized: 1 site, 3 to 4 areas, 2 lines each, about 80 to 120 tags.
- stated: hover shows name, level, topic path, data type, unit, source system, update rate, and child count for non-tag nodes.
- stated: look and feel follow the reference file uns-explorer-web-interface.html (paper ground, ink text, one green accent, IBM Plex Sans and Mono); this replaces the earlier Runway, Warp and Cohere direction.
- stated: light theme by default, with a dark toggle (changed 2026-09-25 from dark by default); UI text in English; the header uses the neutral name "UNS Explorer" and no company or client names.
- stated: delivered as one self-contained HTML file in outputs/, also published as an Artifact.
- assumed: the fake plant is a dairy (food and beverage), because no client industry was given.
- assumed: clicking a tag pins it and keeps its topic path highlighted through the morph, because that is how a tag's changing path becomes visible.
- assumed: libraries are inlined in the HTML file and nothing loads from a CDN, because the file must open offline in the meeting.
Out of scope:
- Real client data or any connection to a live broker or MQTT server.
- Editing or creating UNS structures in the UI.
- Side-by-side comparison of alternatives.
- More than one site.
- Company or client branding.

## Result
<written by /daily-work:record>

## Caveats
<written by /daily-work:record>
