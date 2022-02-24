# youtube-mp3-split
Split large mixtapes from Youtube by their timestamps

## Prerequisite

1. Python 3.6
2. `ffmpeg`
3. `youtube-dl` (Optional)

## How to use

The best way to use it would be to use the following sample

1. Download the `.mp3` of a Youtube video. The best way to download would be to use `youtube-dl`

	`youtube-dl --extract-audio --audio-format mp3 https://www.youtube.com/watch?v=0QKQlf8r7ls`

2. Copy the time stamp details from the "Details" section of the video or from the comments
3. **OPTIONAL**
	* Create a time stamp file in a `.csv` file format with separator as `|`
	* I have supplied a sample time stamp file for the above URL. The name of the file is `song_list.csv`
4. Use the following command

	`python3 time_split.py "%s" big_file.mp3`
	
	Replace the %s with either a path to a csv file formatted as stated before, or text pasted from the clipboard, making sure that whichever you choose 
	that it is wrapped in double quotes.
	
5. All `.mp3`s will be generated in the current working directory

PS: If you want your song to include the artist and/or album name, use the arguments -aa and -al respectively after the above.

## Disclaimer

This is a very basic first attempt at creating such a script. There might be bugs and un-handled exceptions `;_;`
