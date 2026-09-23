# techseed

Terms used when showing a client how industrial data is organised in a Unified Namespace.

## Language

**UNS**:
A Unified Namespace: one hierarchical topic tree (for example `enterprise/site/area/line/cell/tag`) where all plant data is published and found.
_Avoid_: namespace, topic tree (when meaning the whole UNS)

**Level**:
One named tier of the UNS hierarchy, by default the ISA-95 tiers Enterprise, Site, Area, Line and Cell.
_Avoid_: layer, depth

**Tag**:
A single data point at a leaf of the UNS, such as a temperature or a counter.
_Avoid_: signal, datapoint, topic

**Topic path**:
The full slash-separated address of a node in the UNS, from the enterprise down to the node itself. The same tag has a different topic path in each alternative.
_Avoid_: tag path, address, key

**Alternative**:
One named arrangement of the same set of tags into a UNS hierarchy. Alternatives differ in the order or granularity of their levels, not in which tags they contain.
_Avoid_: variant, version, option
