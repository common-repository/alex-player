=== Alex Player ===
Contributors: iamzhirik
Donate link: http://alex.zhyrytovskyi.x10.name/
Tags: audio player, mp3 player, wavesurfer, radio
Requires at least: 4.3
Tested up to: 6.6.2
Stable tag: 4.3
Requires PHP: 5.3.13
License: GPLv3 or later
License URI: https://www.gnu.org/licenses/gpl-3.0.html

Alex Player is simple audio player designed to play local audio files or radio streams on your website.

== Description ==

This audio player is designed to play local audio files or radio streams on your website. It has 6 components: media player, wavesurfer, waveform visualization, equalizer, circular spectrum and play button.

== Screenshots ==

1. /screenshot-1.png
1. /screenshot-2.png
1. /screenshot-3.png
1. /screenshot-4.png

== Live Demo ==

[View live demo here](http://alex.player.x10.name/)

== Installation ==

To install this plugin you need to do the following:

1. Upload the plugin files to the `/wp-content/plugins/plugin-name` directory, or install the plugin through the WordPress plugins screen directly
1. Activate the plugin through the 'Plugins' screen in WordPress
1. Insert shortcodes into the text of your post, list of the shortcodes provided below.

== Shortcodes ==

Media player shortcode:

	[UIMediaPlayer file="/demo.mp3" color="#c0c0c0" width="600"]

Wavesurfer shortcode:

	[UIWaveSurfer file="/demo.mp3" color="#4fcb1d" color2="#8b8b8b"]

[More shortcode examples](http://alex.player.x10.name/)
	
== Frequently Asked Questions ==

After I modify the shortcode it stopped working, why?
When you modify the text the wordpress editor could insert invisible markup. To remove that markup you can copy the shortcode to notepad, and than copy it back from notepad to wordpress editor.

Why this player does not play media file from remote url?
Due to web browser security policy it does not allow to read and process audio which located on remote host. The exception are files where "Access-Control-Allow-Origin: *" is present, such files can be played remotely.

Why do I hear small sound artifacts in Chrome?
It appers only if you playing audio on "http", but on "https" everything works fine. The reason is that modern web browser audio processing features works only with "https", and if you are using "http" then player using older sound processing mechanism which is deprecated.

== Thanks to the authors ==

* Milenko Mitrovic for the [DC-DSP Filter](https://www.dsp-worx.de/?n=4) - most of digital signal processing algorithms was reused from DC-DSP Filter.
* Ryan Geiss for the [Geiss plugin](https://www.geisswerks.com/geiss/) - the minimal version of Geiss was ported into this project as fullscreen audio visualization.

== Changelog ==

= 1.37 =
* Changed: Equalizer right now automatically adjust amplitude of the volume, and amplifier has ability to overload
* Fixed: Visualization for equalizer was boosted with the wrong data
* Fixed: Playback engine was reworked a little

= 1.36 =
* Added: "Geiss" visualization was partially converted from C++ to Javascript and set as audio screensaver
* Fixed: Lowpass filter turned off on 1.00
* Fixed: Change of the volume with no media loaded produced an error in console of web browser
* Fixed: After audio completed if we press play button than it will play audio from the beginning
* Fixed: Radio right now could play through AudioWorklet api, cause old audio processing API could produce sound artifacts

= 1.35 =
* Added: New engine based on AudioWorklet technology, whuch works only on https
* Added: Ability to reorder items inside playlist using drag&drop

= 1.34 =
* Fixed: Equalizer presets popup was not appear with jQuery v3.5.1

= 1.33 =
* Added: Ability to fix media player to the corner of the window
* Fixed: Radio shortcode was reworked, old shortcode is supported but not ducumented any more

= 1.32 =
* Added: Playlist partial implementation

= 1.31 =
* Fixed: Audio screensaver reworked
* Fixed: Visualizations behind the page visible area will not eat processor time

= 1.30 =
* Added: Player can work with or without jQuery
* Added: Optional download selection button inside wavesurfer
* Fixed: Wavesurfer scrollbar becomes transparent

= 1.29 =
* Fixed: Playback engine reworked
* Added: Radio support

= 1.28 =
* Added: Added ability to set channels count for Wavesurfer

= 1.27 =
* Fixed: First screensaver reworked

= 1.26 =
* Added: First screensaver

= 1.25 =
* Added: Equalizer becomes free component

= 1.24 =
* Added: Equalizer can load previous values after page refresh

= 1.23 =
* Added: Wavesurfer selection color change ability
* Added: Ability to download selected area inside Wavesurfer in WAV or MP3 format

= 1.22 =
* Added: Wordpress 5.5 support

= 1.21 =
* Added: Added ability to hide play button for media player and wavesurfer

= 1.20 =
* Added: Spectrum visualization on top of media player

= 1.19 =
* Added: Only one instance at a time can play right now, all the other instances will be paused
* Added: Wavesurfer selection

= 1.18 =
* Added: Local video playback ability

= 1.17 =
* Added: Ability to play url streams

= 1.16 =
* Fixed: Equalizer multiple instance support
* Added: Looped playback option

= 1.15 =
* Fixed: On small audio files wavesurfer stops not on the end of file

= 1.14 =
* Fixed: Volume change does not slow down the performance
* Added: Bars visualization for media player
* Added: Equalizer

= 1.13 =
* Fixed: z-index bug for circular spectrum
* Fixed: Player now works on iOS

= 1.12 =
* Improved: Wavesurfer time line updates more smoothly
* Added: Ability to play remote URLs which are not blocked by CORS

= 1.11 =
* Fixed: Waveform visualization on wide screens

= 1.10 =
* Added: Circular spectrum component
* Added: Play button component

= 1.09 =
* Fixed: Real time visualization right now works immediately
* Fixed: Waveform right now displays global audio from all media players inside the page

= 1.08 =
* Fixed: All the components with same file name will be connected together
* Added: For the big audio files it takes long time for wavesurfer to load visual data, this problem solved by adding one more file near current mp3 file that already has cached visual data

= 1.07 =
* Fixed width bug

= 1.05, 1.06 =
* Initial release for Wordpress