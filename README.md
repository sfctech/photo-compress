# photo-compress
Using Python to Reduce JPEG and PNG Image File Sizes or to Resize Image Without Loss of Quality

## Running Locally
Make sure you have [Python3](https://www.python.org/downloads/) and Pillow(PIL--Python Imaging Library) installed .
```sh
> pip install Pillow
```

## Usage
### show help
```sh
> python photoCompress.py -h
usage: photoCompress.py [-h] [--resize BASEWIDTH]
                        [--mode {compress,restorebackup,deletebackup}]
                        path

Reduce file size of PNG and JPEG images.

positional arguments:
  path                  File or directory name

optional arguments:
  -h, --help            show this help message and exit
  --resize BASEWIDTH    Resize image based on width providing
  --mode {compress,restorebackup,deletebackup}
                        Mode to run with (default: compress). compress:
                        Compress the image(s). restorebackup: Restore the
                        backup images (valid for directory path only).
                        deletebackup: Delete the backup images (valid for
                        directory path only).
```

### compress
Attempt to resize or reduce size of supported JPEG and PNG images
```sh
> python photoCompress.py --mode compress --resize 1920 images
images\IMG_20170619_114327_374.jpg		ratio: 14.98%
......
images\IMG_20170624_194728_742.jpg		ratio: 34.1%

Successfully updated file count: 5
```

### restorebackup
Restore the backup of modified image files
```sh
> python photoCompress.py --mode resotrebackup images
```

### deletebackup
Delete the backup copies of modified image files
```sh
> python photoCompress.py --mode deletebackup images
```
