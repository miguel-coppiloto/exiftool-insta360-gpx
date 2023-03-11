# exiftool-insta360-gpx

Generate .gpx file having Insta360 video (.insv)

Capturing 360 video with the [Insta360 ONE RS 1' 360 edition](https://www.insta360.com/product/insta360-oners/1inch-360) and then upload to Google Street View (in Google Street View Studio). Steps:

1) Capture the 360 video (in this case using the [Insta360 GPS Action Remote](https://store.insta360.com/product/gps-action-remote?c=2156))
2) Transfer files to an external storage drive
3) Export 360 video file as .mp4 (no trim) in the Insta360 Studio (Direction Lock must be enabled)
4) Create the .gpx file with [exiftool](https://exiftool.org) like this `exiftool -m -ee -api largefilesupport -p gpx.fmt VID_20230309_101944_00_001.insv > VID_20230309_101944_00_001.gpx`
5) Go to [Google Street View Studio](https://streetviewstudio.maps.google.com/) and upload the .mp4 & .gpx files.
6) Wait...


Check GPS data in the 360 video:
![check-gps-data-in-video](images/check-gps-data-in-video.png)

Enable `Direction Lock`:
![enable-direction-lock](images/enable-direction-lock.png)

Export as .mp4:
![export-video360-as-h265](images/export-video360-as-h265.png)

Create .gpx file (warning shows up):
![bash-warning-truncate](images/bash-warning-truncate.png)
