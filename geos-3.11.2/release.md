
2023-03-16

- Fixes/Improvements:
  - GEOSIntersection: Fix FE_INVALID exception on intersection of disjoint geometries
    (GH-791, Joris Van den Bossche & Dan Baston)
  - Fix incorrect result from Envelope::disjoint (GH-791, Dan Baston)
  - Fix handling of odd cases in PolygonHoleJoiner (JTS-946, Paul Ramsey, Martin Davis)
  - Support gcc-13 (GH-743, Sergei Trofimovich)
  - Disallow Inf envelopes in Quadtree, avoid inf loop (Paul Ramsey)
  - GEOSUnaryUnion: Fix crash on collection containing empty point (GH-830, Dan Baston)
  - GEOSSTRtree_iterate: Do not return removed items (GH-833, Dan Baston)
  - IndexedFacetDistance: Fix crash with Inf coordinates (GH-821, Dan Baston)
  - HausdorffDistance: Fix crash on collection containing empty point (GH-840, Dan Baston)
  - MaximumInscribedCircle: Fix infinite loop with non-finite coordinates (GH-843, Dan Baston)
  - DistanceOp: Fix crash on collection containing empty point (GH-842, Dan Baston)
  - Guard against non-finite distances in Buffer/OffsetCurve (GH-661, Paul Ramsey)

