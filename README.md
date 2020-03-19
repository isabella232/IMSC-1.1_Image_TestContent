# IMSC-1.1_Image_TestContent

This repository is forked from https://github.com/FoxMediaServices/IMSC-1.1_Image_TestContent with the intent to increase the reach of the materials provided, per https://www.w3.org/2019/02/21-tt-minutes.html#item07

This reel is is for IMSC 1.1 Image based subtitle testing. The items that are tested are all pertinent to subtitles produced for production content. This has been built to help manufacturers with their IMSC 1.1 Image implementations by providing them with a reference IMSC package.

This test content consists of the following assets:

- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20](IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_HLG_Backplate.mxf](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_HLG_Backplate.mxf)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_HLG_CompositedProxy.mov](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_HLG_CompositedProxy.mov)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_Backplate.mxf](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec709_Backplate.mxf)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_CompositedProxy.mov](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec709_CompositedProxy.mov)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec709_Backplate.mxf](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_Backplate.mxf)
- [IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec709_CompositedProxy.mov](http://media.w3.org/2020/03/IMSC1-1_IMAGE_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_CompositedProxy.mov)

The IMSC XML file is to be rendered over the Backplate ProRes HQ file. If the IMSC decoding is accurate, it will look exactly the same as the Composited Proxy file. There is a Rec 709 backplate and proxy, a Rec 2020 PQ backplate and proxy, and an HLG backplate and proxy. The recommended approach for compositing sRGB subtitles to rec 709, rec 2020 PQ, and HLG is:

    sRGB (EOTF 2.2) to 709 (EOTF 2.4)
    Map the sRGB values from an EOTF of 2.2 to an EOTF of 2.4

    sRGB (EOTF 2.2) to PQ 2020 Narrow Range (EOTF PQ)
    Map the sRGB values to PQ 2020 as described in section Q.1 of the Draft TTML2 Recommendation

    sRGB (EOTF 2.0) to HLG Full Range
    Map the sRGB values to PQ 2020 as described in section Q.2 of the Draft TTML2 Recommendation

The IMSC 1.1 XML file includes in-line comments which describes the purpose of each test.

The backplate includes the following:

- Frame counter and Media Time counter
- Grid with lines every 5%
- Yellow crosses at each corner of the text
- Sync counter at the beginning and end of each event
