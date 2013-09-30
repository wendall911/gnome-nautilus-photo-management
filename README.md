# Gnome Nautilus Photo Management
Simple tools for simple photo management in Gnome

## Why
Ok, all photo management software out there pretty much just sucks or is
overkill and still missing the features I need. For the most part, just using
Nauilus works. I can organize photos into folders, import, etc. But there are a
few things missing.

1. Columns representing exif data.
1. Automated importing photos from the camera or other folder and sorting into
an organized structure.
1. Simple modification of exif data.

Here are some issues I'm seeing with other projects:

1. Hyper focused on sharing versus just storing and protecting my original
images.
1. No concept or clue about how many photos a typical user will have and want
to manage and store. [1] I mean not a damn clue.
1. Consider dropbox a solution for anything (Seriously, this is not a backup service)
1. Have no concept of how many photos someone might have in the *existing*
collection. And no real way to deal with this. (But have a dozen half baked
ways you can get your destroyed images back from FB)

[1] I have a fairly small collection of digital photos, ~50GB and 21000 images. If we start doing family movies more regularly, as we already have a few, we'll have some TB of data to store.

## The Plan
Here is the plan for doing this without getting old and grey screwing around
with broken photo management programs that want to shove all my photos into a
database and modify the original files! Screw you guys!

### Columns representing exif data
It appears as though
 [nautilus-columns](https://launchpad.net/~nilarimogard/+archive/webupd8/+packages?field.name_filter=nautilus-columns)
 does a nice job of this. Since this is pretty much a ubuntu thing, I'll pull
 it in here and modify for my own needs.

### Importing photos and sorting
This will be a simple Nautils script that allows the user to right click the
target folder and import the images into the directory designated in the
configuration. I prefer %Y/%M as a layout in Pictures, and I could probably
make this configurable at some point. Can always just move photos around at
will. Event folders work just fine, since I don't have to ask permission to do
so.

### Simple modification of exif data
It appears as though [phatch](http://photobatch.wikidot.com/) works just fine
for this. I'll have to mess around with it and see if it makes sense for basic
exif editing. Mostly I need to be able to add date to scanned images and tags.

## The Future
In the future, I think I'll make a
 [Pyramid](http://www.pylonsproject.org/projects/pyramid/about) based web
 interface with authentication that allows viewing of the underlying
 filesystem. Photos and images. This would allow private sharing for family and
 friends.
