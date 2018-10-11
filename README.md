# LOCL Test

LOCL Test (LOCL &#x30C6;&#x30B9;&#x30C8; is its Japanese name) is a special-purpose OpenType/CFF font that is intended to be used to test the extent to which applications and other text-handling environments support the '[locl](https://www.microsoft.com/typography/otspec/features_ko.htm#locl)' (*Localized Forms*) GSUB feature and language tagging, in terms of supporting common East Asian languages, specifically Japanese, Korean, Simplified Chinese, Traditional Chinese for Taiwan, and Traditional Chinese for Hong Kong SAR.

* The glyph set includes the mandatory *.notdef* glyph at CID+0, along with a *space* (U+0020) glyph at CID+1.

* CIDs 2 through 6 are digraphs that correspond to the regions that use the five supports languages: "JP" for Japan, "KR" for South Korean (ROK), "CN" for China (PRC), "TW" for Taiwan (ROC), and "HK" for Hong Kong SAR. Only the digraph "JP" is encoded, and is double-mapped from "J" (U+004A) and "j" (U+006A). Accessing the digraphs that correspond to the other four regions requires 'locl' GSUB feature support and language tagging.

* CIDs 7 through 11 are region-specific glyphs of the CJK Unified Ideograph U+904D (&#x904D;), and only that for Japan (JP) is encoded. Accessing the glyphs that correspond to the other four regions requires 'locl' GSUB feature support and language tagging.

The image below shows how the provided *locl-test.html* file should display when opened in a browser (the glyphs for Hong Kong SAR are colored red because that is a current pain point for some apps):

![alt text](https://raw.githubusercontent.com/adobe-fonts/locl-test/master/resources/locl-example.jpg "img-View")

The Format 14 '[cmap](https://www.microsoft.com/typography/otspec/cmap.htm)' subtable specifies (unregistered) [PanCJKV](https://github.com/adobe-type-tools/pancjkv-ivd-collection/) IVSes for a total of 11 regions. The image below shows how the second line of text in the provided *uvs-test.html* file should display when opened in a browser (the glyph for Hong Kong SAR is colored red because that is a current pain point for some apps):

![alt text](https://raw.githubusercontent.com/adobe-fonts/locl-test/master/resources/uvs-example.jpg "img-View")

The glyphs that are used in this font are derived from the Regular weight of [Source Han Sans](https://github.com/adobe-fonts/source-han-sans/).

## Font installation instructions

* [macOS](https://support.apple.com/en-us/HT201749)
* [Windows](https://www.microsoft.com/en-us/Typography/TrueTypeInstall.aspx)
* [Linux/Unix-based systems](https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116)

## Building the font from source

### Requirements

To build the binary font file from source, you need to have installed the [Adobe Font Development Kit for OpenType](https://github.com/adobe-type-tools/afdko/) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF font, and the COMMANDS.txt file provides the command lines that are used.

## Getting Involved

Send suggestions for changes to the LOCL Test project maintainer, [Dr. Ken Lunde](mailto:lunde@adobe.com?subject=[GitHub]%20LOCL%20Test), for consideration.
