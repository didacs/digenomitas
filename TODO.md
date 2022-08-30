## Technical Debt

The following is a list of items that could improve the state of the code:

1. In the source `digenom/src/main/scala/com/editasmedicine.digenome/IdentifyCutSites.scala`,
   extract the logic in `IdentifyCutSites.CutSiteAccumulator.accumulate` to check for clipped
   sequences on the 5' end of the read to enable unit testing of just this section.
