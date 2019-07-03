# matplotlib-crash-course
In this lesson I have taught about Matplotlib. 

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>matplotlib Crash Course </title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">from</span> <span class="nn">numpy.random</span> <span class="k">import</span> <span class="n">randint</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">20</span><span class="p">)</span>
<span class="n">x</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[20]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([ 1.        ,  1.47368421,  1.94736842,  2.42105263,  2.89473684,
        3.36842105,  3.84210526,  4.31578947,  4.78947368,  5.26315789,
        5.73684211,  6.21052632,  6.68421053,  7.15789474,  7.63157895,
        8.10526316,  8.57894737,  9.05263158,  9.52631579, 10.        ])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span> <span class="o">=</span> <span class="n">randint</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mi">20</span><span class="p">)</span>
<span class="n">y</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[8]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([18, 14, 17, 46, 11, 44, 48, 16, 49, 25, 28, 22, 18, 24,  2,  4, 43,
       37, 43, 38])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span><span class="o">.</span><span class="n">size</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[9]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>20</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">dir</span><span class="p">(</span><span class="n">plt</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;Annotation&#39;,
 &#39;Arrow&#39;,
 &#39;Artist&#39;,
 &#39;AutoLocator&#39;,
 &#39;Axes&#39;,
 &#39;Button&#39;,
 &#39;Circle&#39;,
 &#39;Figure&#39;,
 &#39;FigureCanvasBase&#39;,
 &#39;FixedFormatter&#39;,
 &#39;FixedLocator&#39;,
 &#39;FormatStrFormatter&#39;,
 &#39;Formatter&#39;,
 &#39;FuncFormatter&#39;,
 &#39;GridSpec&#39;,
 &#39;IndexLocator&#39;,
 &#39;Line2D&#39;,
 &#39;LinearLocator&#39;,
 &#39;Locator&#39;,
 &#39;LogFormatter&#39;,
 &#39;LogFormatterExponent&#39;,
 &#39;LogFormatterMathtext&#39;,
 &#39;LogLocator&#39;,
 &#39;MaxNLocator&#39;,
 &#39;MultipleLocator&#39;,
 &#39;Normalize&#39;,
 &#39;NullFormatter&#39;,
 &#39;NullLocator&#39;,
 &#39;Number&#39;,
 &#39;PolarAxes&#39;,
 &#39;Polygon&#39;,
 &#39;Rectangle&#39;,
 &#39;ScalarFormatter&#39;,
 &#39;Slider&#39;,
 &#39;Subplot&#39;,
 &#39;SubplotTool&#39;,
 &#39;Text&#39;,
 &#39;TickHelper&#39;,
 &#39;Widget&#39;,
 &#39;_INSTALL_FIG_OBSERVER&#39;,
 &#39;_IP_REGISTERED&#39;,
 &#39;__builtins__&#39;,
 &#39;__cached__&#39;,
 &#39;__doc__&#39;,
 &#39;__file__&#39;,
 &#39;__loader__&#39;,
 &#39;__name__&#39;,
 &#39;__package__&#39;,
 &#39;__spec__&#39;,
 &#39;_auto_draw_if_interactive&#39;,
 &#39;_autogen_docstring&#39;,
 &#39;_backend_mod&#39;,
 &#39;_get_running_interactive_framework&#39;,
 &#39;_interactive_bk&#39;,
 &#39;_log&#39;,
 &#39;_pylab_helpers&#39;,
 &#39;_setp&#39;,
 &#39;_setup_pyplot_info_docstrings&#39;,
 &#39;_show&#39;,
 &#39;_string_to_bool&#39;,
 &#39;acorr&#39;,
 &#39;angle_spectrum&#39;,
 &#39;annotate&#39;,
 &#39;arrow&#39;,
 &#39;autoscale&#39;,
 &#39;autumn&#39;,
 &#39;axes&#39;,
 &#39;axhline&#39;,
 &#39;axhspan&#39;,
 &#39;axis&#39;,
 &#39;axvline&#39;,
 &#39;axvspan&#39;,
 &#39;bar&#39;,
 &#39;barbs&#39;,
 &#39;barh&#39;,
 &#39;bone&#39;,
 &#39;box&#39;,
 &#39;boxplot&#39;,
 &#39;broken_barh&#39;,
 &#39;cla&#39;,
 &#39;clabel&#39;,
 &#39;clf&#39;,
 &#39;clim&#39;,
 &#39;close&#39;,
 &#39;cm&#39;,
 &#39;cohere&#39;,
 &#39;colorbar&#39;,
 &#39;colormaps&#39;,
 &#39;connect&#39;,
 &#39;contour&#39;,
 &#39;contourf&#39;,
 &#39;cool&#39;,
 &#39;copper&#39;,
 &#39;csd&#39;,
 &#39;cycler&#39;,
 &#39;dedent&#39;,
 &#39;delaxes&#39;,
 &#39;deprecated&#39;,
 &#39;disconnect&#39;,
 &#39;docstring&#39;,
 &#39;draw&#39;,
 &#39;draw_all&#39;,
 &#39;draw_if_interactive&#39;,
 &#39;errorbar&#39;,
 &#39;eventplot&#39;,
 &#39;figaspect&#39;,
 &#39;figimage&#39;,
 &#39;figlegend&#39;,
 &#39;fignum_exists&#39;,
 &#39;figtext&#39;,
 &#39;figure&#39;,
 &#39;fill&#39;,
 &#39;fill_between&#39;,
 &#39;fill_betweenx&#39;,
 &#39;findobj&#39;,
 &#39;flag&#39;,
 &#39;gca&#39;,
 &#39;gcf&#39;,
 &#39;gci&#39;,
 &#39;get&#39;,
 &#39;get_backend&#39;,
 &#39;get_cmap&#39;,
 &#39;get_current_fig_manager&#39;,
 &#39;get_figlabels&#39;,
 &#39;get_fignums&#39;,
 &#39;get_plot_commands&#39;,
 &#39;get_scale_docs&#39;,
 &#39;get_scale_names&#39;,
 &#39;getp&#39;,
 &#39;ginput&#39;,
 &#39;gray&#39;,
 &#39;grid&#39;,
 &#39;hexbin&#39;,
 &#39;hist&#39;,
 &#39;hist2d&#39;,
 &#39;hlines&#39;,
 &#39;hot&#39;,
 &#39;hsv&#39;,
 &#39;importlib&#39;,
 &#39;imread&#39;,
 &#39;imsave&#39;,
 &#39;imshow&#39;,
 &#39;inferno&#39;,
 &#39;inspect&#39;,
 &#39;install_repl_displayhook&#39;,
 &#39;interactive&#39;,
 &#39;ioff&#39;,
 &#39;ion&#39;,
 &#39;isinteractive&#39;,
 &#39;jet&#39;,
 &#39;legend&#39;,
 &#39;locator_params&#39;,
 &#39;logging&#39;,
 &#39;loglog&#39;,
 &#39;magma&#39;,
 &#39;magnitude_spectrum&#39;,
 &#39;margins&#39;,
 &#39;matplotlib&#39;,
 &#39;matshow&#39;,
 &#39;minorticks_off&#39;,
 &#39;minorticks_on&#39;,
 &#39;mlab&#39;,
 &#39;new_figure_manager&#39;,
 &#39;nipy_spectral&#39;,
 &#39;np&#39;,
 &#39;pause&#39;,
 &#39;pcolor&#39;,
 &#39;pcolormesh&#39;,
 &#39;phase_spectrum&#39;,
 &#39;pie&#39;,
 &#39;pink&#39;,
 &#39;plasma&#39;,
 &#39;plot&#39;,
 &#39;plot_date&#39;,
 &#39;plotfile&#39;,
 &#39;plotting&#39;,
 &#39;polar&#39;,
 &#39;prism&#39;,
 &#39;psd&#39;,
 &#39;pylab_setup&#39;,
 &#39;quiver&#39;,
 &#39;quiverkey&#39;,
 &#39;rc&#39;,
 &#39;rcParams&#39;,
 &#39;rcParamsDefault&#39;,
 &#39;rcParamsOrig&#39;,
 &#39;rc_context&#39;,
 &#39;rcdefaults&#39;,
 &#39;rcsetup&#39;,
 &#39;re&#39;,
 &#39;register_cmap&#39;,
 &#39;rgrids&#39;,
 &#39;savefig&#39;,
 &#39;sca&#39;,
 &#39;scatter&#39;,
 &#39;sci&#39;,
 &#39;semilogx&#39;,
 &#39;semilogy&#39;,
 &#39;set_cmap&#39;,
 &#39;setp&#39;,
 &#39;show&#39;,
 &#39;silent_list&#39;,
 &#39;specgram&#39;,
 &#39;spring&#39;,
 &#39;spy&#39;,
 &#39;stackplot&#39;,
 &#39;stem&#39;,
 &#39;step&#39;,
 &#39;streamplot&#39;,
 &#39;style&#39;,
 &#39;subplot&#39;,
 &#39;subplot2grid&#39;,
 &#39;subplot_tool&#39;,
 &#39;subplots&#39;,
 &#39;subplots_adjust&#39;,
 &#39;summer&#39;,
 &#39;suptitle&#39;,
 &#39;switch_backend&#39;,
 &#39;sys&#39;,
 &#39;table&#39;,
 &#39;text&#39;,
 &#39;thetagrids&#39;,
 &#39;tick_params&#39;,
 &#39;ticklabel_format&#39;,
 &#39;tight_layout&#39;,
 &#39;time&#39;,
 &#39;title&#39;,
 &#39;tricontour&#39;,
 &#39;tricontourf&#39;,
 &#39;tripcolor&#39;,
 &#39;triplot&#39;,
 &#39;twinx&#39;,
 &#39;twiny&#39;,
 &#39;uninstall_repl_displayhook&#39;,
 &#39;violinplot&#39;,
 &#39;viridis&#39;,
 &#39;vlines&#39;,
 &#39;waitforbuttonpress&#39;,
 &#39;warn_deprecated&#39;,
 &#39;warnings&#39;,
 &#39;winter&#39;,
 &#39;xcorr&#39;,
 &#39;xkcd&#39;,
 &#39;xlabel&#39;,
 &#39;xlim&#39;,
 &#39;xscale&#39;,
 &#39;xticks&#39;,
 &#39;ylabel&#39;,
 &#39;ylim&#39;,
 &#39;yscale&#39;,
 &#39;yticks&#39;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1975e952128&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sort</span><span class="p">(</span><span class="n">y</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[ 2  4 11 14 16 17 18 18 22 24 25 28 37 38 43 43 44 46 48 49]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">sort</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[18]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1975e9df2b0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;g&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;X Axis&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Y&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Random Plot&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[47]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y2</span> <span class="o">=</span> <span class="n">y</span><span class="o">*</span><span class="n">x</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[55]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;ro&#39;</span><span class="p">,</span> <span class="n">markersize</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="s1">&#39;b*&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[55]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197609e37f0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="matlab-vs-matplotlib">matlab vs matplotlib<a class="anchor-link" href="#matlab-vs-matplotlib">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[56]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#objet oriented method </span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[63]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">])</span>

