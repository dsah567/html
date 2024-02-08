## figure

```html
<figure>
    <img src="dnr.jpg" alt="The head  of a dinosauskeleton" width="400" height="341" />
    <img src="favicon.png" alt="favicon imagetitle="image" width="800" height="341" />
    <figcaption>
      A T-Rex on display in the ManchesteUniversity Museum.
    </figcaption>
</figure>
```
video tag

```html
 <video src="rabbit320.mp4" controls>
    <p> alt details if video tag dose not work</p>
  </video>

  <video controls
  width="400"
  height="400"
  autoplay
  loop
  muted
  preload="auto"
  poster="poster.png">
    <source src="rabbit320.mp4" type="video/mp4" />
    <source src="rabbit320.webm" type="video/webm" />
    <p>
      Your browser doesn't support this video. Here is a
      <a href="rabbit320.mp4">link to the video</a> instead.
    </p>
  </video>
```
audio tag has also simalar attribute

```html
<video controls>
  <source src="example.mp4" type="video/mp4" />
  <source src="example.webm" type="video/webm" />
  <track kind="subtitles" src="subtitles_es.vtt" srclang="es" label="Spanish" />
</video>
```
WebVTT is a format for writing text files containing multiple strings of text along with metadata such as the time in the video at which each text string should be displayed, and even limited styling/positioning information. These text strings are called cues, and there are several kinds of cues which are used for different purposes. The most common cues are:

subtitles
Translations of foreign material, for people who don't understand the words spoken in the audio.

captions
Synchronized transcriptions of dialog or descriptions of significant sounds, to let people who can't hear the audio understand what is going on.

timed descriptions
Text which should be spoken by the media player in order to describe important visuals to blind or otherwise visually impaired users.

A typical WebVTT file will look something like this:

```webvtt
1
00:00:22.230 --> 00:00:24.606
This is the first subtitle.

2
00:00:30.739 --> 00:00:34.074
This is the second.
```
To get this displayed along with the HTML media playback, you need to:

- Save it as a .vtt file in a sensible place.
- Link to the .vtt file with the \<track> element. \<track> should be placed within \<audio> or \<video>, but after all \<source> elements. Use the kind attribute to specify whether the cues are subtitles, captions, or descriptions. Further, use srclang to tell the browser what language you have written the subtitles in. Finally, add label to help readers identify the language they are searching for.

