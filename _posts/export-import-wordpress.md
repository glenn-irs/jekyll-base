Exporting & Importing WordPress

## Easy?

In theory it's a simple thing. But to be honest, I've always had problems with it. I needed to move a number of sites and content around yesterday, and so I had the chance to try many variations and discover what works and what doesn't. My final solution seems like it has to be wrong! However, it is the only sequence of steps I found that moved my content between WordPress sites, transferred images, and kept links intact.



## *Transferrus Interruptus*

Here in it's awkward glory, but good results, is my *transferrus interruptus* procedure:

1. **Clean stuff up** - adjust categories, delete unneeded pages, etc - make the outgoing site clean for transfer.
2. **Export** - Admin > Tools > Export
3. **Find & Replace** - Open your .xml export and find and replace URL's. If your old site was *thatssocool.de* and you're moving to *runaway.university,* then replace all the instances of *thatssocool.de* with *runaway.university.* There will be **a lot.** Lots of image links.
4. **Download Images** - FTP download all of the image files and any other files from your outgoing site. Keep them in their folders, like */2015/11/nicepix.jpg*
5. **Upload Images** - FTP upload all of the images and any other files to your new site location. If the folder at the new site doesn't exist yet, like: *runaway.university/wp-content/uploads/2015/11*, then you can move that whole directory (folder). If it already does exist, then just add all the files to the new folder, like: *old/2015/11 > new/2015/11*
6. **Import** - *Admin > Tools > Import > WordPress Import.* **Do** click *Download & Import file attachments.* As far as I can see, this *does not* move your files for you. You just did that in steps 4 & 5 above. But it does "inform" WordPress that those files you transferred to your new server location should be part of your WordPress installation. And it makes your *Featured Images* work. However, the images within your posts will have broke links! This is why the paradoxical Step 7 exists:
7. **Delete New Posts!** - Delete all the posts you just added! Having put them in 1 or a few specific categories up above in Step 1 helps with this action. Just go to Posts, then Filter by Category, then select all (carefully!) and then *Move to Trash,* and then *Empty Trash.* (carefully!)
8. **Import Again!** - *Admin > Tools > Import > WordPress Import.* Just like before. Only this time **Do not** click *Download & Import file attachments.* The importer will go through this, warn you that your files already exist, which is true, and then tell you to *have a nice day.* 


## Kludgy, but...

**Importing, deleting & Re-Importing** is obviously a little kludgy! But it's the only sequence of steps I've found that gets the job done. Every other sequence either leaves you with *No featured images,* or with *Broken image links in the bodies of your posts.* With my strange sequence everything comes out clean.

If you know why this works, or is necessary, or what the less kludgy process that still yields clean results is, by all means, shout in the comments below!
