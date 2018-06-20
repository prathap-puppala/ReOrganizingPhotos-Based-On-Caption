# Reorganizing photos based on caption
This program is capable of recursively searching for image files stored in directories inside of other directories inside of other directories, and on and on to an unknown level of depth. JPEG files can contain additional image data stored as EXIF or IPTC. EXIF stands for Exchangeable Image File Format and is a well-documented standard. If you have a digital camera or have taken photos with a newer cell phone camera, the image probably has EXIF data available. Using a Macintosh, you can see this metadata information by opening the image in Preview, opening Tools, Show Inspector, and selecting the EXIF or IPTC tab.

On Windows, you can see metadata by right-clicking an image and selecting Properties and the Details tab. You'll see things like caption, dimensions, camera type, color space, exposure information, and other details. Cell phones will also imbed geographical location data identifying the longitude and latitude at which the picture was taken. This tool is used to, find images, extract the caption data from the metadata, and then reorganize those photos into an alphabetical folder structure based on the caption.


## Getting Started

### Prerequisites

- [Python](http://www.python.org)

### Installing

- Install [Python](http://www.python.org)


## Built With

* [Python](#)

### How it works?
The entry field below that functions the same way and lets you specify the Destination Directory which is where the program will create the sort folders and put the images. If you leave the box below it checked then the program will copy the images from the source directory into their appropriate folders in the destination directory, and if you uncheck it then the images will be moved rather than copied. 

In this folder I have several pictures some of them are JPEGs and some of them are .PNGs, if I run the caption sort program it'll find all of these images, it uses the ExifTool to retrieve their caption data and then based on the first letter of that caption it creates and moves them to the appropriate sort directory in that destination folder. You can see here by the message that I sorted all nine files in that folder. If I switch back over to my file explorer, you'll see that since I had my destination directory set to a folder called sorted, it created a new sorted folder here and if I open it up you'll see several folders for different letters of the alphabet.

Inside each of those folders you'll find images whose first letter, the caption, begins with that letter. This program is basically a three step process. 

ExifTool is a very robust command line application for reading and writing various metadata formats. It was created by Phil Harvey and is available from his website, you'll need to download it to use the Python script. 

The OS module's makedirs function to create the sort directories and then use the shutil module to either copy or move the original image files to their sorted locations. There's also a fourth module used in my solution called tkinter which generates the user interface. 


## Authors

* **Prathap Puppala**  -  [www.prathappuppala.com](https://www.prathappuppala.com)
