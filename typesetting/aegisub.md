# Aegisub & Other Tools

### Tools

The first thing you'll need to do is make sure your tools are in order.
Typesetters will need more tools than most other roles in fansubbing and
they need to be configured properly. 

Here is a list of tools you will want to download:

  - [Aegisub](http://www.aegisub.org)
      - It is **highly** recommended to use line0's builds, which can be
        found [here](https://files.line0.eu/builds/Aegisub/). They
        include a preinstalled automation script package manager built
        by fansubbers called Dependency Control and several *critical*
        fixes to Aegisub that have not been merged into the official
        application.
  - A font manager. 
      - Not all font managers are equal. Choose the one that works the
        best for you. Some important features might include:
          - Performance with large font libraries.
          - Add fonts from folders, not just installed fonts.
          - Activate fonts for use without installing
          - Organize fonts in a meaningful way
          - Works on your OS
      - Free Options
          - [Nexusfont](http://www.xiles.net)
          - [FontBase](http://fontba.se)
      - Paid (Note: can be found free on *certain
            websites)*
          - [MainType](http://www.high-logic.com/font-manager/maintype.html)
          - [Suitcase
            Fusion](https://www.extensis.com/products/font-management/suitcase-fusion/)
  - [Mocha Pro standalone
    app](https://www.imagineersystems.com/products/mocha-pro/)
      - Look for it on *certain websites*.
      - On Windows, Mocha **requires**
        [Quicktime](https://support.apple.com/kb/DL837?locale=en_US)to
        be installed. More information can be found
        [here](http://www.imagineersystems.com/support/support-faq/#quicktime-on-windows).
  - [x264 binary](https://download.videolan.org/x264/binaries/)
      - Download the latest **8-bit** binary for your platform.
      - For example: x264-r2851-ba24899.exe
        **not** x264-10b-r2851-ba24899.exe
      - 32 bit builds on Windows may be more stable.
  - [Adobe Photoshop and
    Illustrator](http://www.adobe.com/creativecloud.html)
      - Look for it on *certain websites*.
      - Alternatively, free software like
        [Gimp](https://www.gimp.org)and
        [Inkscape](https://inkscape.org/en/)may be used in some
        circumstances.

### Configuring Aegisub

For now, just change your settings to reflect the following. If you've
made any changes previously for another fansub role, be careful not to
overwrite those. When in doubt, ask someone with Aegisub experience.
Settings can be accessed via *View \> Options* or with the hotkey *Alt +
O*.

[![aegisub64\_2017-09-08\_01-50-08.png](images/cnvimage100.png)](http://34.201.151.95/uploads/images/gallery/2017-09-Sep/aegisub64_2017-09-08_01-50-08.png)

[![aegisub64\_2017-09-08\_01-54-35.png](images/cnvimage101.png)](http://34.201.151.95/uploads/images/gallery/2017-09-Sep/aegisub64_2017-09-08_01-54-35.png)

[![aegisub64\_2017-09-08\_01-54-59.png](images/cnvimage102.png)](http://34.201.151.95/uploads/images/gallery/2017-09-Sep/aegisub64_2017-09-08_01-54-59.png)

The Advanced \> Video options include two particularly important
settings.

1.  "Force BT.601" Checkbox. This option is enabled by default. For
    fansubbing, ***this is bad***. At least it is in most cases. If you
    want a more in depth explanation of color matrices and how these two
    are different, you can read up
    [here](http://blog.maxofs2d.net/post/148346073513/bt601-vs-bt709),
    but the gist of it is this: BT.601 is for Standard Definition video
    and BT.709 is for High Definition video. Opening a .ass file in
    Aegisub with the default set to BT.601 could *irreversibly ruin the
    colors of any typesetting, dialogue, or kfx already in the script*.
    Even worse, some video renderers will read this setting from the
    muxed subtitles and render the video to match it. So
    please, *please*,* **please*** change it now. 
    1.  If you are working on a DVD or something in Standard Definition,
        you can change this to BT.601 manually in File \> Script
        Properties. 
        1.  Not all Standard Definition video will be BT.601, so when in
            doubt, ask the encoder or check
            [MediaInfo](https://mediaarea.net/en/MediaInfo)if they are
            not available.
        2.  You will almost always want to use TV.601 and not PC.601.
            Once again, if in doubt, ask the encoder.
    2.  It's also recommended that before you start working on a script,
        check that the color matrices are correct in File \> Script
        Properties. 
        1.  You will almost always want to use TV.709 and not PC.709.
            Once again, if in doubt, ask the encoder or
            check [MediaInfo ](https://mediaarea.net/en/MediaInfo)if
            they are not
    available.
    [![aegisub64\_2017-09-08\_02-12-08.png](images/cnvimage103.png)](http://34.201.151.95/uploads/images/gallery/2017-09-Sep/aegisub64_2017-09-08_02-12-08.png)

The "Subtitles Provider". 

1.  Just a few years ago, there was a pretty clear consensus on which
    subtitle renderer to use for anime and softsubs. These days, not so
    much.
2.  It used to be that
    [VSFilter ](https://sourceforge.net/projects/guliverkli/files/VSFilter/)was
    the best renderer around and was the only supported renderer by most
    fansub groups.
3.  However, it was eventually replaced
    with [xy-vsfilter](https://forum.doom9.org/showthread.php?t=168282) and
    then that was replaced
    with [xySubFilter](https://forum.doom9.org/showthread.php?t=168282)
    because VSFilter and xy-vs filter were not keeping up with the
    demands of subtitles.
4.  By 2015, however, xySubFilter development had come to a halt and
    since then, [libass](https://github.com/libass/libass)has made many
    improvements both in speed and compatibility with advanced
    subtitling in part due to contributions from members of the fansub
    community. 
5.  At the end of the day, which renderer you choose is up to you, but
    we recommend libass. It is maintained, cross-platform, can handle
    most typesetting, and has been integrated in to many commercial and
    open source software products. If you prefer, however, stock Aegisub
    ships with VSFIlter and line0's builds come with xy-vsfilter.

#### Hotkeys

As you develop your skills more and begin to integrate automation
scripts into your workflow, you will probably want to consider adding
hotkeys to cut down on time navigating menus. These can be accessed via
*Interface \> Hotkeys *in Aegisub's Options menu. We'll let you decide
on those yourself, however, and move on for now.