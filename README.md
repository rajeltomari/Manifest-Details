Mod Manifest Details
====================
Nova2 Modification (Anodyne Productions)

Created by Moriel Schottlender (mooeypoo@gmail.com)

-

## Description
This modification adds a few details to the manifest page on Nova2. 
It adds "species" and "gender" details, as well as a small thumbnail of the main character images. 

## Important Note
Just like any other modification for Nova, please take great care when editing controllers. Especially when updating or upgrading the mod, make sure you COMPLETELY delete the associated functions and then COMPLETELY replace them with the new functions.
If your controller file was previously edited, be careful not overriding the changes you already made to it.

## Installation

1. Go to Control Panel -> Settings and click the "Manage User-created Settings" link.
Click on "Add User-Created Settings" and add these fields:

```
Label: Manifest Details - Show Species
Setting Key: modManifest_show_species
Value: True
```

```
Lable: Manifest Details - Show Gender
Setting Key: modManifest_show_gender
Value: True
```

```
Label: Manifest Details - Show Thumbnail
Settings Key: modManifest_show_thumbnail
Value: True
```

You will later be able to change these values. 
**It is VERY IMPORTANT that they "Setting Key" is exactly as is written!**

2. Add menu items.  Go to Control Panel -> Menu Items and click on the "Add Menu Items" link.

Add the following item:

```
Name: Manifest Options
Link: admin/modmanifest
Link Type: Onsite

Type: Admin Sub Navigation
Category: Admin Control Panel

Login Requirement: Must be Logged In
Use Access Control: Yes
Access Control URL: site/settings
```


2. Upload the entire contents of the application/assets/js folder into your domain's nova application/assets folder.

3. Open [your domain]/application/controllers/personnel.php controller, and copy the entire function index() { } segment into the one in your domain. For your convenience, the function begins and ends with

```
	/**********************/
	/**** MANIFEST MOD ****/
	/**********************/
```

Just mark the text from the first note to the second, and copy it to your personnel.php controller.

4. Open [your domain]/application/controllers/admin.php controller, and copy the entire function modmanifest() { } segment into the one in your domain. For your convenience, the function begins and ends with

```
	/**********************/
	/**** MANIFEST MOD ****/
	/**********************/
```

Just mark the text from the first note to the second, and copy it to your personnel.php controller.

5. Upload the view folder. PLEASE NOTE: If either of those files:

application/views/_base_override/main/pages/personnel_index.php
application/views/_base_override/main/js/personnel_index_js.php

Were changed in your application/views/ folder, you will need to skip the step. DO NOT upload the view files if they were previously modified, unless the modification was ONLY for this particular mod. If you upload the files, you will override whatever previous modification you already had. 

If the files were only updated by this mod (Manifest Details) then feel free to re-upload them both without worry.

### NOTE
If you already edited these files for another mod, you will have to be careful manually managing this extension into the existing files. I only recommend you do that if YOU REALLY KNOW WHAT YOU'RE DOING! 

I have marked all the changed/additions in the view file with HTML comments, so you should just find where they are and plug them into your previously-edited file.

Credits and help
================
I apologize in advance, I'm a student and I have a full time job, so I don't have as much time as I'd like to help and correct bugs. However, it does matter to me, so please take the time to report whatever bug you find in the "issues" on github.

Alternatively, you can go to the Anodyne Productions forum and catch me up there.

Enjoy!

~mooeypoo
mooeypoo@gmail.com