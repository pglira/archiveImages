# archiveImages

Small python package to create an image archive from a bunch of unordered images. The images are archived on the basis of the timestamp in the exif data.

The default target path of an image in the archive is `year/month/%Y_%m_%d_%H_%M_%S.%f.ext`, e.g. `image_archive\2018\04\2018-04-03_17_21_20.219.jpg`. Note that the extension of an image is automatically converted to lowercase, e.g. ``.JPG`` to ``.jpg``.

Install with `pip install .`, then call the help screen with `archiveImages --help`.

## Help screen

```
usage: archiveImages [-h] -i IMAGEFOLDER -a IMAGEARCHIVE [-e IMAGEEXTENSIONS]
                     [-m {copy,move}] [-d] [-n] [-c]

required arguments:
  -i IMAGEFOLDER, --imageFolder IMAGEFOLDER
                        Path to folder with images to archive (default: None)
  -a IMAGEARCHIVE, --imageArchive IMAGEARCHIVE
                        Path to folder with image archive (default: None)

optional arguments:
  -e IMAGEEXTENSIONS, --imageExtensions IMAGEEXTENSIONS
                        Extensions of images to archive separated by commas
                        (default: ['jpg', 'jpeg'])
  -m {copy,move}, --mode {copy,move}
                        Move or copy image files to archive? (default: copy)
  -d, --addDuplicates   Add duplicates to a subfolder "duplicates" in image
                        archive? (default: False)
  -n, --addNoExif       Add images with no exif information to a subfolder
                        "no_exif" in image archive? (default: False)
  -c, --confirm         Confirm each operation before execution? (default:
                        False)
```
