PAModDetails
============

A place to define additional details and media for PA mods. This additional data can be used by anything that wants to read it (websites, PA Hub plugins, etc).

* The format is a json array with an entry per mod, mirroring the format of the main mod json found here: https://pamm-mereth.rhcloud.com/api/mod
* The only required element for an entry in the list is the mod identifier

#youtube tag

Any number of youtube videos can be defined for a mod, within a json array under the youtube tag like this:

"youtube":[{video_1_details},{video_2_details},...,{video_n_details}],

The tags currently defined for a video are as follows:

* video (required): The youtube code that identifies the video
* desc (optional): A short plaintext description of the video
* list (optional): A youtube playlist that the video is a member of
* time (optional): A time in seconds to begin playback from, relative to the start of the video
* type (optional): Defining the type of video, such as Gameplay, Tutorial, etc. Tutorial defines a video where the mod is the central focus of the video, the video was made to showcase features of the mod. Gameplay defines a video where the mod was used during gameplay
* version (optional): The version of the mod used in the video

#images tag

Any number of images can be defined for a mod, within a json array under the images tag like this:

"images":[{image_1_details},{image_2_details},...,{image_n_details}],

The tags currently defined for an image are as follows:

* url (required): The location of the image
* desc (optional): A short plaintext description of the image
* version (optional): The version of the mod shown in the image

Valid image formats: png, jpg, gif

#New tags

Anyone can define new tags for new types of data (and additional tags for existing data), as long as:
* The format is defined above
* The format is in keeping with existing tags within that data type (or similar existing data types if we are defining a new data type)
* The format makes sense for the type of data being stored
