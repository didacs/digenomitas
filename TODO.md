## Future Improvments

The following is a list of items that could be improved for use with integrases:

1. When the read starts with clipping (sequencing order), be more permissive about matching.  For example:
  - Allow for some reasonable rate of mismatches or fraction matching
  - Allow for the read to start up to `maxClippedLengthDifferences` _into_ the expected sequence (e.g. if shearing or other processes nibbled away a few bases)
  - Allow the read to have up to `maxClippedLengthDifferences` _extra_ bases at the start (e.g. what if end-repair or A-base addition added in a base or two)


## Technical Debt

The following is a list of items that could improve the state of the code:

1. In the source `digenom/src/main/scala/com/editasmedicine.digenome/IdentifyCutSites.scala`,
   extract the logic in `IdentifyCutSites.CutSiteAccumulator.accumulate` to check for clipped
   sequences on the 5' end of the read to enable unit testing of just this section.