<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;X&#39;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Y&#39;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s1">&#39;Set Title of Random&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[63]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;Set Title of Random&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[64]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">dir</span><span class="p">(</span><span class="n">axes</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[64]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;__class__&#39;,
 &#39;__delattr__&#39;,
 &#39;__dict__&#39;,
 &#39;__dir__&#39;,
 &#39;__doc__&#39;,
 &#39;__eq__&#39;,
 &#39;__format__&#39;,
 &#39;__ge__&#39;,
 &#39;__getattribute__&#39;,
 &#39;__getstate__&#39;,
 &#39;__gt__&#39;,
 &#39;__hash__&#39;,
 &#39;__init__&#39;,
 &#39;__init_subclass__&#39;,
 &#39;__le__&#39;,
 &#39;__lt__&#39;,
 &#39;__module__&#39;,
 &#39;__ne__&#39;,
 &#39;__new__&#39;,
 &#39;__reduce__&#39;,
 &#39;__reduce_ex__&#39;,
 &#39;__repr__&#39;,
 &#39;__setattr__&#39;,
 &#39;__setstate__&#39;,
 &#39;__sizeof__&#39;,
 &#39;__str__&#39;,
 &#39;__subclasshook__&#39;,
 &#39;__weakref__&#39;,
 &#39;_add_text&#39;,
 &#39;_adjustable&#39;,
 &#39;_agg_filter&#39;,
 &#39;_alpha&#39;,
 &#39;_anchor&#39;,
 &#39;_animated&#39;,
 &#39;_aspect&#39;,
 &#39;_autoscaleXon&#39;,
 &#39;_autoscaleYon&#39;,
 &#39;_autotitlepos&#39;,
 &#39;_axes&#39;,
 &#39;_axes_locator&#39;,
 &#39;_axisbelow&#39;,
 &#39;_cachedRenderer&#39;,
 &#39;_clipon&#39;,
 &#39;_clippath&#39;,
 &#39;_connected&#39;,
 &#39;_contains&#39;,
 &#39;_current_image&#39;,
 &#39;_facecolor&#39;,
 &#39;_frameon&#39;,
 &#39;_gci&#39;,
 &#39;_gen_axes_patch&#39;,
 &#39;_gen_axes_spines&#39;,
 &#39;_get_axis_list&#39;,
 &#39;_get_lines&#39;,
 &#39;_get_patches_for_fill&#39;,
 &#39;_get_view&#39;,
 &#39;_gid&#39;,
 &#39;_gridOn&#39;,
 &#39;_hold&#39;,
 &#39;_in_layout&#39;,
 &#39;_init_axis&#39;,
 &#39;_label&#39;,
 &#39;_layoutbox&#39;,
 &#39;_left_title&#39;,
 &#39;_make_twin_axes&#39;,
 &#39;_mouseover&#39;,
 &#39;_mouseover_set&#39;,
 &#39;_navigate&#39;,
 &#39;_navigate_mode&#39;,
 &#39;_oid&#39;,
 &#39;_on_units_changed&#39;,
 &#39;_originalPosition&#39;,
 &#39;_path_effects&#39;,
 &#39;_pcolorargs&#39;,
 &#39;_picker&#39;,
 &#39;_position&#39;,
 &#39;_poslayoutbox&#39;,
 &#39;_process_unit_info&#39;,
 &#39;_prop_order&#39;,
 &#39;_propobservers&#39;,
 &#39;_quiver_units&#39;,
 &#39;_rasterization_zorder&#39;,
 &#39;_rasterized&#39;,
 &#39;_remove_legend&#39;,
 &#39;_remove_method&#39;,
 &#39;_right_title&#39;,
 &#39;_sci&#39;,
 &#39;_set_artist_props&#39;,
 &#39;_set_gc_clip&#39;,
 &#39;_set_lim_and_transforms&#39;,
 &#39;_set_position&#39;,
 &#39;_set_title_offset_trans&#39;,
 &#39;_set_view&#39;,
 &#39;_set_view_from_bbox&#39;,
 &#39;_shared_x_axes&#39;,
 &#39;_shared_y_axes&#39;,
 &#39;_sharex&#39;,
 &#39;_sharey&#39;,
 &#39;_sketch&#39;,
 &#39;_snap&#39;,
 &#39;_stale&#39;,
 &#39;_sticky_edges&#39;,
 &#39;_tight&#39;,
 &#39;_transform&#39;,
 &#39;_transformSet&#39;,
 &#39;_twinned_axes&#39;,
 &#39;_update_image_limits&#39;,
 &#39;_update_line_limits&#39;,
 &#39;_update_patch_limits&#39;,
 &#39;_update_title_position&#39;,
 &#39;_update_transScale&#39;,
 &#39;_url&#39;,
 &#39;_use_sticky_edges&#39;,
 &#39;_validate_converted_limits&#39;,
 &#39;_visible&#39;,
 &#39;_xaxis_transform&#39;,
 &#39;_xcid&#39;,
 &#39;_xmargin&#39;,
 &#39;_yaxis_transform&#39;,
 &#39;_ycid&#39;,
 &#39;_ymargin&#39;,
 &#39;acorr&#39;,
 &#39;add_artist&#39;,
 &#39;add_callback&#39;,
 &#39;add_child_axes&#39;,
 &#39;add_collection&#39;,
 &#39;add_container&#39;,
 &#39;add_image&#39;,
 &#39;add_line&#39;,
 &#39;add_patch&#39;,
 &#39;add_table&#39;,
 &#39;aname&#39;,
 &#39;angle_spectrum&#39;,
 &#39;annotate&#39;,
 &#39;apply_aspect&#39;,
 &#39;arrow&#39;,
 &#39;artists&#39;,
 &#39;autoscale&#39;,
 &#39;autoscale_view&#39;,
 &#39;axes&#39;,
 &#39;axhline&#39;,
 &#39;axhspan&#39;,
 &#39;axis&#39;,
 &#39;axison&#39;,
 &#39;axvline&#39;,
 &#39;axvspan&#39;,
 &#39;bar&#39;,
 &#39;barbs&#39;,
 &#39;barh&#39;,
 &#39;bbox&#39;,
 &#39;boxplot&#39;,
 &#39;broken_barh&#39;,
 &#39;bxp&#39;,
 &#39;callbacks&#39;,
 &#39;can_pan&#39;,
 &#39;can_zoom&#39;,
 &#39;child_axes&#39;,
 &#39;cla&#39;,
 &#39;clabel&#39;,
 &#39;clear&#39;,
 &#39;clipbox&#39;,
 &#39;cohere&#39;,
 &#39;collections&#39;,
 &#39;containers&#39;,
 &#39;contains&#39;,
 &#39;contains_point&#39;,
 &#39;contour&#39;,
 &#39;contourf&#39;,
 &#39;convert_xunits&#39;,
 &#39;convert_yunits&#39;,
 &#39;csd&#39;,
 &#39;dataLim&#39;,
 &#39;drag_pan&#39;,
 &#39;draw&#39;,
 &#39;draw_artist&#39;,
 &#39;end_pan&#39;,
 &#39;errorbar&#39;,
 &#39;eventplot&#39;,
 &#39;eventson&#39;,
 &#39;figure&#39;,
 &#39;fill&#39;,
 &#39;fill_between&#39;,
 &#39;fill_betweenx&#39;,
 &#39;findobj&#39;,
 &#39;fmt_xdata&#39;,
 &#39;fmt_ydata&#39;,
 &#39;format_coord&#39;,
 &#39;format_cursor_data&#39;,
 &#39;format_xdata&#39;,
 &#39;format_ydata&#39;,
 &#39;get_adjustable&#39;,
 &#39;get_agg_filter&#39;,
 &#39;get_alpha&#39;,
 &#39;get_anchor&#39;,
 &#39;get_animated&#39;,
 &#39;get_aspect&#39;,
 &#39;get_autoscale_on&#39;,
 &#39;get_autoscalex_on&#39;,
 &#39;get_autoscaley_on&#39;,
 &#39;get_axes_locator&#39;,
 &#39;get_axisbelow&#39;,
 &#39;get_children&#39;,
 &#39;get_clip_box&#39;,
 &#39;get_clip_on&#39;,
 &#39;get_clip_path&#39;,
 &#39;get_contains&#39;,
 &#39;get_cursor_data&#39;,
 &#39;get_data_ratio&#39;,
 &#39;get_data_ratio_log&#39;,
 &#39;get_default_bbox_extra_artists&#39;,
 &#39;get_facecolor&#39;,
 &#39;get_fc&#39;,
 &#39;get_figure&#39;,
 &#39;get_frame_on&#39;,
 &#39;get_gid&#39;,
 &#39;get_images&#39;,
 &#39;get_in_layout&#39;,
 &#39;get_label&#39;,
 &#39;get_legend&#39;,
 &#39;get_legend_handles_labels&#39;,
 &#39;get_lines&#39;,
 &#39;get_navigate&#39;,
 &#39;get_navigate_mode&#39;,
 &#39;get_path_effects&#39;,
 &#39;get_picker&#39;,
 &#39;get_position&#39;,
 &#39;get_rasterization_zorder&#39;,
 &#39;get_rasterized&#39;,
 &#39;get_renderer_cache&#39;,
 &#39;get_shared_x_axes&#39;,
 &#39;get_shared_y_axes&#39;,
 &#39;get_sketch_params&#39;,
 &#39;get_snap&#39;,
 &#39;get_tightbbox&#39;,
 &#39;get_title&#39;,
 &#39;get_transform&#39;,
 &#39;get_transformed_clip_path_and_affine&#39;,
 &#39;get_url&#39;,
 &#39;get_visible&#39;,
 &#39;get_window_extent&#39;,
 &#39;get_xaxis&#39;,
 &#39;get_xaxis_text1_transform&#39;,
 &#39;get_xaxis_text2_transform&#39;,
 &#39;get_xaxis_transform&#39;,
 &#39;get_xbound&#39;,
 &#39;get_xgridlines&#39;,
 &#39;get_xlabel&#39;,
 &#39;get_xlim&#39;,
 &#39;get_xmajorticklabels&#39;,
 &#39;get_xminorticklabels&#39;,
 &#39;get_xscale&#39;,
 &#39;get_xticklabels&#39;,
 &#39;get_xticklines&#39;,
 &#39;get_xticks&#39;,
 &#39;get_yaxis&#39;,
 &#39;get_yaxis_text1_transform&#39;,
 &#39;get_yaxis_text2_transform&#39;,
 &#39;get_yaxis_transform&#39;,
 &#39;get_ybound&#39;,
 &#39;get_ygridlines&#39;,
 &#39;get_ylabel&#39;,
 &#39;get_ylim&#39;,
 &#39;get_ymajorticklabels&#39;,
 &#39;get_yminorticklabels&#39;,
 &#39;get_yscale&#39;,
 &#39;get_yticklabels&#39;,
 &#39;get_yticklines&#39;,
 &#39;get_yticks&#39;,
 &#39;get_zorder&#39;,
 &#39;grid&#39;,
 &#39;has_data&#39;,
 &#39;have_units&#39;,
 &#39;hexbin&#39;,
 &#39;hist&#39;,
 &#39;hist2d&#39;,
 &#39;hitlist&#39;,
 &#39;hlines&#39;,
 &#39;ignore_existing_data_limits&#39;,
 &#39;images&#39;,
 &#39;imshow&#39;,
 &#39;in_axes&#39;,
 &#39;indicate_inset&#39;,
 &#39;indicate_inset_zoom&#39;,
 &#39;inset_axes&#39;,
 &#39;invert_xaxis&#39;,
 &#39;invert_yaxis&#39;,
 &#39;is_figure_set&#39;,
 &#39;is_transform_set&#39;,
 &#39;legend&#39;,
 &#39;legend_&#39;,
 &#39;lines&#39;,
 &#39;locator_params&#39;,
 &#39;loglog&#39;,
 &#39;magnitude_spectrum&#39;,
 &#39;margins&#39;,
 &#39;matshow&#39;,
 &#39;minorticks_off&#39;,
 &#39;minorticks_on&#39;,
 &#39;mouseover&#39;,
 &#39;mouseover_set&#39;,
 &#39;name&#39;,
 &#39;patch&#39;,
 &#39;patches&#39;,
 &#39;pchanged&#39;,
 &#39;pcolor&#39;,
 &#39;pcolorfast&#39;,
 &#39;pcolormesh&#39;,
 &#39;phase_spectrum&#39;,
 &#39;pick&#39;,
 &#39;pickable&#39;,
 &#39;pie&#39;,
 &#39;plot&#39;,
 &#39;plot_date&#39;,
 &#39;properties&#39;,
 &#39;psd&#39;,
 &#39;quiver&#39;,
 &#39;quiverkey&#39;,
 &#39;redraw_in_frame&#39;,
 &#39;relim&#39;,
 &#39;remove&#39;,
 &#39;remove_callback&#39;,
 &#39;reset_position&#39;,
 &#39;scatter&#39;,
 &#39;semilogx&#39;,
 &#39;semilogy&#39;,
 &#39;set&#39;,
 &#39;set_adjustable&#39;,
 &#39;set_agg_filter&#39;,
 &#39;set_alpha&#39;,
 &#39;set_anchor&#39;,
 &#39;set_animated&#39;,
 &#39;set_aspect&#39;,
 &#39;set_autoscale_on&#39;,
 &#39;set_autoscalex_on&#39;,
 &#39;set_autoscaley_on&#39;,
 &#39;set_axes_locator&#39;,
 &#39;set_axis_off&#39;,
 &#39;set_axis_on&#39;,
 &#39;set_axisbelow&#39;,
 &#39;set_clip_box&#39;,
 &#39;set_clip_on&#39;,
 &#39;set_clip_path&#39;,
 &#39;set_contains&#39;,
 &#39;set_facecolor&#39;,
 &#39;set_fc&#39;,
 &#39;set_figure&#39;,
 &#39;set_frame_on&#39;,
 &#39;set_gid&#39;,
 &#39;set_in_layout&#39;,
 &#39;set_label&#39;,
 &#39;set_navigate&#39;,
 &#39;set_navigate_mode&#39;,
 &#39;set_path_effects&#39;,
 &#39;set_picker&#39;,
 &#39;set_position&#39;,
 &#39;set_prop_cycle&#39;,
 &#39;set_rasterization_zorder&#39;,
 &#39;set_rasterized&#39;,
 &#39;set_sketch_params&#39;,
 &#39;set_snap&#39;,
 &#39;set_title&#39;,
 &#39;set_transform&#39;,
 &#39;set_url&#39;,
 &#39;set_visible&#39;,
 &#39;set_xbound&#39;,
 &#39;set_xlabel&#39;,
 &#39;set_xlim&#39;,
 &#39;set_xmargin&#39;,
 &#39;set_xscale&#39;,
 &#39;set_xticklabels&#39;,
 &#39;set_xticks&#39;,
 &#39;set_ybound&#39;,
 &#39;set_ylabel&#39;,
 &#39;set_ylim&#39;,
 &#39;set_ymargin&#39;,
 &#39;set_yscale&#39;,
 &#39;set_yticklabels&#39;,
 &#39;set_yticks&#39;,
 &#39;set_zorder&#39;,
 &#39;specgram&#39;,
 &#39;spines&#39;,
 &#39;spy&#39;,
 &#39;stackplot&#39;,
 &#39;stale&#39;,
 &#39;stale_callback&#39;,
 &#39;start_pan&#39;,
 &#39;stem&#39;,
 &#39;step&#39;,
 &#39;sticky_edges&#39;,
 &#39;streamplot&#39;,
 &#39;table&#39;,
 &#39;tables&#39;,
 &#39;text&#39;,
 &#39;texts&#39;,
 &#39;tick_params&#39;,
 &#39;ticklabel_format&#39;,
 &#39;title&#39;,
 &#39;titleOffsetTrans&#39;,
 &#39;transAxes&#39;,
 &#39;transData&#39;,
 &#39;transLimits&#39;,
 &#39;transScale&#39;,
 &#39;tricontour&#39;,
 &#39;tricontourf&#39;,
 &#39;tripcolor&#39;,
 &#39;triplot&#39;,
 &#39;twinx&#39;,
 &#39;twiny&#39;,
 &#39;update&#39;,
 &#39;update_datalim&#39;,
 &#39;update_datalim_bounds&#39;,
 &#39;update_from&#39;,
 &#39;use_sticky_edges&#39;,
 &#39;viewLim&#39;,
 &#39;violin&#39;,
 &#39;violinplot&#39;,
 &#39;vlines&#39;,
 &#39;xaxis&#39;,
 &#39;xaxis_date&#39;,
 &#39;xaxis_inverted&#39;,
 &#39;xcorr&#39;,
 &#39;yaxis&#39;,
 &#39;yaxis_date&#39;,
 &#39;yaxis_inverted&#39;,
 &#39;zorder&#39;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[70]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax1</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">])</span>
<span class="n">ax2</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span> <span class="mf">0.6</span><span class="p">,</span> <span class="mf">0.4</span><span class="p">,</span> <span class="mf">0.3</span><span class="p">])</span>


<span class="n">ax1</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;X&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Y&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s1">&#39;Y Plot&#39;</span><span class="p">)</span>

<span class="n">ax2</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="s1">&#39;g&#39;</span><span class="p">)</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;X&#39;</span><span class="p">)</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Y&#39;</span><span class="p">)</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s1">&#39;Y2 Plot&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[70]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;Y2 Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAeMAAAFdCAYAAAAwtwU9AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAIABJREFUeJzt3XmYjeXjx/H3jaEI2RvGVlS2bGMpJdtoR5ZKhMh8SSV9VVq+1a+ytVFCFJGU0DLI0mTJUmgslSWEwQwxZuz7jPv3xzPtyDLn3Gf5vK7LNXOeOXPOZ+aST8/z3Iux1iIiIiLuZHMdQEREJNypjEVERBxTGYuIiDimMhYREXFMZSwiIuKYylhERMQxlbGIAGCMecEY86HrHCLhSGUsEsSMMeONMaP/duxGY0yqMSbyFM8fY4w5bow5aIxJM8bEG2OuPo/3TTTGNLmQ7CLyB5WxSHB7BLjVGBMDYIy5CHgX+K+1dsdpvucVa+0lQBSwCxjjj6AicnoqY5EgZq1NBR4GRhpj8gDPAxuttWPO4nsPAx8BlU/1dWNMM2PMamPMXmPMPGNMhczj44BSwNTMM+wnsujHEQlbKmORIGetnQQsAz4GYoH/nM33GWMuAdoBK07xtSszX+9RoAgwHa98c1pr7wO2AndYay+x1r6SJT+ISBhTGYuEhh5AI+BFa+3Wf3lub2PMXuAX4BKg0ymeczfwpbU23lp7AngNuBi4Lusii8hvcrgOICIXzlq70xizG1h9Fk9/zVr77L88pziw5U+vf9IYsw0ocQExReQ0dGYsIqeyHSj92wNjjAFKAsmZh7Tdm0gWUhmLyKlMBG4zxjQ2xkQA/wWOAd9mfn0ncLmrcCKhRmUsIv9grV0HtAeGALuBO/AGbB3PfEp/4NnMkda9HcUUCRnGWl1tEhERcUlnxiIiIo6pjEVERBxTGYuIiDimMhYREXFMZSwiIuJYUKzAVbhwYVumTBnXMURERM7JsmXLdltri/zb84KijMuUKUNCQoLrGCIiIufEGLPl35+ly9QiIiLOqYxFREQc8+llamNMInAAyADSrbXRxpiCwCdAGSARuMtau8eXOURERAKZP86MG1prq1lrozMf9wFmW2vLA7MzH4uIiIQtF5epmwNjMz8fC7RwkEFERCRg+LqMLfCVMWaZMSY281gxa+0OgMyPRU/1jcaYWGNMgjEmISUlxccxRURE3PH11KZ61trtxpiiQLwx5uez/UZr7UhgJEB0dLS2lhIRkZDl0zNja+32zI+7gM+B2sBOY0wkQObHXb7MICIiEuh8VsbGmDzGmLy/fQ40BVYBU4COmU/rCMT5KoOIiEgw8OVl6mLA58aY397nI2vtTGPM98BEY0wXYCvQxocZREREzp614PWWX/msjK21m4CqpzieCjT21fuKiIicNWth7VqIj/f+JCXBypV+j6EVuCTolSlThq+//tp1DBEJFjt3wvjx0KkTlCwJlSrBo4/C+vVQrx4cO+b3SCpj8Yl27drRuXPnvxz75ptvKFSoEDt27GDs2LHUrFmTfPnyERUVxRNPPEF6evppX88YQ548ebjkkksoUaIEjz32GBkZGeeUad68eURFRZ3XzyMiQezwYZg1C3r3hqpV4bLLoH17mDbNK99334XERK+Mhw6FXLn8HjEodm2S4PPWW29RqVIl4uPjiYmJ4ejRo3Tt2pXXX3+dyMhIDh8+zODBg6lTpw4pKSk0a9aM1157jT59Tr8g2w8//EC5cuX4+eefadCgAVdeeSXdunXz408lIkHh5ElYseKPS88LF8Lx45AzJ1x/PfTvDzExUL06ZAuMc1KVsfhEoUKFGDJkCLGxsaxatYqXX36ZK664gk6dOgHQvXv3359bokQJ2rVrx9y5c8/qta+++mpuuOEGVq1a9Y+vHTt2jCeffJKJEycCcNdddzFw4EDS09O55ZZbOHbsGJdccgkA69evp3jx4hf4k4pIQNiy5Y/ynT0bUlO949dcAw8/7JXvDTdA7txuc56Gylh8pk2bNnzyySe0bduWRYsWsWLFitM+d/78+VSqVOmsXnfNmjUsWLCAvn37/uNrffv2ZfHixaxcuRJjDM2bN+fll1/mpZdeYsaMGbRv356kpKTz/plEJECkp8P06d7l5/h42LDBO168ONx+u1e+TZpAsWJuc54llbH41NChQ7niiivo27cvpUqVOuVz3n//fRISEnjvvffO+Fo1atQge/bsFCxYkAceeID777//H88ZP348Q4YMoWhRb5XV559/nv/85z+89NJLF/7DiIh71sLUqfDUU7BmDeTJAw0aQI8eXgFXqOBkatKFUhmLTxUrVozChQuf9qz3iy++oE+fPnz99dcULlz4jK+1fPlyypUr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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[71]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#plt.subplot()</span>
<span class="c1">#plt.subplots()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[79]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">)</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[79]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197621555c0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[87]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">)</span>
<span class="n">col</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;r&#39;</span><span class="p">,</span> <span class="s1">&#39;g&#39;</span><span class="p">]</span>
<span class="n">data</span> <span class="o">=</span> <span class="p">[</span><span class="n">y</span><span class="p">,</span> <span class="n">y2</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">axes</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">ax</span><span class="p">):</span>
    <span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">],</span> <span class="n">col</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="n">fig</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[110]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">figsize</span> <span class="o">=</span> <span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">),</span> <span class="n">dpi</span> <span class="o">=</span> <span class="mi">100</span><span class="p">)</span>

