Simple
======

./gst-gendcparse-launch gendcseparator ! videoconvert ! xvimagesink

Format filter
=============

./gst-gendcparse-launch gendcseparator ! video/x-raw,format=GRAY16_LE,depth=12 ! videoconvert ! xvimagesink
