# widevine-L3-WEB-DL-Script
This is a script created to WEB-DL L3 Widevine Content.

Last Updated September 3, 2021.

## Scirpts
webdl.py - Uses yt-dlp

webdl2.py Uses N_m3u8
Use Command python webdl2.py -o FILENAME

## Notes For webdl2.py Script
You WIll need to Edit The Script to mach the Audio you are Selecting.

Example 

encrypted(Audio).m4a and decrypted(Audio).m4a = ACC Audio

encrypted(Audio).ac3 and decrypted(Audio).ac3 = AC3 Audio

encrypted(Audio).eac3 and decrypted(Audio).eac3 = E-AC3 Audio

Chnage All secetion in the script to match the Audio Selected

## How to use
### Requirements
* Python and pip
* Widewine Key Gyesser
  * Download zip from https://github.com/parnexcodes/widevine-l3-guesser-modified
  * Activate developer mode in Chrome Extensions
  * Use "Load unpacked" to load the extracted extension folder
* pyfiglet
  * `pip install pyfiglet`
* rich
  * `pip install rich`

### Get the keys
Go to the protected stream you want to download. Activate the plugin (restart may be required after installing the extension) and download the extracted keys (keys.json).

### Decode the video
Download the widevine-L3-WEB-DL-Script from here (Code -> Download zip). Copy the downloaded keys.json file to the same folder.

Run the downloader with `python webdl.py -o <name_without_extension>` from the folder you downloaded and extracted the script from.

The script will look in the keys.json file, starting from the second element in the JSON array. If the script can't find any keys, either modify the script (line 27 and 31), or the keys.json. See <https://gist.github.com/parnexcodes/74fef2e33a2171031000a97c371a1a65> for examples for some common use cases.

If there are multiple `mpd_url`s in the file and it isn't working, try changing them around. You can also change the `mpd_url` for a custom one if you have one.

### Options
-id and -s are optional (**id** to manually enter video and audio id from ytdl, **s** for subtitle url.). **Subtitle part is bugged right now**. **Not Applicable to webdl2.py script**.

## Report Issues

Open Issue on Github if you get any problem.