<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="s1">&#39;y&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="s1">&#39;y*x&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;X&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Y&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s1">&#39;Random Number Plot&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span> <span class="o">=</span> <span class="mi">0</span><span class="p">)</span>
<span class="n">fig</span><span class="o">.</span><span class="n">savefig</span><span class="p">(</span><span class="s1">&#39;random file.png&#39;</span><span class="p">,</span> <span class="n">dpi</span> <span class="o">=</span> <span class="mi">100</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[125]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">markersize</span> <span class="o">=</span> <span class="mi">12</span><span class="p">,</span> <span class="n">linewidth</span> <span class="o">=</span> <span class="mi">3</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;#005425&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[125]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1976225b860&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[136]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="n">figsize</span> <span class="o">=</span> <span class="p">(</span><span class="mi">12</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">)</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="o">**</span><span class="mi">2</span><span class="p">,</span> <span class="s1">&#39;k&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">500</span><span class="p">])</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">)</span>
<span class="n">ax</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">100</span><span class="p">])</span>
<span class="n">ax</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">([</span><span class="mi">1</span> <span class="p">,</span><span class="mi">4</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[136]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(1, 4)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[135]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">dir</span><span class="p">(</span><span class="n">ax</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[135]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;__class__&#39;,
 &#39;__delattr__&#39;,
 &#39;__dict__&#39;,
 &#39;__dir__&#39;,
 &#39;__doc__&#39;,
 &#39;__eq__&#39;,
 &#39;__format__&#39;,
 &#39;__ge__&#39;,
 &#39;__getattribute__&#39;,
 &#39;__getstate__&#39;,
 &#39;__gt__&#39;,
 &#39;__hash__&#39;,
 &#39;__init__&#39;,
 &#39;__init_subclass__&#39;,
 &#39;__le__&#39;,
 &#39;__lt__&#39;,
 &#39;__module__&#39;,
 &#39;__ne__&#39;,
 &#39;__new__&#39;,
 &#39;__reduce__&#39;,
 &#39;__reduce_ex__&#39;,
 &#39;__repr__&#39;,
 &#39;__setattr__&#39;,
 &#39;__setstate__&#39;,
 &#39;__sizeof__&#39;,
 &#39;__str__&#39;,
 &#39;__subclasshook__&#39;,
 &#39;__weakref__&#39;,
 &#39;_add_text&#39;,
 &#39;_adjustable&#39;,
 &#39;_agg_filter&#39;,
 &#39;_alpha&#39;,
 &#39;_anchor&#39;,
 &#39;_animated&#39;,
 &#39;_aspect&#39;,
 &#39;_autoscaleXon&#39;,
 &#39;_autoscaleYon&#39;,
 &#39;_autotitlepos&#39;,
 &#39;_axes&#39;,
 &#39;_axes_class&#39;,
 &#39;_axes_locator&#39;,
 &#39;_axisbelow&#39;,
 &#39;_cachedRenderer&#39;,
 &#39;_clipon&#39;,
 &#39;_clippath&#39;,
 &#39;_connected&#39;,
 &#39;_contains&#39;,
 &#39;_current_image&#39;,
 &#39;_facecolor&#39;,
 &#39;_frameon&#39;,
 &#39;_gci&#39;,
 &#39;_gen_axes_patch&#39;,
 &#39;_gen_axes_spines&#39;,
 &#39;_get_axis_list&#39;,
 &#39;_get_lines&#39;,
 &#39;_get_patches_for_fill&#39;,
 &#39;_get_view&#39;,
 &#39;_gid&#39;,
 &#39;_gridOn&#39;,
 &#39;_hold&#39;,
 &#39;_in_layout&#39;,
 &#39;_init_axis&#39;,
 &#39;_label&#39;,
 &#39;_layoutbox&#39;,
 &#39;_left_title&#39;,
 &#39;_make_twin_axes&#39;,
 &#39;_mouseover&#39;,
 &#39;_mouseover_set&#39;,
 &#39;_navigate&#39;,
 &#39;_navigate_mode&#39;,
 &#39;_oid&#39;,
 &#39;_on_units_changed&#39;,
 &#39;_originalPosition&#39;,
 &#39;_path_effects&#39;,
 &#39;_pcolorargs&#39;,
 &#39;_picker&#39;,
 &#39;_position&#39;,
 &#39;_poslayoutbox&#39;,
 &#39;_process_unit_info&#39;,
 &#39;_prop_order&#39;,
 &#39;_propobservers&#39;,
 &#39;_quiver_units&#39;,
 &#39;_rasterization_zorder&#39;,
 &#39;_rasterized&#39;,
 &#39;_remove_legend&#39;,
 &#39;_remove_method&#39;,
 &#39;_right_title&#39;,
 &#39;_sci&#39;,
 &#39;_set_artist_props&#39;,
 &#39;_set_gc_clip&#39;,
 &#39;_set_lim_and_transforms&#39;,
 &#39;_set_position&#39;,
 &#39;_set_title_offset_trans&#39;,
 &#39;_set_view&#39;,
 &#39;_set_view_from_bbox&#39;,
 &#39;_shared_x_axes&#39;,
 &#39;_shared_y_axes&#39;,
 &#39;_sharex&#39;,
 &#39;_sharey&#39;,
 &#39;_sketch&#39;,
 &#39;_snap&#39;,
 &#39;_stale&#39;,
 &#39;_sticky_edges&#39;,
 &#39;_subplotspec&#39;,
 &#39;_tight&#39;,
 &#39;_transform&#39;,
 &#39;_transformSet&#39;,
 &#39;_twinned_axes&#39;,
 &#39;_update_image_limits&#39;,
 &#39;_update_line_limits&#39;,
 &#39;_update_patch_limits&#39;,
 &#39;_update_title_position&#39;,
 &#39;_update_transScale&#39;,
 &#39;_url&#39;,
 &#39;_use_sticky_edges&#39;,
 &#39;_validate_converted_limits&#39;,
 &#39;_visible&#39;,
 &#39;_xaxis_transform&#39;,
 &#39;_xcid&#39;,
 &#39;_xmargin&#39;,
 &#39;_yaxis_transform&#39;,
 &#39;_ycid&#39;,
 &#39;_ymargin&#39;,
 &#39;acorr&#39;,
 &#39;add_artist&#39;,
 &#39;add_callback&#39;,
 &#39;add_child_axes&#39;,
 &#39;add_collection&#39;,
 &#39;add_container&#39;,
 &#39;add_image&#39;,
 &#39;add_line&#39;,
 &#39;add_patch&#39;,
 &#39;add_table&#39;,
 &#39;aname&#39;,
 &#39;angle_spectrum&#39;,
 &#39;annotate&#39;,
 &#39;apply_aspect&#39;,
 &#39;arrow&#39;,
 &#39;artists&#39;,
 &#39;autoscale&#39;,
 &#39;autoscale_view&#39;,
 &#39;axes&#39;,
 &#39;axhline&#39;,
 &#39;axhspan&#39;,
 &#39;axis&#39;,
 &#39;axison&#39;,
 &#39;axvline&#39;,
 &#39;axvspan&#39;,
 &#39;bar&#39;,
 &#39;barbs&#39;,
 &#39;barh&#39;,
 &#39;bbox&#39;,
 &#39;boxplot&#39;,
 &#39;broken_barh&#39;,
 &#39;bxp&#39;,
 &#39;callbacks&#39;,
 &#39;can_pan&#39;,
 &#39;can_zoom&#39;,
 &#39;change_geometry&#39;,
 &#39;child_axes&#39;,
 &#39;cla&#39;,
 &#39;clabel&#39;,
 &#39;clear&#39;,
 &#39;clipbox&#39;,
 &#39;cohere&#39;,
 &#39;colNum&#39;,
 &#39;collections&#39;,
 &#39;containers&#39;,
 &#39;contains&#39;,
 &#39;contains_point&#39;,
 &#39;contour&#39;,
 &#39;contourf&#39;,
 &#39;convert_xunits&#39;,
 &#39;convert_yunits&#39;,
 &#39;csd&#39;,
 &#39;dataLim&#39;,
 &#39;drag_pan&#39;,
 &#39;draw&#39;,
 &#39;draw_artist&#39;,
 &#39;end_pan&#39;,
 &#39;errorbar&#39;,
 &#39;eventplot&#39;,
 &#39;eventson&#39;,
 &#39;figbox&#39;,
 &#39;figure&#39;,
 &#39;fill&#39;,
 &#39;fill_between&#39;,
 &#39;fill_betweenx&#39;,
 &#39;findobj&#39;,
 &#39;fmt_xdata&#39;,
 &#39;fmt_ydata&#39;,
 &#39;format_coord&#39;,
 &#39;format_cursor_data&#39;,
 &#39;format_xdata&#39;,
 &#39;format_ydata&#39;,
 &#39;get_adjustable&#39;,
 &#39;get_agg_filter&#39;,
 &#39;get_alpha&#39;,
 &#39;get_anchor&#39;,
 &#39;get_animated&#39;,
 &#39;get_aspect&#39;,
 &#39;get_autoscale_on&#39;,
 &#39;get_autoscalex_on&#39;,
 &#39;get_autoscaley_on&#39;,
 &#39;get_axes_locator&#39;,
 &#39;get_axisbelow&#39;,
 &#39;get_children&#39;,
 &#39;get_clip_box&#39;,
 &#39;get_clip_on&#39;,
 &#39;get_clip_path&#39;,
 &#39;get_contains&#39;,
 &#39;get_cursor_data&#39;,
 &#39;get_data_ratio&#39;,
 &#39;get_data_ratio_log&#39;,
 &#39;get_default_bbox_extra_artists&#39;,
 &#39;get_facecolor&#39;,
 &#39;get_fc&#39;,
 &#39;get_figure&#39;,
 &#39;get_frame_on&#39;,
 &#39;get_geometry&#39;,
 &#39;get_gid&#39;,
 &#39;get_gridspec&#39;,
 &#39;get_images&#39;,
 &#39;get_in_layout&#39;,
 &#39;get_label&#39;,
 &#39;get_legend&#39;,
 &#39;get_legend_handles_labels&#39;,
 &#39;get_lines&#39;,
 &#39;get_navigate&#39;,
 &#39;get_navigate_mode&#39;,
 &#39;get_path_effects&#39;,
 &#39;get_picker&#39;,
 &#39;get_position&#39;,
 &#39;get_rasterization_zorder&#39;,
 &#39;get_rasterized&#39;,
 &#39;get_renderer_cache&#39;,
 &#39;get_shared_x_axes&#39;,
 &#39;get_shared_y_axes&#39;,
 &#39;get_sketch_params&#39;,
 &#39;get_snap&#39;,
 &#39;get_subplotspec&#39;,
 &#39;get_tightbbox&#39;,
 &#39;get_title&#39;,
 &#39;get_transform&#39;,
 &#39;get_transformed_clip_path_and_affine&#39;,
 &#39;get_url&#39;,
 &#39;get_visible&#39;,
 &#39;get_window_extent&#39;,
 &#39;get_xaxis&#39;,
 &#39;get_xaxis_text1_transform&#39;,
 &#39;get_xaxis_text2_transform&#39;,
 &#39;get_xaxis_transform&#39;,
 &#39;get_xbound&#39;,
 &#39;get_xgridlines&#39;,
 &#39;get_xlabel&#39;,
 &#39;get_xlim&#39;,
 &#39;get_xmajorticklabels&#39;,
 &#39;get_xminorticklabels&#39;,
 &#39;get_xscale&#39;,
 &#39;get_xticklabels&#39;,
 &#39;get_xticklines&#39;,
 &#39;get_xticks&#39;,
 &#39;get_yaxis&#39;,
 &#39;get_yaxis_text1_transform&#39;,
 &#39;get_yaxis_text2_transform&#39;,
 &#39;get_yaxis_transform&#39;,
 &#39;get_ybound&#39;,
 &#39;get_ygridlines&#39;,
 &#39;get_ylabel&#39;,
 &#39;get_ylim&#39;,
 &#39;get_ymajorticklabels&#39;,
 &#39;get_yminorticklabels&#39;,
 &#39;get_yscale&#39;,
 &#39;get_yticklabels&#39;,
 &#39;get_yticklines&#39;,
 &#39;get_yticks&#39;,
 &#39;get_zorder&#39;,
 &#39;grid&#39;,
 &#39;has_data&#39;,
 &#39;have_units&#39;,
 &#39;hexbin&#39;,
 &#39;hist&#39;,
 &#39;hist2d&#39;,
 &#39;hitlist&#39;,
 &#39;hlines&#39;,
 &#39;ignore_existing_data_limits&#39;,
 &#39;images&#39;,
 &#39;imshow&#39;,
 &#39;in_axes&#39;,
 &#39;indicate_inset&#39;,
 &#39;indicate_inset_zoom&#39;,
 &#39;inset_axes&#39;,
 &#39;invert_xaxis&#39;,
 &#39;invert_yaxis&#39;,
 &#39;is_figure_set&#39;,
 &#39;is_first_col&#39;,
 &#39;is_first_row&#39;,
 &#39;is_last_col&#39;,
 &#39;is_last_row&#39;,
 &#39;is_transform_set&#39;,
 &#39;label_outer&#39;,
 &#39;legend&#39;,
 &#39;legend_&#39;,
 &#39;lines&#39;,
 &#39;locator_params&#39;,
 &#39;loglog&#39;,
 &#39;magnitude_spectrum&#39;,
 &#39;margins&#39;,
 &#39;matshow&#39;,
 &#39;minorticks_off&#39;,
 &#39;minorticks_on&#39;,
 &#39;mouseover&#39;,
 &#39;mouseover_set&#39;,
 &#39;name&#39;,
 &#39;numCols&#39;,
 &#39;numRows&#39;,
 &#39;patch&#39;,
 &#39;patches&#39;,
 &#39;pchanged&#39;,
 &#39;pcolor&#39;,
 &#39;pcolorfast&#39;,
 &#39;pcolormesh&#39;,
 &#39;phase_spectrum&#39;,
 &#39;pick&#39;,
 &#39;pickable&#39;,
 &#39;pie&#39;,
 &#39;plot&#39;,
 &#39;plot_date&#39;,
 &#39;properties&#39;,
 &#39;psd&#39;,
 &#39;quiver&#39;,
 &#39;quiverkey&#39;,
 &#39;redraw_in_frame&#39;,
 &#39;relim&#39;,
 &#39;remove&#39;,
 &#39;remove_callback&#39;,
 &#39;reset_position&#39;,
 &#39;rowNum&#39;,
 &#39;scatter&#39;,
 &#39;semilogx&#39;,
 &#39;semilogy&#39;,
 &#39;set&#39;,
 &#39;set_adjustable&#39;,
 &#39;set_agg_filter&#39;,
 &#39;set_alpha&#39;,
 &#39;set_anchor&#39;,
 &#39;set_animated&#39;,
 &#39;set_aspect&#39;,
 &#39;set_autoscale_on&#39;,
 &#39;set_autoscalex_on&#39;,
 &#39;set_autoscaley_on&#39;,
 &#39;set_axes_locator&#39;,
 &#39;set_axis_off&#39;,
 &#39;set_axis_on&#39;,
 &#39;set_axisbelow&#39;,
 &#39;set_clip_box&#39;,
 &#39;set_clip_on&#39;,
 &#39;set_clip_path&#39;,
 &#39;set_contains&#39;,
 &#39;set_facecolor&#39;,
 &#39;set_fc&#39;,
 &#39;set_figure&#39;,
 &#39;set_frame_on&#39;,
 &#39;set_gid&#39;,
 &#39;set_in_layout&#39;,
 &#39;set_label&#39;,
 &#39;set_navigate&#39;,
 &#39;set_navigate_mode&#39;,
 &#39;set_path_effects&#39;,
 &#39;set_picker&#39;,
 &#39;set_position&#39;,
 &#39;set_prop_cycle&#39;,
 &#39;set_rasterization_zorder&#39;,
 &#39;set_rasterized&#39;,
 &#39;set_sketch_params&#39;,
 &#39;set_snap&#39;,
 &#39;set_subplotspec&#39;,
 &#39;set_title&#39;,
 &#39;set_transform&#39;,
 &#39;set_url&#39;,
 &#39;set_visible&#39;,
 &#39;set_xbound&#39;,
 &#39;set_xlabel&#39;,
 &#39;set_xlim&#39;,
 &#39;set_xmargin&#39;,
 &#39;set_xscale&#39;,
 &#39;set_xticklabels&#39;,
 &#39;set_xticks&#39;,
 &#39;set_ybound&#39;,
 &#39;set_ylabel&#39;,
 &#39;set_ylim&#39;,
 &#39;set_ymargin&#39;,
 &#39;set_yscale&#39;,
 &#39;set_yticklabels&#39;,
 &#39;set_yticks&#39;,
 &#39;set_zorder&#39;,
 &#39;specgram&#39;,
 &#39;spines&#39;,
 &#39;spy&#39;,
 &#39;stackplot&#39;,
 &#39;stale&#39;,
 &#39;stale_callback&#39;,
 &#39;start_pan&#39;,
 &#39;stem&#39;,
 &#39;step&#39;,
 &#39;sticky_edges&#39;,
 &#39;streamplot&#39;,
 &#39;table&#39;,
 &#39;tables&#39;,
 &#39;text&#39;,
 &#39;texts&#39;,
 &#39;tick_params&#39;,
 &#39;ticklabel_format&#39;,
 &#39;title&#39;,
 &#39;titleOffsetTrans&#39;,
 &#39;transAxes&#39;,
 &#39;transData&#39;,
 &#39;transLimits&#39;,
 &#39;transScale&#39;,
 &#39;tricontour&#39;,
 &#39;tricontourf&#39;,
 &#39;tripcolor&#39;,
 &#39;triplot&#39;,
 &#39;twinx&#39;,
 &#39;twiny&#39;,
 &#39;update&#39;,
 &#39;update_datalim&#39;,
 &#39;update_datalim_bounds&#39;,
 &#39;update_from&#39;,
 &#39;update_params&#39;,
 &#39;use_sticky_edges&#39;,
 &#39;viewLim&#39;,
 &#39;violin&#39;,
 &#39;violinplot&#39;,
 &#39;vlines&#39;,
 &#39;xaxis&#39;,
 &#39;xaxis_date&#39;,
 &#39;xaxis_inverted&#39;,
 &#39;xcorr&#39;,
 &#39;yaxis&#39;,
 &#39;yaxis_date&#39;,
 &#39;yaxis_inverted&#39;,
 &#39;zorder&#39;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[137]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">dir</span><span class="p">(</span><span class="n">plt</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[137]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;Annotation&#39;,
 &#39;Arrow&#39;,
 &#39;Artist&#39;,
 &#39;AutoLocator&#39;,
 &#39;Axes&#39;,
 &#39;Button&#39;,
 &#39;Circle&#39;,
 &#39;Figure&#39;,
 &#39;FigureCanvasBase&#39;,
 &#39;FixedFormatter&#39;,
 &#39;FixedLocator&#39;,
 &#39;FormatStrFormatter&#39;,
 &#39;Formatter&#39;,
 &#39;FuncFormatter&#39;,
 &#39;GridSpec&#39;,
 &#39;IndexLocator&#39;,
 &#39;Line2D&#39;,
 &#39;LinearLocator&#39;,
 &#39;Locator&#39;,
 &#39;LogFormatter&#39;,
 &#39;LogFormatterExponent&#39;,
 &#39;LogFormatterMathtext&#39;,
 &#39;LogLocator&#39;,
 &#39;MaxNLocator&#39;,
 &#39;MultipleLocator&#39;,
 &#39;Normalize&#39;,
 &#39;NullFormatter&#39;,
 &#39;NullLocator&#39;,
 &#39;Number&#39;,
 &#39;PolarAxes&#39;,
 &#39;Polygon&#39;,
 &#39;Rectangle&#39;,
 &#39;ScalarFormatter&#39;,
 &#39;Slider&#39;,
 &#39;Subplot&#39;,
 &#39;SubplotTool&#39;,
 &#39;Text&#39;,
 &#39;TickHelper&#39;,
 &#39;Widget&#39;,
 &#39;_INSTALL_FIG_OBSERVER&#39;,
 &#39;_IP_REGISTERED&#39;,
 &#39;__builtins__&#39;,
 &#39;__cached__&#39;,
 &#39;__doc__&#39;,
 &#39;__file__&#39;,
 &#39;__loader__&#39;,
 &#39;__name__&#39;,
 &#39;__package__&#39;,
 &#39;__spec__&#39;,
 &#39;_auto_draw_if_interactive&#39;,
 &#39;_autogen_docstring&#39;,
 &#39;_backend_mod&#39;,
 &#39;_get_running_interactive_framework&#39;,
 &#39;_interactive_bk&#39;,
 &#39;_log&#39;,
 &#39;_pylab_helpers&#39;,
 &#39;_setp&#39;,
 &#39;_setup_pyplot_info_docstrings&#39;,
 &#39;_show&#39;,
 &#39;_string_to_bool&#39;,
 &#39;acorr&#39;,
 &#39;angle_spectrum&#39;,
 &#39;annotate&#39;,
 &#39;arrow&#39;,
 &#39;autoscale&#39;,
 &#39;autumn&#39;,
 &#39;axes&#39;,
 &#39;axhline&#39;,
 &#39;axhspan&#39;,
 &#39;axis&#39;,
 &#39;axvline&#39;,
 &#39;axvspan&#39;,
 &#39;bar&#39;,
 &#39;barbs&#39;,
 &#39;barh&#39;,
 &#39;bone&#39;,
 &#39;box&#39;,
 &#39;boxplot&#39;,
 &#39;broken_barh&#39;,
 &#39;cla&#39;,
 &#39;clabel&#39;,
 &#39;clf&#39;,
 &#39;clim&#39;,
 &#39;close&#39;,
 &#39;cm&#39;,
 &#39;cohere&#39;,
 &#39;colorbar&#39;,
 &#39;colormaps&#39;,
 &#39;connect&#39;,
 &#39;contour&#39;,
 &#39;contourf&#39;,
 &#39;cool&#39;,
 &#39;copper&#39;,
 &#39;csd&#39;,
 &#39;cycler&#39;,
 &#39;dedent&#39;,
 &#39;delaxes&#39;,
 &#39;deprecated&#39;,
 &#39;disconnect&#39;,
 &#39;docstring&#39;,
 &#39;draw&#39;,
 &#39;draw_all&#39;,
 &#39;draw_if_interactive&#39;,
 &#39;errorbar&#39;,
 &#39;eventplot&#39;,
 &#39;figaspect&#39;,
 &#39;figimage&#39;,
 &#39;figlegend&#39;,
 &#39;fignum_exists&#39;,
 &#39;figtext&#39;,
 &#39;figure&#39;,
 &#39;fill&#39;,
 &#39;fill_between&#39;,
 &#39;fill_betweenx&#39;,
 &#39;findobj&#39;,
 &#39;flag&#39;,
 &#39;gca&#39;,
 &#39;gcf&#39;,
 &#39;gci&#39;,
 &#39;get&#39;,
 &#39;get_backend&#39;,
 &#39;get_cmap&#39;,
 &#39;get_current_fig_manager&#39;,
 &#39;get_figlabels&#39;,
 &#39;get_fignums&#39;,
 &#39;get_plot_commands&#39;,
 &#39;get_scale_docs&#39;,
 &#39;get_scale_names&#39;,
 &#39;getp&#39;,
 &#39;ginput&#39;,
 &#39;gray&#39;,
 &#39;grid&#39;,
 &#39;hexbin&#39;,
 &#39;hist&#39;,
 &#39;hist2d&#39;,
 &#39;hlines&#39;,
 &#39;hot&#39;,
 &#39;hsv&#39;,
 &#39;importlib&#39;,
 &#39;imread&#39;,
 &#39;imsave&#39;,
 &#39;imshow&#39;,
 &#39;inferno&#39;,
 &#39;inspect&#39;,
 &#39;install_repl_displayhook&#39;,
 &#39;interactive&#39;,
 &#39;ioff&#39;,
 &#39;ion&#39;,
 &#39;isinteractive&#39;,
 &#39;jet&#39;,
 &#39;legend&#39;,
 &#39;locator_params&#39;,
 &#39;logging&#39;,
 &#39;loglog&#39;,
 &#39;magma&#39;,
 &#39;magnitude_spectrum&#39;,
 &#39;margins&#39;,
 &#39;matplotlib&#39;,
 &#39;matshow&#39;,
 &#39;minorticks_off&#39;,
 &#39;minorticks_on&#39;,
 &#39;mlab&#39;,
 &#39;new_figure_manager&#39;,
 &#39;nipy_spectral&#39;,
 &#39;np&#39;,
 &#39;pause&#39;,
 &#39;pcolor&#39;,
 &#39;pcolormesh&#39;,
 &#39;phase_spectrum&#39;,
 &#39;pie&#39;,
 &#39;pink&#39;,
 &#39;plasma&#39;,
 &#39;plot&#39;,
 &#39;plot_date&#39;,
 &#39;plotfile&#39;,
 &#39;plotting&#39;,
 &#39;polar&#39;,
 &#39;prism&#39;,
 &#39;psd&#39;,
 &#39;pylab_setup&#39;,
 &#39;quiver&#39;,
 &#39;quiverkey&#39;,
 &#39;rc&#39;,
 &#39;rcParams&#39;,
 &#39;rcParamsDefault&#39;,
 &#39;rcParamsOrig&#39;,
 &#39;rc_context&#39;,
 &#39;rcdefaults&#39;,
 &#39;rcsetup&#39;,
 &#39;re&#39;,
 &#39;register_cmap&#39;,
 &#39;rgrids&#39;,
 &#39;savefig&#39;,
 &#39;sca&#39;,
 &#39;scatter&#39;,
 &#39;sci&#39;,
 &#39;semilogx&#39;,
 &#39;semilogy&#39;,
 &#39;set_cmap&#39;,
 &#39;setp&#39;,
 &#39;show&#39;,
 &#39;silent_list&#39;,
 &#39;specgram&#39;,
 &#39;spring&#39;,
 &#39;spy&#39;,
 &#39;stackplot&#39;,
 &#39;stem&#39;,
 &#39;step&#39;,
 &#39;streamplot&#39;,
 &#39;style&#39;,
 &#39;subplot&#39;,
 &#39;subplot2grid&#39;,
 &#39;subplot_tool&#39;,
 &#39;subplots&#39;,
 &#39;subplots_adjust&#39;,
 &#39;summer&#39;,
 &#39;suptitle&#39;,
 &#39;switch_backend&#39;,
 &#39;sys&#39;,
 &#39;table&#39;,
 &#39;text&#39;,
 &#39;thetagrids&#39;,
 &#39;tick_params&#39;,
 &#39;ticklabel_format&#39;,
 &#39;tight_layout&#39;,
 &#39;time&#39;,
 &#39;title&#39;,
 &#39;tricontour&#39;,
 &#39;tricontourf&#39;,
 &#39;tripcolor&#39;,
 &#39;triplot&#39;,
 &#39;twinx&#39;,
 &#39;twiny&#39;,
 &#39;uninstall_repl_displayhook&#39;,
 &#39;violinplot&#39;,
 &#39;viridis&#39;,
 &#39;vlines&#39;,
 &#39;waitforbuttonpress&#39;,
 &#39;warn_deprecated&#39;,
 &#39;warnings&#39;,
 &#39;winter&#39;,
 &#39;xcorr&#39;,
 &#39;xkcd&#39;,
 &#39;xlabel&#39;,
 &#39;xlim&#39;,
 &#39;xscale&#39;,
 &#39;xticks&#39;,
 &#39;ylabel&#39;,
 &#39;ylim&#39;,
 &#39;yscale&#39;,
 &#39;yticks&#39;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[138]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[138]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x1976301e550&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[143]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="n">height</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">width</span><span class="o">=</span><span class="mf">0.5</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[143]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;BarContainer object of 20 artists&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[144]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">random</span> <span class="k">import</span> <span class="n">sample</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[146]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span> <span class="o">=</span> <span class="n">sample</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">10000</span><span class="p">),</span> <span class="mi">10</span><span class="p">)</span>
<span class="n">data</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[146]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[981, 8668, 5340, 7486, 114, 9562, 6817, 2753, 9944, 3504]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[148]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">rwidth</span><span class="o">=</span><span class="mf">0.8</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[148]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([2., 0., 1., 1., 0., 1., 1., 1., 1., 2.]),
 array([ 114., 1097., 2080., 3063., 4046., 5029., 6012., 6995., 7978.,
        8961., 9944.]),
 &lt;a list of 10 Patch objects&gt;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[155]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span> <span class="o">=</span> <span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">normal</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="n">std</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span> <span class="k">for</span> <span class="n">std</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">3</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[157]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">vert</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="n">patch_artist</span><span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[164]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span> <span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
<span class="n">ax</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">)</span>

<span class="n">ax</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
<span class="n">ax</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">set_yscale</span><span class="p">(</span><span class="s1">&#39;log&#39;</span><span class="p">)</span>
<span class="n">fig</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAsgAAAEYCAYAAABBfQDEAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAIABJREFUeJzs3Xd4VFXixvHvSQ9JCCUBIXQCSBeINLGhIhYWbAgIYkXsrrqWXf25q+uuuu7alWXFVelFpYm6ihVRhNA7oYeWQEIaqTPn98cMGhAkQCY3M/N+nocnM3fuzLy4S/LmzLnnGGstIiIiIiLiEeJ0ABERERGR6kQFWURERESkHBVkEREREZFyVJBFRERERMpRQRYRERERKUcFWURERESkHBVkEREREZFyVJBFRERERMpRQRYRERERKSfM6QAACQkJtlmzZk7HEBHxqdTU1P3W2kSncxyPvheLSKCr6PfhalGQmzVrxpIlS5yOISLiU8aY7U5n+C36Xiwiga6i34c1xUJEREREpJwKFWRjzDZjzCpjzHJjzBLvsTrGmM+NMZu8X2t7jxtjzKvGmDRjzEpjTFdf/gVEROT0GGMGGGPG5uTkOB1FRKRaOJkR5AuttWdZa1O89x8D5ltrWwHzvfcBLgNaef+MAt6qrLAiIlL5rLVzrLWj4uPjnY4iIlItnM4Ui4HAe97b7wGDyh1/33r8CNQyxjQ4jfcREREREakyFS3IFvifMSbVGDPKe6y+tXYPgPdrPe/xJGBnueeme48dwRgzyhizxBizJDMz89TSi4iIiIhUsoquYnGOtXa3MaYe8LkxZv1vnGuOccz+6oC1Y4GxACkpKb96XERERETECRUaQbbW7vZ+zQA+AroD+w5PnfB+zfCeng40Lvf0RsDuygosIiIiIuJLJyzIxpgYY0zc4dtAP2A1MBsY6T1tJDDLe3s2cKN3NYueQM7hqRgiIiIiItVdRUaQ6wMLjDErgJ+Aj621nwLPAZcYYzYBl3jvA8wDtgBpwH+Auyo9tYiIEzZ8CtNvgrISp5OIiASlwhIXD05dzmdr9vr0fU44B9lauwXofIzjB4CLjnHcAndXSjoRkepiw6cwdTic0QHKCiEswulEIiJBZdv+AkZPSGXDvjzaNqjp0/eqFltNi4hUaxs+gakjPOV4xEyI0nrBIiJV6Yu1+/j9tOWEhhjevbk757dO9On7qSCLiPyW9fNg2o1wRkcY8RFE13I6UaUzxgwABiQnJzsdRUTkCC635eUvNvLal2l0SKrJWzd0o3GdGj5/39PZKEREJLAdLscNOgVsOQbtpCci1VN2QQk3v7uY175M47pujZgxuneVlGPQCLKIyLGt/ximjfylHGtahYhIlVmVnsPoCalk5hXz96s7MuTsxhhzrK02fEMFWUTkaCrHIiKOmbZ4J0/MWk1CTATTR/eic+Oq//ROBVlEpLx1c2H6SGhwFoz4UOVYRKSKFJe5+PPstUz+aQd9khN4dWgX6sQ4s2KQCrKIyGGHy3HDLjD8A5VjEZEqsutgIXdNSGVFeg53XdCSh/q1ITSk6qZUHE0FWUQEYN0czyYgDbvA8A8hyrdrbIqIiMeCTfu5d/JSylyWf4/oxqXtz3A6kgqyiAhrZ8OMm6FhV+/IscqxiIivWWt565vNvPjZBpLrxTJmeDdaJMY6HQtQQRaRYLd2Fsy4BZK6wQ0zVI5FRKpAblEpD09bwf/W7mNA54Y8f01HakRUn1pafZKIiFS1tbNg+s3QKMUzchwZ53QiEZGAt3FfHqPHp7Ij6xBPDWjHTb2bVekSbhWhgiwiwUnlWESkys1esZtHZ6wkNiqMSbf3pHvzOk5HOiYVZBEJPmtmeqZVNDobhs9QORYR8bFSl5u/z1vPO99v5exmtXljWFfq1YxyOtZxqSCLSHBZN9dTjht3hxumqxyLiPhYRm4Rd09ayuJt2dxyTnMev/xMwkNDnI71m1SQRSR47F0NH97uWcpN5VhExOcWb8virolLyS8q49WhXfhd54ZOR6qQ6l3fRUQqy6EsmDLMs/nHkIlBUY6NMTHGmFRjzJVOZxGR4GKt5Z0FWxk69kdiI8OYefc5flOOQQVZRIKBq8wzrSJvD1w/AeKcX4T+VBhj3jHGZBhjVh91vL8xZoMxJs0Y81i5hx4FplVtShEJdgXFZdw3ZTlPz13LhWfWY9Y959DmDP8alNAUCxEJfPP/Alu+goFveFat8F/vAq8D7x8+YIwJBd4ALgHSgcXGmNlAQ2AtUH2vghGRgLMlM5/RE1JJy8jnD5e24c7zWxLi4JbRp0oFWUQC26oZsPBV6D4Kugx3Os1psdZ+a4xpdtTh7kCatXYLgDFmCjAQiAVigHZAoTFmnrXWXYVxRSTIfLZmLw9PW0FYqOH9W3rQp1WC05FOmQqyiASuPStg1j3Q9By49G9Op/GVJGBnufvpQA9r7T0AxpibgP3HK8fGmFHAKIAmTZr4NqmIBCSX2/Li/zbw1teb6dQonreGdyOpVrTTsU6LCrKIBKaC/TDlBqhRB657D0LDnU7kK8f67NL+fMPad3/rydbascBYgJSUFPtb54qIHO1AfjH3T1nOgrT9DO3ehKcGtCMqPNTpWKdNBVlEAo+rFKbfBAWZcMunEJvodCJfSgcal7vfCNh9Mi9gjBkADEhOTq7MXCIS4JbvPMhdE1LZX1DCC9d0YvDZjU/8JD+hVSxEJPD870nY9h0MeMWz5nFgWwy0MsY0N8ZEAEOA2SfzAtbaOdbaUfHx8T4JKCKBxVrLpEU7GDzmB4wxfDC6d0CVY9AIsogEmuWTYNFb0PNu6DzE6TSVyhgzGbgASDDGpANPWWvHGWPuAT4DQoF3rLVrHIwpIgGsqNTFkzNXMz01nfNaJ/LK9WdROybC6ViVTgVZRALHrlSY8wA0Pw8uedrpNJXOWjv0OMfnAfNO9XU1xUJEKmJn1iHunJjK6l253Nc3mfsvbk2oHy7hVhGaYiEigSE/A6YMh9j6cO27EKrf/ytKUyxE5ES+3pDBgNcXsP3AId6+MYUH+7UJ2HIMGkEWkUBQVgLTboTCbLj1fxBT1+lEIiIBwe22vP5VGi99sZE29eMYM7wbzRJinI7lcyrIIuL/PnscdvwA14yDBp2cTiMiEhByCkt5cOpy5q/PYNBZDfn71Z2IjvD/JdwqQgVZRPxb6nuw+G04537oeK3TafyS5iCLyNHW7s7lzomp7Mou5OmB7RnRsynGBO6UiqNpDrKI+K+dP8G8h6FlX7joKafT+C3NQRaR8j5als7Vb31PUamLqXf05MZezYKqHINGkEXEX+XugakjoGaSZ2pFSHB87Cci4islZW7++vFa3v9hO92b1+H1YV2oFxfldCxHqCCLiP8pK4ZpI6A4D0Z85NlOWk6ZpliIyN6cIu6amMrSHQe5/dzmPNL/TMJDg3eiQfD+zUXEP1kLHz8I6YvhqregfjunE/k9TbEQCW4/bD7Ala99x/q9ebwxrCt/uqJdUJdj0AiyiPibha/Csglw3iPQbqDTaURE/Ja1lre/28pzn66nad0aTL69J63qxzkdq1pQQRYR/7H+Y/j8KWh/NVz4R6fTiIj4rfziMh6ZsYJ5q/bSv/0Z/OO6TsRFhTsdq9pQQRYR/7BnBXxwGyR1hUFvQpBdUS0iUlnSMvK5Y/wStu4v4PHLzmTUeS2CbpWKE1FBFpHqL3cPTBoC0XVgyGQIj3Y6UUDRRXoiweOTVXt4ePoKosJDmXBrD3onJzgdqVqq8AxsY0yoMWaZMWau935zY8wiY8wmY8xUY0yE93ik936a9/FmvokuIkGh5BBMGQpFOTBsCsTVdzpRwNFFeiKBr8zl5u/z1nHnxKW0qh/H3Pv6qBz/hpO5RPF+YF25+88DL1lrWwHZwK3e47cC2dbaZOAl73kiIifP7YaZo2H3crh2HJzR0elEIiJ+Z39+McPHLeLf325heM8mTL2jJw3i9Uncb6lQQTbGNAKuAN723jdAX2CG95T3gEHe2wO99/E+fpHRxBYRORVfPQtrZ0G/v0Kby5xOIyLid5buyObKVxewbMdBXryuM38d1JHIMG2sdCIVHUF+GXgEcHvv1wUOWmvLvPfTgSTv7SRgJ4D38Rzv+UcwxowyxiwxxizJzMw8xfgiErBWTIHvXoSuI6HX3U6nERHxK9Zaxv+4nev//QPhYYYP7+rNtd0aOR3Lb5ywIBtjrgQyrLWp5Q8f41Rbgcd+OWDtWGttirU2JTExsUJhRSRIbP8BZt8Lzc+DK/6pFSt8zBgzwBgzNicnx+koIlIJCktcPDR9BU/OXE2f5ATm3nMu7RvqGoOTUZFVLM4BfmeMuRyIAmriGVGuZYwJ844SNwJ2e89PBxoD6caYMCAeyKr05CISmLK2wtQboFYTGPw+hGpdTl+z1s4B5qSkpNzudBYROT3bDxQwesJS1u/N5YGLW3Ff31aEhGiQ4WSdcATZWvu4tbaRtbYZMAT40lp7A/AVcK33tJHALO/t2d77eB//0lr7qxFkEZFfKcqByUPA7YJh0yC6ttOJRET8xpfr9zHgtQXsyj7EOyPP5oGLW6scn6LTWQf5UWCKMeavwDJgnPf4OGC8MSYNz8jxkNOLKCJBwVUG02+GA2kwYibUbel0IhERv+B2W16Zv4lX5m+iXYOajBnejSZ1azgdy6+dVEG21n4NfO29vQXofoxzioDrKiGbiASTzx6HzfNhwKvQ/Fyn04iI+IWDh0p4YOpyvt6QydVdk3h2UEeiI7RKxenSTnoi4rxFY+GnsdD7Xug28sTni4gIq3flMHpCKvtyi3hmUAeG92iiLaMriQqyiDhr0xfw6aPQ5nK4+C9OpxER8QszUtP500erqF0jgml39KJLE12zUZlUkEXEORnrYMbNUK89XP0fCNHHgiIiv6W4zMXTc9YycdEOerWoy2vDupAQG+l0rICjgiwizijYD5Ouh/BoGDYFImOdThS0jDEDgAHJyclORxGR37D7YCF3TlzKip0HueP8FvyhXxvCQiu655ucDP1XFZGql7sH3h8E+ftg6GSI1+5OTrLWzrHWjoqP10YCItXVwrT9XPnaAtL25fHWDV15/LK2Ksc+pBFkEalaGetgwrVQdBCGTIKkbk4nEhGptqy1/PvbLbzw6XpaJMYyZng3kuvpEzdfU0EWkaqzbQFMGQZhUXDzPGjQ2elEIiLVVl5RKQ9PX8Fna/ZxRccGvHBtJ2IiVd2qgv4ri0jVWDUDZt4JtZvD8BmeraRFROSYNu3L447xqWzPOsQTV7Tl1j7NtYRbFVJBFhHfshYWvgafPwlNz4EhE7WFtIjIb5i7cjePzFhJjYhQJt7Wg54t6jodKeioIIuI77hd8Oljnk1A2l8Fg8ZAeJTTqUREqqVSl5vnPlnPuAVb6dqkFm/e0I0z4vU90wkqyCLiG6WF8MFtsH4u9LoHLnkGQnTFtYjIsWTkFXHPpGX8tDWLm3o344+XtyUiTN8znaKCLCKVr+AATL4e0pdA/+eh52inE4mIVFup27O4a+JScgpLeen6zlzVRUtfOk0FWUQqV9YWzzJuubtg8PvQ7ndOJxIRqZastby3cBt//XgdSbWjeffm7rRtUNPpWIIKsohUpvRUmDQYrAtunA1NejidSCpAO+mJVL1DJWX88cNVzFy+m4vb1uOfg88iPjrc6VjipcktIlI5NnwC714BETFw6+cqx35EO+mJVK1t+wu4+s2FzFqxm4f7tWbsiBSV42pGI8gicvqWvAMfP+TZ+GPYNIit53QiEZFq6Yu1+/j9tOWEhhjevbk757dOdDqSHIMKsoicOmth/tOw4F/Q6lK47r+eEWQRETmCy2156fONvP5VGh2SavLWDd1oXKeG07HkOFSQReTU5O6BeQ97lnHrdhNc/k8I1bcUEZGjZReUcN+UZXy3aT+DUxrx9MAORIWHOh1LfoN+monIyXG7YPHbMP8ZcJVAv7961jnWFqgiIr+yKj2H0RNSycwr5u9Xd2Ro9yZOR5IKUEEWkYrbvRzmPgC7l0HLvnD5i1C3pdOpRESqpamLd/DkrDUkxEQwfXQvOjeu5XQkqSAVZBE5saJc+OpZz5bRNRLgmnHQ4RqNGouIHENRqYs/z17DlMU76ZOcwKtDu1AnJsLpWHISVJBF5PishXWz4ZNHIW8vnH0r9H0SojUKIiJyLOnZh7hzwlJW7crhrgta8lC/NoSGaDDB36ggi8ixZW/3XIS36X9wRke4fgI0SnE6lYhItfXdpkzum7yMMpdl7Ihu9Gt/htOR5BSpIIvIkVyl8MPr8PXzYELg0r9B9zu0QoWIyHG43Za3vtnMi//bQKt6sYwZ3o0WibFOx5LToJ94IvKLHT/C3N9Dxlo480q47HmIb+R0KhGRaiunsJSHpq3gi3X7GNC5Ic9d3ZGYSNUrf6f/BUUEDmXBF0/B0vehZiMYMhnOvNzpVCIi1dr6vbmMHp9KenYhTw1ox029m2F08XJAUEEWCXYbPoFZ90BhNvS+F85/DCL10aCIyG+ZtXwXj32witioMCaP6snZzeo4HUkqkQqySDDL2wsf3AZ1msONMz0X40lAMMa0Be4HEoD51tq3HI4kEhBKXW6e/Xgd7y7cxtnNavPGsK7UqxnldCypZCFOBxARB33xF89ueNe9p3LsB4wx7xhjMowxq4863t8Ys8EYk2aMeQzAWrvOWjsaGAxo+RGRSpCRW8TQsT/y7sJt3HJOcybd3lPlOECpIIsEq/QlsGIS9Lpbu+H5j3eB/uUPGGNCgTeAy4B2wFBjTDvvY78DFgDzqzamSOD5aWsWV7y2gDW7c3l1aBf+b0A7wkNVowKV/pcVCUZuN8z7A8SeAec+5HQaqSBr7bdA1lGHuwNp1tot1toSYAow0Hv+bGttb+CG472mMWaUMWaJMWZJZmamr6KL+C1rLeMWbGXof34kNjKMmXefw+86N3Q6lviY5iCLBKMVk2D3UrhqLETGOZ1GTk8SsLPc/XSghzHmAuBqIBKYd7wnW2vHAmMBUlJSrO9iivifguIyHv1gJXNX7qFfu/q8OLgzNaPCnY4lVUAFWSTYFOXAF3+GRt2h02Cn08jpO9aaUtZa+zXwddVGEQkcWzLzGT0hlbSMfB7p34bR57UkRFtGBw0VZJFg880LULAfbpgOWq8zEKQDjcvdbwTsPpkXMMYMAAYkJydXZi4Rv/XZmr08NG0FEWEhvH9LD/q0SnA6klQxzUEWCSaZG2HRGOg6Ahp2cTqNVI7FQCtjTHNjTAQwBJh9Mi9grZ1jrR0VHx/vk4Ai/sLltjz/6XruGJ9Ky8QY5tzbR+U4SGkEWSRYWAufPgrhMdD3/5xOI6fAGDMZuABIMMakA09Za8cZY+4BPgNCgXestWtO8nU1gixB70B+MfdNWcb3aQcY2r0JTw1oR1R4qNOxxCEqyCLBYsMnsPlL6P8cxCY6nUZOgbV26HGOz+M3LsSrwOvOAeakpKTcfqqvIeLPlu88yF0TUtlfUMIL13Ri8NmNT/wkCWgnnGJhjIkyxvxkjFlhjFljjPmL93hzY8wiY8wmY8xU70d7GGMivffTvI838+1fQUROqLQIPnscEs+Es29zOo2ISLVgrWXSoh0MHvMDxhg+vLO3yrEAFZuDXAz0tdZ2Bs4C+htjegLPAy9Za1sB2cCt3vNvBbKttcnAS97zRMRJP74B2dug/98hVEsUiYgUlbp4ZMZK/vjRKnq2rMvce/vQIUnz8MXjhAXZeuR774Z7/1igLzDDe/w9YJD39kDvfbyPX2SMLpUXcUzubvj2n3DmldCyr9NppBoyxgwwxozNyclxOopIldiZdYhr3lrI9NR07uubzH9vOpvaMRFOx5JqpEKrWBhjQo0xy4EM4HNgM3DQWlvmPSUdz2L1UG7Reu/jOUDdY7ymdm8SqQqfPwXuMrj0WaeTSDWlVSwkmHy9IYMrX1vAjqxDjBuZwoP92hCq9Y3lKBUqyNZal7X2LDzra3YH2h7rNO/XYy5af4zXHGutTbHWpiQm6oIhEZ/Y8SOsmgbn3Ae1mzmdRkTEMW635dX5m7j53cU0iI9izj19uKhtfadjSTV1UqtYWGsPGmO+BnoCtYwxYd5R4vIL0x9etD7dGBMGxANZlRdZRCrE7YJ5f4CaSdDn906nERFxTM6hUn4/bTlfrs/gqi5J/O2qjkRHaAk3Ob6KrGKRaIyp5b0dDVwMrAO+Aq71njYSmOW9Pdt7H+/jX1prfzWCLCI+tvR92LsSLnkaImKcTiPVmOYgSyBbuzuXAa8v4NuNmTw9sD3/GtxZ5VhOqCJTLBoAXxljVuLZselza+1c4FHgQWNMGp45xuO8548D6nqPPwg8VvmxReQ3FWbDl89Ak97Q4Rqn00g1pznIEqg+XJrO1W99T3GZi6l39OTGXs3QugFSESecYmGtXQn8ak9aa+0WPPORjz5eBFxXKelE5NR8/ZynJF/2POiHgYgEmZIyN8/MXcv4H7fTo3kdXhvWhXpxUU7HEj+infREAs2+tfDTf6DbTdCgk9NpRESq1N6cIu6cmMqyHQe5/dzmPNr/TMJCK7QmgcjPVJBFAom18OmjEBkHFz7hdBrxE8aYAcCA5ORkp6OInJYfNh/g3slLOVTi4o1hXbmiUwOnI4mf0q9UIoFk3RzY+i30fQJifrX8uMgxaQ6y+DtrLWO/3czwcYuoGR3OrLvPUTmW06IRZJFAUVoIn/0J6rWHbjc7nUZEpErkF5fxyIwVzFu1l8s6nMEL13YiLirc6Vji51SQRQLF969Czg4YOQdC9U9bRAJfWkYed4xPZev+Ah6/7ExGnddCq1RIpdBPUZFAcHAnLHgJ2g2C5uc5nUZExOfmrdrDH6avICo8lAm39qB3coLTkSSAqCCL+LuiXJh9j+d2v2eczSIi4mNlLjf/+GwD//52C2c1rsVbw7vSID7a6VgSYFSQRfzZnhUwbSQc3AFX/gtqNXE6kfghrWIh/iIzr5h7Jy/lxy1ZjOjZlCeubEtkmHbFk8qnVSxE/JG1sHgcvH0JlBXDTR971j0WOQVaxUL8wdId2Qx4bQHLdhzkn9d15plBHVSOxWc0gizib4pyYc79sOZDSL4YrhqrJd1EJGBZa5nw43aenruWM+Kj+PCu3rRvqF/mxLdUkEX8yZ6VMP0myN4GFz0F5zwAIfogSEQCU2GJiz/NXMWHS3dxYZtEXr6+C/E1tISb+J4Ksog/sBZS/wufPAY16sBNc6Fpb6dTiYj4zPYDBYyesJT1e3N54OJW3Ne3FSEhWsJNqoYKskh1V5wHcx6A1TOg5UVw9ViI0XJGIhK4vlqfwf1TlmGM4Z2bzubCNvWcjiRBRgVZpDrbuxqmj4SsLdD3SejzoKZUiEjAcrktr8zfxKvzN9GuQU3GDO9Gk7o1nI4lQUgFWaQ6shaWvgefPApRtWDkXGh2jtOpJEBpmTepDg4eKuH+Kcv5ZmMm13RtxLNXdSAqXKtUiDNUkEWqm+J8mPt7WDUNWlwIV/8HYhOdTiUBzFo7B5iTkpJyu9NZJDit3pXD6Amp7Mst4tmrOjCsexNtGS2OUkEWqU72rvasUpG1Gfo+AX0e0pQKEQlo05fs5ImZq6kTE8G0O3rRpUltpyOJqCCLVBsrp3u2jI6KhxtnQ/NznU4kIuIzxWUu/jJnLZMW7aBXi7q8NqwLCbGRTscSAVSQRaqHQ1kw+15o2AUGvw+xumJbRALX7oOF3DlxKSt2HmT0+S15uF9rwkL1aZlUHyrIItXBknegrBCu+JfKsYgEtO/T9nPv5GWUlLkZM7wr/Ts0cDqSyK+oIIs4rawYfhrrWeO4fjun04iI+IS1ljHfbOEfn62nRWIsY4Z3I7lerNOxRI5JBVnEaas/gPx9MOgtp5OIiPhEXlEpD09fwWdr9nFFxwa8cG0nYiJVQaT60v87RZxkLSx8Heq1g5Z9nU4jIlLpNu7LY/T4VLZnHeKJK9pya5/mWsJNqj0VZBEnbfkaMtbAwDdAPzBEJMDMWbGbRz9YSY2IUCbe1oOeLeo6HUmkQlSQRZz0w+sQUw86Xud0Egli2klPKlupy81zn6xn3IKtdG1Sizdv6MYZ8VFOxxKpMK2pIuKUjHWQ9gV0HwVhWvtTnGOtnWOtHRUfH+90FAkAGXlF3PCfRYxbsJWRvZoyZVQvlWPxOxpBFnHKD29AWDSk3OJ0EhGRSrFkWxZ3TVxKblEpL13fmau6NHI6ksgpUUEWcUJ+BqycCl2GQ4zm5ImIf7PW8t7Cbfz143Uk1Y7mvVu607ZBTadjiZwyFWQRJyx+G1wl0PNup5OIiJyWQyVlPP7hKmYt383Fbevxz8FnER8d7nQskdOigixS1UoLPQW59WWQoIuiRMR/bdtfwOgJqWzYl8fD/Vpz1wXJhIRoRR7xfyrIIlVtxRQ4dAB63+N0EhGRU/b52n08OG05oSGGd2/uzvmtE52OJFJpVJBFqpLb7bk4r0FnaHqO02lERE6ay2156fONvP5VGh2T4nnzhq40rlPD6VgilUoFWaQqpX0OBzbB1W9rYxAR8TvZBSXcN2UZ323az/UpjfnLwPZEhYc6HUuk0qkgi1Slha9BzSRoP8jpJCIiJ2Vl+kHunLCUzLxinru6I0O6N3E6kojPqCCLVJU9K2Dbd3DJ0xCqK7xFxH9MXbyDJ2etITE2kumje9G5cS2nI4n4lAqySFX54Q2IiIWuI51OIiJSIUWlLv48ew1TFu/k3FYJvDKkC3ViIpyOJeJzKsgiVSF3N6z+AM6+HaI18iIi1V969iHunLCUVbtyuPvCljx4SRtCtYSbBImQE51gjGlsjPnKGLPOGLPGGHO/93gdY8znxphN3q+1vceNMeZVY0yaMWalMaarr/8SItXeon+DdUPP0U4nERE5oe82ZTLgtQVs21/A2BHd+MOlZ6ocS1A5YUEGyoCHrLVtgZ7A3caYdsBjwHxrbStgvvc+wGVAK++fUcBblZ5axJ8U50Pqf6HtAKjdzOk0EiSMMYOMMf8xxswyxvRzOo/4B7fb8sZXadz4zk/Ui4ti9r196Nf+DKdjiVS5ExZka+0ea+1S7+08YB2QBAwE3vOe9h5w+LI7+lbzAAAgAElEQVT8gcD71uNHoJYxpkGlJxfxF8snQlEO9NLGIHJ6jDHvGGMyjDGrjzre3xizwfvJ3WMA1tqZ1trbgZuA6x2IK34mp7CUUeNT+cdnGxjQqSEf3d2b5gkxTscScURFRpB/ZoxpBnQBFgH1rbV7wFOigXre05KAneWelu49dvRrjTLGLDHGLMnMzDz55CL+wO2CH9+ERt2hcXen04j/exfoX/6AMSYUeAPPp3ftgKHeT/kOe8L7uMhxrd+by8DXF/D1hgyeGtCOV4acRY0IXaYkwavCBdkYEwt8ADxgrc39rVOPccz+6oC1Y621KdbalMREbU8pAWr9x5C9DXrd7XQSCQDW2m+BrKMOdwfSrLVbrLUlwBRgoPd6kOeBTw5/CngsGqyQWct3cdUbCykocTF5VE9uPqc5RhsZSZCrUEE2xoTjKccTrbUfeg/vOzx1wvs1w3s8HWhc7umNgN2VE1fEz/zwOtRq6pl/LOIbx/vU7l7gYuBaY8xxrw7VYEXwKilz8+fZa7h/ynI6JsXz8b19OLtZHadjiVQLJ/z8xHh+jRwHrLPW/qvcQ7OBkcBz3q+zyh2/xxgzBegB5ByeiiESVHYuhp2LoP9zEKKtWMVnjvmpnbX2VeDVqg4j/mFfbhF3T1zKku3Z3HJOcx6//EzCQ09q1qVIQKvIBKNzgBHAKmPMcu+xP+IpxtOMMbcCO4DrvI/NAy4H0oBDwM2VmljEX/zwOkTGQ5fhTieRwHban9oZYwYAA5KTkyszl1RTi7Yc4O5JyygoLuPVoV34XeeGTkcSqXZOWJCttQs49ggFwEXHON8CmnApwS17O6yb7Vm5IjLO6TQS2BYDrYwxzYFdwBBg2Mm8gLV2DjAnJSXldh/kk2rCWsu4BVv5+yfraVKnBpNu70Hr+vr+JHIsukRVxBcWjQETAj20MYhUHmPMZOACIMEYkw48Za0dZ4y5B/gMCAXesdaucTCmVEMFxWU8+sFK5q7cQ7929XlxcGdqRoU7HUuk2lJBFqlsRTmw9H1ofzXE/2qFQ5FTZq0depzj8/BMbzslmmIR2DZn5jN6fCqbM/N5pH8bRp/XkhDtiifymzQjX6Sypb4HJfla2k38hrV2jrV2VHx8vNNRpJJ9unovA1//nv35xbx/Sw/uuiBZ5VikAjSCLFKZXKWw6N/Q7FxoeJbTaUQkSJW53Lz4v42M+WYznRvF8+bwbiTVinY6lojfUEEWqUxrZ0FuOlzxotNJRCpMUywCy4H8Yu6dvIyFmw8wtHsTnhrQjqhwLTUpcjI0xUKkshRmw7f/gLrJ0OpSp9OIVJimWASO5TsPcuVrC1iyPZsXru3E36/uqHIscgo0gixSGfL2wvirIWsLDJkEIfrdU0SqjrWWyT/t5M+z15AYF8mHd/amQ5J+4RE5VSrIIqcrayuMHwT5mTBsGrS80OlEIhJEikpdPDlzNdNT0zmvdSKvXH8WtWMinI4l4tdUkEVOx761MP4qKCuCkbOhUYrTiUROmuYg+6+dWYcYPSGVNbtzua9vMvdf3JpQrVIhctr0ObDIqdq5GP57GRgDt3yqcix+S3OQ/dPXGzK48rUF7Mg6xLiRKTzYr43KsUgl0QiyyKnY/CVMuQFi68ONM6F2M6cTiUiQcLstr3+VxktfbKRN/Tj+PaIbTevGOB1LJKCoIIucrDUz4YPbILENDP8Q4uo7nUhEgkTOoVJ+P205X67P4KouSfztqo5ER2iVCpHKpoIscjJS34O5D0Cj7jBsKkTXcjqRyGnTHGT/sHZ3LqMnpLInp5CnB7ZnRM+mGKMpFSK+oDnIIhW14GWYcx+0vAhGfKRyLAFDc5Crvw+XpnP1W99TXOZiyqhe3NirmcqxiA9pBFnkRKyFL/4M378MHa6BQWMgTEsoiYjvlZS5eWbuWsb/uJ0ezevw+rCuJMZFOh1LJOCpIIv8FrcL5v4elr4HKbfA5S9CiOb7iYjv7c0p4s6JqSzbcZBR57XgkUvbEBaqD35FqoIKssjxlBXDh6Ng7Uw492Ho+4RnSTcRER/7YfMB7p28lMISF2/e0JXLOzZwOpJIUFFBFjmWkgKYOtyznFu/Z6H3PU4nEpEgYK3lP99t4flPN9C0bg2mjOpJcr04p2OJBB0VZJGjHcqCSdfDriUw8A3oMtzpRCI+pVUsqof84jIembGCeav2clmHM3jh2k7ERYU7HUskKGkyk8hh1sLaWfD2xbBnOQx+X+VYgoJWsXBeWkYeA19fwKer9/LHy8/kzRu6qhyLOEgjyCLWQtp8+PIZTzFOaO1Zxq1ZH6eTiUgQmLdqD3+YvoKo8FAm3NaD3i0TnI4kEvRUkCW4bV8I85+BHQuhVhMY9BZ0ul4rVYiIz5W53Lzw2QbGfruFsxrX4q3hXWkQH+10LBFBBVmC1e5lnmK8eT7EngFX/BO63Kj1jUWkSmTmFXPv5KX8uCWLET2b8sSVbYkM0y/mItWFCrIEl4x18NWzsG4ORNeBS56Bs2+DiBpOJxORIJG6PZu7Jy4l+1AJ/7yuM9d0a+R0JBE5igqyBIesrfD1c7ByKkTEwgV/hJ53QlRNp5OJSJCw1jLhx+08PXctZ8RH8eFdvWnfUBdGilRHKsgS2HJ3wzcvwLLxEBIO59wH5zwANeo4nUyk2tAyb75XWOLiTx+t4sNlu7iwTSIvX9+F+BpapUKkulJBlsBUsB8WvAQ//QesG7rdDOc9DHFnOJ1MpNqx1s4B5qSkpNzudJZAtP1AAXeMT2XDvjweuLgV9/VtRUiIduUUqc5UkCWwuN2Q+l/44s9Qkg+dh8H5j0Dtpk4nE5EgNH/dPh6YupwQY3jnprO5sE09pyOJSAWoIEvgyNwIc+6DHT9A8/Ph8hchsbXTqUQkCLncllfmb+LV+Zto16AmY4Z3o0ldXQws4i9UkMX/lZV4plN89yKE14CBb8JZw8DoI0wRqXoHD5Vw/5TlfLMxk2u6NuLZqzoQFa4l3ET8iQqy+LedP8Hs+yBzHXS4Fvo/B7GJTqcSkSC1elcOoyeksi+3iGev6sCw7k0w+mVdxO+oIIt/KsqF+U/D4rchvhEMmw6t+zmdSkSC2PQlO3li5mrqxEQw7Y5edGlS2+lIInKKVJDF/6yfBx8/BHl7oMdo6PsERMY6nUpEglRxmYu/zFnLpEU76N2yLq8O7UJCbKTTsUTkNKggi//I2wefPAJrZ0K99nD9BGjUzelUIhLEdh8s5M6JS1mx8yCjz2/Jw/1aExYa4nQsETlNKshS/VkLS9+Hz5+E0iLo+ySccz+EapF9EXHO92n7uXfyMkrK3IwZ3pX+HRo4HUlEKokKslRvBzbDnPth23fQ7Fy48mVI0G5fIpVJO+mdHGstY77Zwj8+W0/LxFjGjOhGy0RN8xIJJCrIUj253fD9y/D1cxAeBb97DbqM0NJtIj6gnfQqLq+olIenr+CzNfu4olMDXrimEzGR+lEqEmhO+K/aGPMOcCWQYa3t4D1WB5gKNAO2AYOttdnGs5bNK8DlwCHgJmvtUt9El4BVUgAf3QHr5kC7gXDZPyCuvtOpRCTIbdyXx+jxqWzPOsQTV7Tl1j7NtYSbSICqyJUE7wL9jzr2GDDfWtsKmO+9D3AZ0Mr7ZxTwVuXElKCRuwf+ezmsmwuX/g2ue0/lWEQcN2fFbga98T25RWVMuq0Ht53bQuVYJICdcATZWvutMabZUYcHAhd4b78HfA086j3+vrXWAj8aY2oZYxpYa/dUVmAJYLuXw+ShUJwLQ6dAm6N/LxMRqVqlLjfPfbKecQu20q1pbd68oSv1a0Y5HUtEfOxUJ07VP1x6rbV7jDH1vMeTgJ3lzkv3HvtVQTbGjMIzykyTJk1OMYYEjHVz4MNRUKMu3PIZnNHB6UQiEuQy8oq4Z+IyftqWxU29m/HHy9sSEaYl3ESCQWVfWXCsz5vssU601o4FxgKkpKQc8xwJAtZ6Lsb74s+QlAJDJmlKhYg4bsm2LO6auJTcolJevv4sBnVJcjqSiFShUy3I+w5PnTDGNAAyvMfTgcblzmsE7D6dgBLAykpg7gOwfCJ0uAYGvgHh0U6nEpEgZq3l3YXbePbjdSTVjua9W7rTtkFNp2OJSBU71c+KZgMjvbdHArPKHb/RePQEcjT/WI6p4ACMH+Qpxxc8DteMUzkWEUcdKinjganL+cuctVzQJpHZ9/RRORYJUhVZ5m0yngvyEowx6cBTwHPANGPMrcAO4Drv6fPwLPGWhmeZt5t9kFn8XeYGmDTYs2LFNeOg47VOJxKRILd1fwGjx6eyMSOPh/u15q4LkgkJ0SoVIsGqIqtYDD3OQxcd41wL3H26oSSAbf4Spt0EYRFw08fQ+GynE4lIkPt87T4enLqc0FDDezd357zWiU5HEhGHafsfqTqLx8G8P0DimTBsCtTS6iUi4hyX2/LS5xt5/as0OibF8+YNXWlcp4bTsUSkGlBBFt9zlcH//gSLxkCrS+HacRAZ53QqEQliWQUl3D9lGd9t2s/1KY35y8D2RIWHOh1LRKoJFWTxraJcmHELpH0OPe+Gfs9AiH4IiYhzVqYf5M4JS8nMK+a5qzsypLs+zRKRI6kgS+UrLYSdP8HWb2DNR5C9Ha58CVJucTqZSNAwxrQA/gTEW2t1JazXlJ928H+z1pAQG8H00b3o3LiW05FEpBpSQZbT5yqD3Us9hXjrt7BjEbiKwYRCUjdPOW5xgdMpRfyeMeYd4Eogw1rbodzx/sArQCjwtrX2OWvtFuBWY8wMZ9JWL0WlLp6atYapS3ZybqsEXhnShToxEU7HEpFqSgVZTp7bDRlrPGV4yzewfSGU5Hkeq98Rut8Ozc+DJr0gSmuIilSid4HXgfcPHzDGhAJvAJfg2axpsTFmtrV2rSMJq6H07EPcOWEpq3blcPeFLXnwkjaEagk3EfkNKshyYtZC1hbPCPGWb2Dbd3DogOexOi2h03WeQtzsPIip62xWkQBmrf3WGNPsqMPdgTTviDHGmCnAQKBCBdkYMwoYBdCkSeDNxf12Yyb3TVmGy2UZO6Ib/dqf4XQkEfEDKshyfBnrYMUUWP0h5OzwHItrCK36QfPzofm5EN/I2YwikgTsLHc/HehhjKkLPAt0McY8bq39+7GebK0dC4wFSElJsb4OW1XcbsubX6fxz8830rpeHGNGdKN5QozTsUTET6ggy5Hy9sKqGbByCuxd5ZlHnHwR9HnAU4rrtgSjjyZFqpFj/YO01toDwOiqDlMd5BSW8tC0FXyxbh+/69yQ567pSI0I/bgTkYrTdwyBkgJYN9dTird8DdYNDbtC/+ehwzUQq12lRKqxdKBxufuNgN0n8wLGmAHAgOTk5MrM5Yj1e3MZPT6V9OxCnhrQjpt6N8Pol3oROUkqyMHK7fKU4ZXTYN0cKC2A+CbQ50HodD0ktnY6oYhUzGKglTGmObALGAIMO5kXsNbOAeakpKTc7oN8VWbW8l08+sFK4qLCmTyqJ2c3q+N0JBHxUyrIwcRaz7SJlVM90yjy90JkPHS8FjoPgcY9ISTE6ZQichzGmMnABUCCMSYdeMpaO84Ycw/wGZ5l3t6x1q5xMGaVKylz87d563h34Ta6N6vD68O6UK9mlNOxRMSPqSAHg+ztng07Vk6FjLUQEu650K7z9Z6tn8P1g0TEH1hrhx7n+Dxg3qm+rj9PsdiXW8TdE5eyZHs2t/ZpzmOXnUl4qH7RF5HTo4IcqLK3w9qZsGamZxMPgEZnw+UveuYV19BHjyLi4a9TLBZtOcDdk5ZRUFzGq0O78LvODZ2OJCIBQgU5kByrFDfsAhf/BdoNhDrNnc0nIlIJrLWMW7CVv3+ynqZ1ajDp9h60rh/ndCwRCSAqyP5OpVhETpM/TbEoKC7j0Q9WMnflHvq1q8+LgztTMyrc6VgiEmBUkP1R9nZYO8szr1ilWOSErLUUlbrJLSolt7CUghIXxaUuisvc3j8uSg7f9h4vKfeY57ibEpcbay0vD+ni9F+pUvnLFIvNmfmMHp/K5sx8Hu1/JqPPb6El3ETEJ1SQ/UXuHlg1XaVYgpLLbckvKvMU3KJScgvLyCsqJbfI+7XQ89jh23nF5Y+VkVtYSpn75DeJCzEQGRZKZHgIkWEhRIaFUiMi1Ad/QzmRT1fv5eHpK4gIC2H8rT04JznB6UgiEsBUkKuzsmLY8AksnwhpX3g38FAplurJWkuZ2x458lrqLjca6/rVaG1BsctbdH8psnmHi3C5EpxfXHbC94+JCCUuKpya0WHERYWTEBtB84QYakaHUTMq/IjHYiNDPcXXW3oPF+CIw/fDPPfDtBqC48pcbl7830bGfLOZzo3ieXN4N5JqRTsdS0QCnApydWMt7FkByyfBqmlQmA01k6DP7+GsGzxbPYucAmstWQUlbNlfwJbMfLZkFrA5s4At+/PJLSw95dctc1tvEXZxCoO0gGektmZ0uLfIegpt07o1jjwW/ctjh0vv4cfiosJUZk9DdZ2DfCC/mHsnL2Ph5gMM69GEpwa0IzJMI/gi4nsqyNVFwX7PrnbLJ8K+1RAaCW2v9JTiFhdAiH4oSMUUlbrYfuCQpwTvL2Cztwxvycwnt+iXkdiI0BCaJdSgdb046sRGcKozOUNDDFHhoUSEeqchhHtGYSPCfpmW8MvobAiR4b+M0EZHhFIzKpwaEaGaS+qg6jgHefnOg9w5IZUDBSW8cG0nBqc0PvGTREQqiQqyk1ylsOlzTyne+Cm4y6BhV7jin561iqNrO51QqlBWQQn7couOuFDsV9MTfuMCsr25RWzZn096diG23Ehu/ZqRtEiIZUDnhrRIjKVFYgwtE2JJqh1NaIhKqVQv1lom/bSDv8xeS72akXx4Z286JMU7HUtEgowKshMy1sGyCZ4R44IMiEmEHqOhy3Co19bpdFJFistcpG7L5ttN+/luUyZrduee1PPLX0AWERpCQmwknRvV4qoujWiZGEOLhFiaJ8YQG6l/5uIfikpdPDFzNTNS0zmvdSKvXH8WtWMinI4lIkFIPzmrSmE2rP4Alk30rEIREgat+3tKcfLFEKp1PAOdtZbNmfl8u9FTiH/ckkVhqYuwEEO3prX5w6VtaJEQQ1R46JEXjOkCMvGx6jAHeWfWIUZPSGXN7lzuu6gV91/USp9wiIhjVJB9ye2CLV97plCsmwuuYqjXHi79O3QaDDFapijQZReUsCDNU4i/27SfPTlFALRIiGFwSiPObZVIz5Z1NcorjnJ6DvJXGzJ4YMpyzw55I1O4qG19J2KIiPxMP5V9IWuLZxWK5ZMhNx2iakG3kZ4L7hp0Bl2MFLBKytws25HNd95pEyt35WAt1IwKo0+rBO5rlUif5AQa16nhdFQRx7ndlte+TOPl+RtpUz+Of4/oRtO6MU7HEhFRQa40xfme3e2WT4Tt34MJgZZ9od8z0OZyCI9yOqGcojKXm6yCEjLyitmfX8z+/BIyf75dXO52CVkFJYBnZYcujWvxwEWtObd1Ap2S4jUlQqScnEOl/H7acr5cn8FVXZL421UdidYmLCJSTaggnw5rYcePsHwCrJkJJflQpwVc9H/QeSjUbOh0wqBS5nKTX1xGXlEZOYWlFJW6jrnawy8bVvx6Q4vDjx08VML+vBL25xeTdajkiFUhDosODyUxLpKE2Aia1Y3h7GZ1SIiNpG2DOHq1TCA+WvPKRY5lze4c7pywlD05hTw9sD0jejbVMn8iUq2oIJ+KnF2wYrJnGkXWZoiIhfaD4Kzh0KSnplCcpqJSF7sPFrL7YBHZh0rK7az2yy5rh3ddK3+7oMR1Su939Hq9kWEhxNcIp0ndGnRrVpuE2EgS4yJJjI34+XZCbCQxmjcsctI+SE3njx+tolaNcKaM6kW3plrOUkSqH/2EPxl7VsKCl2DtTM+2z037wHkPQ9vfQWSs0+n8Rl5RKbsOFrIru/Dnr+nl7mfmFR/zeWEh5ojd1OKiwmiREPvz9sFH77hWIyL0qA0rPJtURISG/LIyRGiIRq4k6FXFKhYlZW6embuW8T9up0fzOrw+rCuJcZE+ez8RkdOhglwR2xfCd/+CtM8hIg563QMpN3umU/gJa+1xNp5wU+I6cmOK4rJyUxNKXZS43MecYlARLmvJyC0+ohDnHLWtcURYCEm1okmqFU3fNvVIqh1No9rRNKwVTd2YiJ8Lb3S4dlsT8QVfr2KxJ6eQuyYuZdmOg4w6rwWPXNpGc/JFpFpTQT4ea2HT/zzFeOePUKMu9H0Czr4domtV+tu53ZaCkrJy0wnKyCs6cgpBXlHZcefMFpcvtEfPu/WWYqfERISSVNtTgLs2rUWj2jU8hbh2NI1qRZMQG0mI1jsVCUgLN+/n3knLKCp18eYNXbm8YwOnI4mInJAK8tFcZZ4pFAtegn2rIb4xXPYCdBkBERVbmsvttmQfKjnOagclv5pPm1tYSn5xGe4TjNJGhoX8vImEZ4rAkdMFakWHExEX+ct8Wu8Oa5HhIUSGeqYXRJafbxv+y+2I3zgeERbCqfZXgyEqXNMYRIKNtZax327h+U/X0zwhhn+P6ElyvTinY4mIVIgK8mFlxZ6L7r5/BbK3QkJrGPQWdLzuiF3uDh4qYe2eXDLzPIU3M7/459UODpfhAwUluI7RdiNCQ6gbG0F8dDg1o8NpWCuKM6PijphXW34+7S+3PV8jwvSRpIhUf/nFZfxh+go+Wb2XyzqcwT+u66zNcETEr+g7VnEeLPkv/PAG5O+Fhl29axdfQbHbsnZXLit2HmS598+2A4eOeHpEaAgJsREkxEXSID6KjknxJMRFkBgbSYJ3tYPDqx7UjArTSKqIBLS0jDzuGJ/K1v0F/PHyM7n93Bb6vicifid4C3LBAVg0Bn4aC0UHsc3PZ0/fl/nRdmDFxhyWz1/I2j25lLo8I8H14iI5q3EtBp/dmI5J8TSIjyYxNpKa0Sq9IiIAH6/cwyMzVhAVHsqE23rQu2WC05FERE6JTwqyMaY/8AoQCrxtrX3OF+/zm9xuyN8HOemQs/OIrzZnJ+zfhCkrYlOdCxhf8xpmbq1P7royYCU1IkLpmBTPLX2ac1ajWpzVpBYN4qOr/K8gIlIVTneZtzKXm+c/Xc9/vttKlya1ePOGrvqeKSJ+rdILsjEmFHgDuARIBxYbY2Zba9dW5vscOpRP1q7NlBzYgTt7B+SkE5q/i8j8XdQo3ENcyT5CbdkRz8mjBrtJJN1Vh632Qia7+rJ1TxKt68dxRadadPaW4Vb14gjVqgoiEiROZ5m3zLxi7pm0lEVbsxjRsylPXNmWyDBtGS0i/s0XI8jdgTRr7RYAY8wUYCBQqQV59bwxdF/9zM/3Xdawj9rstgnssk3ZH5JCVvgZ5EXWpyCqASWxDQirUfvnC95qx0Twt4Y16dgonhoRwTvTRETkVLncliFjfyA9u5B/XteZa7o1cjqSiEil8EUzTAJ2lrufDvSo7DdpcFZ/FofVgNpNCKvdmMg6jagZE02rqHC6RIZpBFhExMdCQwxPXNGOejUjad8w3uk4IiKVxhcF+VjN9FdrnhljRgGjAJo0aXLSb9I4uQONkzuc9PNERKTyXHhmPacjiIhUOl8srJsONC53vxGw++iTrLVjrbUp1tqUxMREH8QQERERETl5vijIi4FWxpjmxpgIYAgw2wfvIyIiIiJS6Sp9ioW1tswYcw/wGZ5l3t6x1q6p7PcREREREfEFnyzfYK2dB8zzxWuLiIiIiPiSL6ZYiIiIiIj4LRVkEZEgZ4wZYIwZm5OT43QUEZFqQQVZRCTIWWvnWGtHxcdrLWMREVBBFhERERE5ggqyiIiIiEg5xtpfbXJX9SGMyQS2O53jFCQA+50O8f/t3U+opXMcx/H3p7nEjIREzMhQ8iel0SyGKclYKDI2yoImWYoZKWFjayGxUhp/pkwjXVMkiYaym2JGGa5SaFyGOyV/skE+Fs9z62lWOtfz/O74fl6bc+6zuH2+95zzud97znPuaajy/JVnh9rzr2T2i22v2k9GSheflCrPDrXnrzw7zD7/v+rhVbEgn6wkfWR7c+scrVSev/LsUHv+yrOvVpVvk8qzQ+35K88O48+fUywiIiIiIgayIEdEREREDGRBXpnnWwdorPL8lWeH2vNXnn21qnybVJ4das9feXYYef6cgxwRERERMZBnkCMiIiIiBrIgR0REREQMZEGegaSLJH0gaUHSZ5J2ts40NUlrJB2W9FbrLFOTdJakeUlf9PeB61pnmoqkh/r7/BFJ+ySd1jrTmCS9KGlJ0pHBsXMkvSfpy/7y7JYZq0oPd6p2ceUehnRxf2zULs6CPJu/gIdtXwlsAe6XdFXjTFPbCSy0DtHIs8A7tq8ArqHIz0HSeuBBYLPtq4E1wF1tU43uZeCWE449ChywfRlwoP86ppce7lTt4pI9DOnigVG7OAvyDGwfs32ov/4b3QNzfdtU05G0AbgV2N06y9QknQncALwAYPsP2z+3TTWpOeB0SXPAWuD7xnlGZftD4KcTDm8H9vTX9wB3TBoqgPQw1O3i9DCQLoaRuzgL8gpJ2ghsAg62TTKpZ4BHgL9bB2ngUuA48FL/suZuSetah5qC7e+Ap4CjwDHgF9vvtk3VxPm2j0G3pAHnNc5TXtEehrpdXLaHIV08MGoXZ0FeAUlnAK8Du2z/2jrPFCTdBizZ/rh1lkbmgGuB52xvAn6nyEvs/fld24FLgAuBdZLubpsqqqvYw1C+i8v2MKSLp5IFeUaSTqEr5b2297fOM6GtwO2SvgFeBW6S9ErbSJNaBBZtLz9TNU9X1BXcDHxt+7jtP4H9wPWNM7Xwo6QLAPrLpcZ5yircw1C7iyv3MKSLl43axVmQZyBJdOc+Ldh+unWeKdl+zPYG2xvp3hTwvu0yf7na/gH4VtLl/aFtwOcNI03pKLBF0tr+MbCNQm+MGXgT2NFf3wG80TBLWZV7GGp3ceb0hosAAACoSURBVPEehnTxslG7eO6//GaFbAXuAT6V9El/7HHbbzfMFNN5ANgr6VTgK+DexnkmYfugpHngEN1/EDjM//yjTiXtA24EzpW0CDwBPAm8Juk+ul9Ud7ZLWFp6uLaSPQzp4qm6OB81HRERERExkFMsIiIiIiIGsiBHRERERAxkQY6IiIiIGMiCHBERERExkAU5IiIiImIgC3JERERExEAW5IiIiIiIgX8AqRRrNMa9B9sAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[181]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">figsize</span> <span class="o">=</span> <span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">5</span><span class="p">))</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticks</span><span class="p">([</span><span class="mi">1</span> <span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">10</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">([</span><span class="sa">r</span><span class="s1">&#39;a&#39;</span><span class="p">,</span> <span class="sa">r</span><span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="sa">r</span><span class="s1">&#39;$\gamma$&#39;</span><span class="p">,</span> <span class="sa">r</span><span class="s1">&#39;$\delta$&#39;</span><span class="p">],</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">18</span><span class="p">)</span>

<span class="n">ax</span><span class="o">.</span><span class="n">set_yticks</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mi">500</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[181]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.axis.YTick at 0x197670f06a0&gt;,
 &lt;matplotlib.axis.YTick at 0x197670fff28&gt;,
 &lt;matplotlib.axis.YTick at 0x197670ec978&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[185]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">matplotlib</span> <span class="k">import</span> <span class="n">ticker</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[189]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s1">&#39;Scientific Notation&#39;</span><span class="p">)</span>

<span class="n">formatter</span> <span class="o">=</span> <span class="n">ticker</span><span class="o">.</span><span class="n">ScalarFormatter</span><span class="p">(</span><span class="n">useMathText</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">formatter</span><span class="o">.</span><span class="n">set_scientific</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">formatter</span><span class="o">.</span><span class="n">set_powerlimits</span><span class="p">((</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">))</span>
<span class="n">ax</span><span class="o">.</span><span class="n">yaxis</span><span class="o">.</span><span class="n">set_major_formatter</span><span class="p">(</span><span class="n">formatter</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAW8AAAEICAYAAACQzXX2AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAIABJREFUeJzt3Xl8VOXZ//HPRVYChBBIghD2HZRFkMW9ilRbqz5Wiru2KlafLlq7WJ+2Ll2eqq2P1lr9KW6tCLi21rYsKriDLEYk7EsgYUnCkhCWhCzX748ZaqQIA2RyMpPv+/XKKzPnnDnnysnkmzP3uc99zN0REZHY0iLoAkRE5MgpvEVEYpDCW0QkBim8RURikMJbRCQGKbxFRGKQwlsanJnlm9mZUVr3v8zsmnrPf2VmW81si5l1NbNdZpYQjW1Hk5mdZmYrgq5DYofCW76QmZ1qZh+YWbmZbTez983spMO9zt0HufucBtj+XWb23AHrPs/dnw3P7wLcBgx0947uvsHdW7t77RFu51ozczP70QHTiyL5J2RmZ5pZ0RFu082s9/7n7v6uu/c7knVI86bwloMys3TgdeBhIBPoDNwNVAVZ1wG6AdvcvaQB1rUd+En45xZp8mIuvM3sIjN7wsz+Zmbjgq4njvUFcPcp7l7r7nvdfaa7L96/gJndYGbLzKzCzJaa2Ynh6QVmNjb8uIWZ3W5ma8xsm5m9YGaZ4Xndw0eg15jZhnDzx/+E550L3AFMCDeFfBKePsfMrg+vfxbQKTz/mXrrSwwvm2lmT5vZJjPbYWZ/PcTPuwz4ELj1YDPNLMXMHgyva1P4cYqZtQL+Va+OXWbWycxGmtmHZlZmZpvN7I9mlhxe1zvh1X4SXn7CgUfvZjYg/LOWhZuhLqg37xkze8TM/hHe9/PMrFekv1iJE+4e6BfwFFACLDlg+rnACmA1cPtBXtcOeDLo+uP1C0gHtgHPAucB7Q6YPx7YCJwEGNAb6BaeVwCMDT++BZgL5AIpwP8DpoTndQcceAJoCQwhdGQ/IDz/LuC5A7Y7B7g+/PhMoKjevP3rSww//wcwLfxeSQLO+IKf9VrgPWAoUAZkhqcXAWeGH98T/jmygSzgA+CXB6sjPG04MBpIDNe1DLil3nwHetd7/u91hGtdTeifVzJwFlAB9AvPf4bQJ4WR4fVPBqYG/Z7RV+N+Rf3I28yyzazNAdN613v6DKGgrj8/AXiEUGgMBC4zs4EHrPpn4WUkCtx9J3Aqn4VrqZm9ZmY54UWuB+5z9/kestrd1x9kVTcC/+PuRe5eRSiQL9l/dBx2t4eO7D8BPiEU4sfEzI4j9P75trvvcPdqd3/7UK9x9zxgJvCTg8y+ArjH3UvcvZRQE9JVh1jXQnef6+417l5A6J/WGRGWPxpoDfzW3fe5+1uEmrAuq7fMK+7+kbvXEArvoRGuW+JEYzSbnAH8zcxSIfRRG/jD/pnu/g6ho4j6RgKr3X2tu+8DpgIXhl9vZnYv8C93X9QI9Tdb7r7M3a9191zgeKAT8GB4dhdgTQSr6Qa8Gv74X0boCLQWyKm3zJZ6j/cQCq5j1QXY7u47jvB1vwBuMrOOB0zvBNT/57Q+PO2gzKyvmb0e7gWzE/gN0CHCGjoBhe5ed8D2Otd7Ho19JjEk6uHt7i8C04GpZnYF8C3gG4d5WWegsN7zIj57434XGEvo6O3bDVyufAF3X07oU9Lx4UmFQCTtrIXAee6eUe8r1d03RrLZo6v239vNNLOMI3lR+Od8hVCTRX2bCP0j2q9reBocvM5HgeVAH3dPD6/PIixjE9DFzOr/fXYl1EwlAjTSCUt3vw+oJPSGvsDddx3mJQd7k3t4XX9w9+Hu/m13f6yBS5UwM+tvZreZWW74eRdCH9vnhheZBPzQzIaHPw31NrNuB1nVY8Cv988zsywzuzDCMoqB7geEWETcfTOhE4l/MrN2ZpZkZqdH+PK7gW8C9YN/CvCzcP0dCB2h7+/GWAy0N7O29ZZvA+wEdplZf+CmA7ZRDPT8gu3PA3YDPw7XfSbwNUKfQEWARgpvMzuN0BHbq8CdEbykiNDH3v1y+ewoRxpHBTAKmGdmuwmF9hJC/ar3f6L6NfB8eNm/EupSeKCHgNeAmWZWEV7PqAhreDH8fZuZHU0T2VVANaEj4BJCJ08Py93XAX8BWtWb/CtgAbAY+BRYFJ62/2h9CrA23DzUCfghcDmhffMEoROn9d0FPBte/nOfRMNNhRcQarPfCvwJuDq8HREAzD26N2Mws2GE3thfBdYROlpZ6+4/q7dMd+B1dz8+/DwRWAmcTeij4nzgcnfPj2qxIiIxojGOvNOA8e6+JnwC5hrqnfgxsymE+tf2s9AVbdeFz6B/B5hB6ATXCwpuEZHPRP3IW0REGl7MXWEpIiIKbxGRmJR4+EWOTocOHbx79+7RWr2ISFxauHDhVnfPOtxyUQvv7t27s2DBgmitXkQkLpnZwYaZ+A9qNhERiUEKbxGRGBRRs4mZFRC6UqwWqHH3EdEsSkREDu1I2ry/5O5bo1aJiIhErEGbTcxsopktMLMFpaWlDblqERGpJ9LwdkIDCy00s4lfuJD74+4+wt1HZGUdtqeLiIgcpUibTU5x901mlg3MMrPl4ZsoiIhIACI68nb3TeHvJYSGdR0ZzaJERGLRzspq7notn11VNVHf1mHD28xa7b8HZfhO2eMIjessIiJhBVt3c/GfPuC5uetZUHDgnR0bXiTNJjmE7kG4f/nn3X16VKsSEYkhH6zZys2TQ/cL+ct1oxjTq33Ut3nY8Hb3tTTA3bxFROLRX+au5+7X8unRoRVPXnMSXdunNcp2oza2iYhIPKuureOevy/lL3PXc1b/bB66dChtUpMabfsKbxGRI1S2Zx83T17EB2u2cePpPfnxuf1JaHGw+6ZHj8JbROQIrC6p4PpnF7CprJLfjR/CJcNzA6lD4S0iEqHZK0r43vMfk5LUgikTRzO8W7vAalF4i4gchrvz5Hvr+M0/l9G/YzpPXDOCzhktA61J4S0icghVNbX8/K9LeGFBEecO6sgDE4aQlhx8dAZfgYhIE7V1VxU3PbeQ+QU7+N7Zfbjl7D60aOQTk19E4S0ichDLNu/k+mcXsHVXFQ9fNoyvDekUdEmfo/AWETnAjPwt3Dotjzapibz47TEMzs0IuqT/oPAWEQlzd/40Zw33z1jBkNy2PH71CHLSU4Mu66AU3iIihIL7N/9cxhPvruPCoZ249+uDSU1KCLqsL6TwFhEBHpi1kifeXcc1Y7px1wWDCA/G12Tp7vEi0uw9/OYqHn5rNZeN7MKdX2v6wQ0KbxFp5h5/Zw2/n7WSi4d15tcXndBkugIejsJbRJqtZz8o4Df/XM5XBx/HfZcMjpngBoW3iDRTUz7awJ2v5XPOwBwenDCUxITYisPYqlZEpAG8vLCIO179lDP7ZfHHy4eRFGPBDQpvEWlm/v7JJn700iec3Ks9j105nJTEptsd8FAU3iLSbMzI38It0/IY0S2TJ64e0aT7cR+OwltEmoXZy0v4zvOLGJzblqe+eVKTGBnwWCi8RSTuvb96Kzc+t5B+HdvwzDdH0joltoMbFN4iEufmrd3Gdc/Op2eHVvzlW6No27LxbhIcTQpvEYlbizbs4FvPzKdzRkueu34U7VolB11Sg1F4i0hc+rSonGue+ogObVJ4/obRdGidEnRJDUrhLSJxZ9nmnVz11DzSU5N4/obRTXZY12Oh8BaRuLK6pIIrJ80jNTGBKTeMDvxGwdGi8BaRuLG2dBeXPzEPM+P5G0bRtX1a0CVFjcJbROLC6pJdXPr4XGrrnOdvGEXPrNZBlxRVsd/ZUUSavVXFFVz2xDwApk4cTZ+cNgFXFH068haRmLZiSwWXPj6XFtZ8ght05C0iMWzppp1c+eQ8khKMKTeMjvumkvp05C0iMWnJxnIunzSXlMQWTJs4plkFNxxBeJtZgpl9bGavR7MgEZHDWVxUxuVPzKVVciLTJo6he4dWQZfU6I7kyPv7wLJoFSIiEom8wjKumDSP9JZJTJ04Oq67Ax5KROFtZrnAV4FJh1luopktMLMFpaWlDVGfiMi/LVy/g6smzaNdWjLTbhxDl8zmGdwQ+ZH3g8CPgbpDLeTuj7v7CHcfkZWVdczFiYjsN79gO1c/OY/2rZOZdmP8XjkZqcOGt5mdD5S4+8JGqEdE5D/MW7uNa576iJz0VKbdOIbj2jbv4IbIjrxPAS4wswJgKnCWmT0X1apERMI+WLOVa5+ez3FtU5k6MT4HmToahw1vd/+pu+e6e3fgUuAtd78y6pWJSLP33qqtfOuZ+eS2a8nUiWPIVnD/m/p5i0iT9PbKUq57dj7d27diysTRZLWJr/G4j9URXWHp7nOAOVGpREQkbPbyEm58biG9sloz+fpRZMbRHXAaii6PF5Em5Y2lxdw8eRF9O7bmuetGkZGm4D4YhbeINAnuznPzNnDP3/MZcFx66GbBafFxs+BoUHiLSODK91Tzk5cXMz1/C6f3zeLhy4bFzV3eo0XhLSKBWlCwne9PzaN4ZyV3fKU/15/akxYtLOiymjyFt4gEorbOeXTOav7vjVV0zmjJSzedzNAuGUGXFTMU3iLS6Ip3VnLL1Dw+XLuNrw3pxK//63jSU9VMciQU3iLSqGYvL+G2Fz9h775a7vv6YMaPyMVMzSRHSuEtIo1iX00d901fzqT31tG/Yxv+ePkwemc3j1uWRYPCW0SirmDrbr475WM+3VjO1WO6ccdXBpCalBB0WTFN4S0iUfXqx0X87NUlJCa04LErh3Pu8R2DLikuKLxFJCp2V9Xwi7/l8/KiIk7q3o4HLx3W7MfgbkgKbxFpcPmbyvnu8x+zbttuvnd2H753Vm8SEzQOXkNSeItIg6mrc579sID//edy2rVKYvL1ozi5V4egy4pLCm8ROWbuzlvLS/j9zJUs3byTs/tnc//4IRoNMIoU3iJy1Nyd91Zv5fczV5JXWEa39mk8OGEoFw7tpL7bUabwFpGj8tG67fxu5go+WredzhktuffrJ3DxibkkqW27USi8ReSI5BWW8fuZK3h31Vay26Rwz4WDmHBSF1IS1W+7MSm8RSQiSzft5IFZK3ljWTGZrZL5n68M4MrR3WiZrNAOgsJbRA5pdUkF/zdrFf/4dDPpqYn8cFxfrj2lB61TFB9B0t4XkYNav203D72xir/mbaRlUgLfO6s3153WUzdJaCIU3iLyORvL9vLHt1bxwoIikhKMG07ryY1n9FK3vyZG4S0i/zZnRQkT/7wQgKtGd+PmM3uRnZ4acFVyMApvEQFg664qfvjiJ/TMasWT156kcUiaOIW3iODu3P7yYnZW1jD5+tEK7hig3vQiwpSPCnljWQm3n9uffh11g4RYoPAWaebWlu7il68v5bQ+Hbj25O5BlyMRUniLNGPVtXXcMi2PlKQW/G78EFq00HgksUJt3iLN2B/eXMXionIeu/JEctSrJKboyFukmZpfsJ1HZq9m/PBczj3+uKDLkSOk8BZphioqq7l1Wh657dK484JBQZcjR0HNJiLN0F2vLWVT2V5e/PYYjVESow575G1mqWb2kZl9Ymb5ZnZ3YxQmItHxj8WbeXlREd85qw/Du2UGXY4cpUj+5VYBZ7n7LjNLAt4zs3+5+9wo1yYiDWxz+V7uePVThnTJ4Ltn9Q66HDkGhz3y9pBd4adJ4S8/2LJmNtHMFpjZgtLS0gYsU0SOVV2d88MXP2FfTR0PThiqO97EuIh+e2aWYGZ5QAkwy93nHWw5d3/c3Ue4+4isrKyGrFNEjtFT76/j/dXb+MXXBtKjQ6ugy5FjFFF4u3utuw8FcoGRZnZ8dMsSkYa0bPNO7pu+gnMG5nDpSV2CLkcawBF9bnL3MmAOcG5UqhGRBldZXcstU/NIb5nEby8+QXd1jxOR9DbJMrOM8OOWwFhgebQLE5GGcf+MFaworuD+8YNp3zol6HKkgUTS2+Q44FkzSyAU9i+4++vRLUtEGsJ7q7by5HvruHpMN77ULzvocqQBHTa83X0xMKwRahGRBrRj9z5uezGP3tmt+el5A4IuRxqY+gqJxCF3545XP2X77n08OGEoLZMTgi5JGpjCWyQOvbxoI/9asoUfnNOP4zu3DbociQKFt0ic2bBtD3f+bQkje2Qy8fSeQZcjUaLwFokjNbV13PpCHi1aGP83YSgJurlC3NJwYiJxYvmWndzxyqcs2lDGgxOG6ibCcU7hLRLj9u6r5Q9vreKJd9bSJjWRB74xhIuGdQ66LIkyhbdIDJuzooSf/20Jhdv3Mn54Lj/9ygAyWyUHXZY0AoW3SAwq2VnJPa8v5fXFm+mV1YqpE0czumf7oMuSRqTwFokhdXXO5I82cN/05VTV1PGDc/py4xk9SUlUP+7mRuEtEiOWbd7JHa9+yscbyji5V3t+ddHx9MxqHXRZEhCFt0gTt2dfDQ+9uYpJ766jbcskHvjGEP5rWGeNDtjMKbxFmrDZy0MnJIt27GXCiC7cfl5/2umEpKDwFmmSindWcs/fl/KPT0MnJKdNHM0onZCUehTeIk1IXZ0zed567pu+gqraOm47py8TdUJSDkLhLdKEPP1BAb98fSmn9G7Pry46QfealC+k8BZpIsr3VvPwW6s4rU8H/vytkTohKYekgalEmoj/9/YayvZUc/t5/RXcclgKb5EmYEt5JU+9v44Lh3ZiUCeNvy2Hp/AWaQIeenMltXXObef0C7oUiREKb5GArS7ZxbT5hVwxqhtd26cFXY7ECIW3SMDun7GctOREvntW76BLkRii8BYJ0ML1O5iRX8zE03vSvnVK0OVIDFF4iwTE3bn3X8vp0DqF607tEXQ5EmMU3iIBmb2ihI8KtvP9sX1olaJLLuTIKLxFAlBb59z7rxV0b5/GpSd1CbociUEKb5EAvPrxRlYUV/CjL/cnKUF/hnLk9K4RaWSV1bU8MHMFg3Pb8pUTOgZdjsQohbdII/vLh+vZVF7J7efqMng5egpvkUZUvreaP85ezel9szi5d4egy5EYpvAWaUSPvb2G8r3V/ORcXQYvx0bhLdJItpRX8tR767hIg09JA1B4izSSB99YSZ07t43TUbccu4jC28y6mNlsM1tmZvlm9v1oFyYST1aXVPDCgkKuHN2NLpkafEqOXaSXddUAt7n7IjNrAyw0s1nuvjSKtYnEjfumryAtOZHvfEmDT0nDiOjI2903u/ui8OMKYBnQ+cDlzGyimS0wswWlpaUNW6lIjFq4fgczlxZzowafkgZ0xG3eZtYdGAbMO3Ceuz/u7iPcfURWVtaxVycS4z43+NRpGnxKGs4RhbeZtQZeBm5x953RKUkkfry1/LPBp9KSNfiUNJyIw9vMkggF92R3fyV6JYnEh9o6597pyzX4lERFpL1NDHgSWObuD0S3JJH48MqiIlYW79LgUxIVkb6jTgGuAs4ys7zw11eiWJdITKusruWBWSsZosGnJEoiaoRz9/cAjaAjEqE/f1jA5vJKfv+NIRp8SqJCn+VEGlj5nmoemb2GM/pmcXIvDT4l0aHwFmlgj769hp2V1fzk3P5BlyJxTOEt0oAKt+/h6ffXcdHQzgzslB50ORLHFN4iDWTu2m38158+IKGF8YNz+gZdjsQ5hbfIMXJ3Hnt7DVdMmkd6aiKv3nyKBp+SqNMlXyLHoHxvNT988RNmLS3mKyd05N6vD6ZNalLQZUkzoPAWOUpLN+3kpskL2bhjLz8/fyDfOqW7ugVKo1F4ixyFFxcU8rO/LiEjLYmpE0czontm0CVJM6PwFjkCldW13PVaPlPnF3Jyr/Y8dOkwstpomFdpfApvkQht2LaHmyYvJH/TTv77S734wTn9SGihZhIJhsJbJAJvLC3mBy/kATDp6hGMHZgTcEXS3Cm8RQ6hpraOB2at5E9z1jCoUzqPXjGcru3VDVCCp/AW+QKlFVV8b8rHfLh2G5eN7MKdXxtEalJC0GWJAApvkYNaULCd/35+EWV7qrn/ksGMH6GbKUjTovAWqcfdeer9Av73n8vo3K4lr948UmOUSJOk8BYh1AXwrx9v5JkPCli+pYJxA3O4f/wQ2rbU1ZLSNCm8pVnbVLaXv8xdz5SPNlC2p5oBx6Xz+/FDuPjEzrpaUpo0hbc0O+7OwvU7ePqDAqYv2YK7M25gR649pTujemQqtCUmKLyl2aiqqeUfizfz9PsFfLqxnPTURK47tQdXje6mUQAl5ii8Je6VVFQyee4GJs/bwNZdVfTKasUvLzqer5/YmbRk/QlIbNI7V+LW4qIynn6/gNcXb6K61vlSvyy+eUoPTuvTQU0jEvMU3hJXamrrmJ6/haffL2Dh+h20Sk7gilHduObk7vTo0Cro8kQajMJb4oK7M33JFu6fuYK1pbvpmpnGz88fyPgRuaTr5ggShxTeEvPeW7WV+2YsZ3FROb2zW/PoFScyblBHjfgncU3hLTErr7CM+6Yv54M12+ic0ZL7LxnMxSfmKrSlWVB4S8xZXVLB72asZHr+FjJbJfOL8wdyxeiupCRq0ChpPhTeEjM2lu3lwVkreXlREWnJidw6ti/XndaD1il6G0vzo3e9NHnbdlXxyOw1PDd3PRh885Qe3HxmL9q31u3HpPlSeEuTVVFZzaR31zHp3bXsra7lkuG5fH9sXzpntAy6NJHAKbylyamsrmXyvA08Mns123fv47zjO3LbuL70zm4TdGkiTYbCW5qUGflbuPu1fDaVV3Jq7w786Mv9GNIlI+iyRJqciMLbzJ4CzgdK3P346JYkzdGuqhru+Xs+LywoYsBx6dx3yRBO7dMh6LJEmqxIj7yfAf4I/Dl6pUhztXD9dm6d9gmFO/Zw85m9uGVsX5ITWwRdlkiTFlF4u/s7Ztb9cMuZ2URgIkDXrl2PqTCJf9W1dfzhzVU8Mns1x7VtybSJYxjZIzPoskRiQoO2ebv748DjACNGjPCGXLfElzWlu7h1Wh6Li8r5+om53HXBQNpoDBKRiOmEpTQqd+e5eRv49T+WkpqUwKNXnMh5JxwXdFkiMUfhLY2mpKKSn7y0mNkrSjm9bxb3XzKYnPTUoMsSiUkKb2kUM/K38NNXPmV3VQ13XzCIq8d00w0RRI5BpF0FpwBnAh3MrAi4092fjGZhEh92VdXwy78vZdqCQgZ1SufBCUPpk6OLbUSOVaS9TS6LdiESfxau38Gt0/LUBVAkCtRsIg2uuraOh99cxR9nr6ZTRkteuHEMJ3VXF0CRhqTwlgbh7hTt2EteYRmT3l3LJ+oCKBJVCm85Kjsrq1lcWE5e4Q7yCsvIKyxj6659AGS2SlYXQJEoU3jLYdXU1rGiuCIU0htCQb26dBcevgyrZ1YrzuibzdCuGQzrkkG/jm1ISlDbtkg0KbzlP2wu30vehjI+Dof1pxvL2VtdC0C7tCSGdW3H14Z0YmiXDIbkZtA2Tc0iIo1N4S3U1NaxYP0O3lxWzJvLSli7dTcAyQktGNgpnQkndWFY1wyGdsmga2aa+meLNAEK72aqfG81b68s5c1lxcxZUUr53mqSEozRPdtz+aiuDO/WjoGd0nVTX5EmSuHdjBRs3c0b4aPr+QXbqalz2qUlcfaAbMYOyOG0Ph3UM0QkRii841hNbR2LNpTx5rJi3lhWzJrSUHNIn+zWXH9aT8YOyGZY13YktFAziEisUXjHmfK91by3aitvLCtm9ooSyvZUk9jCGNUzkytGdWPsgBy6tk8LukwROUYK7xhXW+csLirjnZVbeWdVKXmFZdTWORlpSXypXzZnD8jm9L5ZpKs5RCSuKLxj0Obyvby7citvryrl/dVbKdtTjRmc0LktN53RizP6ZTGsSwaJ6mstErcU3jGgsrqWeeu2887KUt5ZWcqqkl0AZLdJYeyAHE7vm8WpvTuQ2So54EpFpLEovJsgd2dVyS7eWVnK2ytL+Wjddqpq6khObMGoHpmMH5HL6X2z6JfTRn2uRZophXcTUVVTy4drtjFzaTFvLSthy85KAHpnt+aKUd04vW8HRvVoT8tk9bsWEYV3oCoqq5mzopSZS4uZs7yEiqoaWiUncHrfLM7om8VpfbPonNEy6DJFpAlSeDey0ooqZi0tZubSLXywehv7auto3yqZrw4+jnGDcji5VwdSk3R0LSKHpvBuBAVbdzNz6RZm5BezaMMO3KFrZhrXnNyNcYM6cqIulBGRI6TwjgJ3Z8nGncxcuoWZ+cWsKK4AYFCndG4d25dxg3J0slFEjonCu4HU1NbxUcF2ZuYXMzN/C5vKK2lhMLJHJr84fyDjBuWQ205XNopIw1B4H4PK6lreWVnKjPxi3lxeTNmealISW3BanyxuPacvZw/IUd9rEYkKhfcRKt9TzVsripmxpJi3V5ayt7qW9NREzh6Qw5cHhS6YSUvWbhWR6FLKRGBLeSWzwicc567dRk2dk5OewiXDc/nyoI6M6pmp236JSKNSeH+BNaW7mJEfOuGYV1gGhO7VeMPpPRk3MIchuRm0UA8REQmIwruezeV7eWlBEX/7ZBOrw+OHDM5ty4++3I8vD8qhd3abgCsUEQlp9uFdXVvH7OUlTJ1fyJwVJdQ5jO6ZyVWjB3HOwBw66QpHEWmCmm14r9+2m2nzC3lxYRGlFVVkt0nhpjN7MWFEV92sQESavGYV3pXVtczI38K0+YV8sGYbLQzO6p/NhJO68qV+WRr/WkRiRrMI7xVbKpg6fwOvfryRsj3VdMlsyQ/H9eWS4V3o2DY16PJERI5Y3Ib37qoaXl+8ianzC/l4QxnJCS0YNyiHS0/qysm92quniIjEtJgPb3enoqqGkp1VlFRUUlpRxdy123ktbyO799XSO7s1P/vqAC4+MVdXO4pI3Giy4e3ulO2ppqQiFMolO6soDn8v3T+toorinZVUVtd97rUtkxI4f/BxXDqyCyd2bacBoEQk7kQU3mZ2LvAQkABMcvffRqugB2at5OVwD5B9tXX/Mb91SiLZbVLIapPC4NwMctqkkJ2eQnabVLLDjztnpOmOMyIS1w4b3maWADwCnAMUAfPN7DV3XxqNgjqmpzKqRyZZ9QO5TQo56alkp6do3BARESI78h4JrHb3tQBmNhVWdrDVAAADmklEQVS4EPiP8DazicBEgK5dux5VQZeP6srlo47utSIizUUkHZs7A4X1nheFp/0Hd3/c3Ue4+4isrKyGqE9ERA4ikvA+2Nk+b+hCREQkcpGEdxHQpd7zXGBTdMoREZFIRBLe84E+ZtbDzJKBS4HXoluWiIgcymFPWLp7jZl9B5hBqKvgU+6eH/XKRETkC0XU787d/wn8M8q1iIhIhDSMnohIDFJ4i4jEIHOPTq8/MysF1kdl5Y2nA7A16CKaEO2Pz2hffJ72x+cdy/7o5u6HvVAmauEdD8xsgbuPCLqOpkL74zPaF5+n/fF5jbE/1GwiIhKDFN4iIjFI4X1ojwddQBOj/fEZ7YvP0/74vKjvD7V5i4jEIB15i4jEIIW3iEgMUngfhJl1MbPZZrbMzPLN7PtB1xQ0M0sws4/N7PWgawmamWWY2Utmtjz8HhkTdE1BMbNbw38jS8xsipmlBl1TYzKzp8ysxMyW1JuWaWazzGxV+Hu7aGxb4X1wNcBt7j4AGA38t5kNDLimoH0fWBZ0EU3EQ8B0d+8PDKGZ7hcz6wx8Dxjh7scTGrju0mCranTPAOceMO124E137wO8GX7e4BTeB+Hum919UfhxBaE/zoPePag5MLNc4KvApKBrCZqZpQOnA08CuPs+dy8LtqpAJQItzSwRSKOZjfXv7u8A2w+YfCHwbPjxs8BF0di2wvswzKw7MAyYF2wlgXoQ+DFQF3QhTUBPoBR4OtyMNMnMWgVdVBDcfSPwO2ADsBkod/eZwVbVJOS4+2YIHQgC2dHYiML7EMysNfAycIu77wy6niCY2flAibsvDLqWJiIROBF41N2HAbuJ0sfipi7clnsh0APoBLQysyuDrar5UHh/ATNLIhTck939laDrCdApwAVmVgBMBc4ys+eCLSlQRUCRu+//JPYSoTBvjsYC69y91N2rgVeAkwOuqSkoNrPjAMLfS6KxEYX3QZiZEWrTXObuDwRdT5Dc/afunuvu3QmdjHrL3Zvt0ZW7bwEKzaxfeNLZwNIASwrSBmC0maWF/2bOppmevD3Aa8A14cfXAH+LxkYiupNOM3QKcBXwqZnlhafdEb6jkMh3gcnhe7quBb4ZcD2BcPd5ZvYSsIhQD62PaWaXyZvZFOBMoIOZFQF3Ar8FXjCz6wj9gxsflW3r8ngRkdijZhMRkRik8BYRiUEKbxGRGKTwFhGJQQpvEZEYpPAWEYlBCm8RkRj0/wHfoZS4Csv+YwAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>

