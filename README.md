PAModDetails
============

A place to define additional details and media for PA mods. This additional data can be used by anything that wants to read it (websites, PA Hub plugins, etc).

* The format is a json array with an entry per mod, mirroring the format of the main mod json found here: https://pamm-mereth.rhcloud.com/api/mod
* The only required element for an entry in the list is the mod identifier

#Youtube tag

Any number of youtube videos can be defined for a mod, within a json array under the youtube tag like this:

"youtube":[{video_1_details},{video_2_details},...,{video_n_details}],

The tags currently defined for a video are as follows:

* type (optional): Defining the type of video, such as Gameplay, Tutorial, etc. Tutorial defines a video where the mod is the central focus of the video, the video was made to showcase features of the mod. Gameplay defines a video where the mod was used during gameplay
* video (required): The youtube code that identifies the video
* list (optional): A youtube playlist that the video is a member of
* desc (optional): A short plaintext description of the video

#New tags

Anyone can define new tags for new types of data (and additional tags for existing data), as long as:
* The format is defined above
* The format is in keeping with existing tags within that data type (or similar existing data types if we are defining a new data type)
* The format makes sense for the type of data being stored
