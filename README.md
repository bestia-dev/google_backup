# google_backup

**Export data from all Google services and backup to local disk (2023-08)**  
***date: 2023-08-11 author: [bestia.dev](https://bestia.dev) repository: [GitHub](https://github.com/bestia-dev/google_backup)***  

 ![maintained](https://img.shields.io/badge/maintained-green)
 ![ready_for_use](https://img.shields.io/badge/ready_for_use-green)
 [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/bestia-dev/dropbox_backup_to_external_disk/blob/main/LICENSE)
 ![google_backup](https://bestia.dev/webpage_hit_counter/get_svg_image/1081163093.svg)

My digital identity is created around Gmail. Just like most of the people I know.  
So if Google goes out of business or suddenly disables my account I am really in a bad place.  
It is wise to make a backup of my data that Google has. Not only Gmail but also other Google services.  

## Create a backup scheduler

It is not hard. Go to  
https://takeout.google.com/  
and click on `Create new Export`  
You want to select all of the data services except:

1. Access Log Activity - this is absolutely too large and has no value at all
2. Google Photos - if you use it, it can be huge. Probably you already have this photo synched somewhere.
3. My Activity - this is absolutely too large and has no value at all
4. Youtube - this can be huge if you uploaded videos. Probably you already have a backup copy of that somewhere.

Click on `Next step` and choose  
`Notify me by email when the download is ready`  
`Export every 2 months for 1 year`  
File Type: `.zip`  
File size: `50GB`  
The file size option is not really what you would expect. It does not make a zip with multiple files. If makes separate files for separate services and a single file (not ziped) can still be bigger than this limit. It is a completely pointless option.  

## Download the backup

The preparation of the backup can take hours or days.  
You will receive an email that the backup is ready to download. Go to  
https://takeout.google.com/  

Click on `Download` and wait. You have to wait quite some time for the download to finish for big files.  
When downloaded, check in Totalcmd if it can read the zip file.  
I have more than one Google account and email address for different purposes. So I want to distinguish between them.  
Rename the file to something meaningful like this:  
`LF2023-08-10 luciano.bestia@gmail.com_backup.zip`

Because of Dropbox API, we must limit the file size to less than 1 GB.  
If the file is bigger than 800MB then:  
Use TotalCmd to unzip the files, then zip them using the option `Multiple disk archive` and size 800000000 (800MB) using TotalCommander.  
Finally, move the zip files to a folder that will be synched to DropBox.  

## My Activity

It is intrusive to have the history of all your activity on Google services for ever.  
It can be disabled or limited to only 3 months.  

Go to:  
https://myactivity.google.com

and turn Off or limit history of your activity of Google services to 3 months for

1. Web & App Activity
2. Location History
3. Youtube History

