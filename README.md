homebrew-mplayer2
=================

This is my fork of pigoz's mplayer2 formule, whitout install python3, because i'm using pythonbrew.

Usage
-----

 *  make sure you have Homebrew 0.9
 *  `brew tap twlz0ne/mplayer2`
 *  `ln -s ~/.pythonbrew/pythons/Python-3.3.0 /usr/local/Cellar/Python-3.3.0`

To install with FFmpeg (default):
 *  `brew install --HEAD twlz0ne/mplayer2/mplayer2`

If you want to use libav instead of FFmpeg:
 *  `brew install --HEAD twlz0ne/mplayer2/libav`: since brew will error out on
    mplayer2's installation because libav is a head only formula. Just
    install it manually.
 *  `brew install --HEAD twlz0ne/mplayer2/mplayer2 --with-libav`

To update the tapped formulae from this repository use `brew update`.

Why is FFmpeg default?
----------------------

mplayer2 is currently not compatible with audio using planar sample formats
which libav uses: this results in broken ALAC support. FFmpeg also has a Video
Decode Acceleration (VDA) decoder that mplayer2 can use for accelerating h264
decoding.

Available formulas
------------------

 *  libav: official libav HEAD
 *  mplayer2: official mplayer2 HEAD
