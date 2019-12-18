# PaddedTipDates

BEAST2 package that contains operators that having padding to avoid creating negative branches and can change ancestral node dates if needed.

## Installation

1. Download the GitHub repository.

2. Unzip dist/PaddedTipDates.addon.zip into your BEAST2 library folder given below based on your operating system / version of BEAST2.

  * MACOS: ~/Library/Application Support/BEAST/2.X
  * Linux: ~/.beast/2.X

3. Run BEAUTi2.

4. Close BEAUTi2.

## Usage

To use the padded or recursive tip date operators in the this package first create a BEAST2 XML file with Tip Date sampling.

Then edit the XML in a text editor:

1. In the first line of the XML file replace either

  * `required=""` with `required="TipDates v1.0.1"`
  * `required="SomePackages"` with `required="TipDates v1.0.1:SomePackages"`
   
2. Replace each instance of `TipDatesRandomWalker` with either `TipDatesRandomWalkerPadded` or `TipDatesRandomWalkerRecursive`.
  
  * In the same line you can add `Padding="SomeNumber"` to change the padding to SomeNumber (default is 1e-4).
  * For TipDatesRandomWalkerRecursive, you can also add `depthPenalty="SomeNumber"` to add set a penalty for increased depth (default is 0).
