## Flickr-Faces-HQ Public Domain Dataset (FFHQ-PD)
**Modified from the original dataset [found here.](https://github.com/NVlabs/ffhq-dataset)**

![License CC](https://img.shields.io/badge/license-CC-green.svg?style=plastic)
![Format PNG](https://img.shields.io/badge/format-PNG-green.svg?style=plastic)
![Resolution 1024&times;1024](https://img.shields.io/badge/resolution-1024&times;1024-green.svg?style=plastic)

Flickr-Faces-HQ (FFHQ) is a high-quality image dataset of human faces, originally created as a benchmark for generative adversarial networks (GAN):

> **A Style-Based Generator Architecture for Generative Adversarial Networks**
> Tero Karras (NVIDIA), Samuli Laine (NVIDIA), Timo Aila (NVIDIA)
> https://arxiv.org/abs/1812.04948

**This dataset is a modified version of the original FFHQ dataset, filtered to only contain public domain images.**

## Licenses

The images were all published in Flickr by their respective authors under either [Public Domain Mark 1.0](https://creativecommons.org/publicdomain/mark/1.0/) or [Public Domain CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). All of these licenses allow **free use, redistribution, and adaptation for non-commercial purposes**. The license and original author of each image are indicated in the metadata.

* [https://creativecommons.org/publicdomain/mark/1.0/](https://creativecommons.org/publicdomain/mark/1.0/)
* [https://creativecommons.org/publicdomain/zero/1.0/](https://creativecommons.org/publicdomain/zero/1.0/)

The original dataset files (not including raw images) were made available under [Creative Commons BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license by NVIDIA Corporation under the following terms:

You can **use, redistribute, and adapt it for non-commercial purposes**, as long as you (a) give appropriate credit by **citing our paper**, (b) **indicate any changes** that you've made, and (c) distribute any derivative works **under the same license**.

* [https://creativecommons.org/licenses/by-nc-sa/4.0/](https://creativecommons.org/licenses/by-nc-sa/4.0/)

All files from the original dataset were removed except for this documentation which was modified to match the structure and goals of this project, and the JSON metadata, which has all file paths removed (since all images are in one path and thumbnails have been removed), image indexes removed (metadata indexes still match the photo numbers, it is just no longer explicitly stated in the file itself) and all entries removed for the images that had not been published under Public Domain Mark 1.0 or Public Domain CC0 1.0.

## Metadata

The `ffhq-pd-dataset-v2.json` file contains the following information for each image in a machine-readable format. The index of each set of metadata for an image matches the number of the photograph (photo[0] == images1024x1024/0.png,  photo[1] == images1024x1024/1.png, etc.)

```
{
  "{                                                 
    "category": "training",                              # Training or validation
    "metadata": {                                        # Info about the original Flickr photo:
      "photo_url": "https://www.flickr.com/photos/...",  # - Flickr URL
      "photo_title": "Day at the Beach",                 # - File name
      "author": "Brian Benson",                          # - Author
      "country": "Australia",                            # - Country where the photo was taken
      "license": "Attribution-NonCommercial License",    # - License name
      "license_url": "https://creativecommons.org/...",  # - License detail URL
      "date_uploaded": "2007-08-16",                     # - Date when the photo was uploaded to Flickr
      "date_crawled": "2018-10-10"                       # - Date when the photo was crawled from Flickr
    },
    "image": {                                           # Info about the aligned 1024x1024 image:
      "file_url": "https://drive.google.com/...",        # - Google Drive URL
      "file_size": 1488194,                              # - Size of the PNG file in bytes
      "file_md5": "ddeaeea6ce59569643715759d537fd1b",    # - MD5 checksum of the PNG file
      "pixel_size": [1024, 1024],                        # - Image dimensions
      "pixel_md5": "47238b44dfb87644460cbdcc4607e289",   # - MD5 checksum of the raw pixel data
      "face_landmarks": [...]                            # - 68 face landmarks reported by dlib
    },
    "thumbnail": {                                       # Info about the 128x128 thumbnail:
      "file_url": "https://drive.google.com/...",        # - Google Drive URL
      "file_size": 29050,                                # - Size of the PNG file in bytes
      "file_md5": "bd3e40b2ba20f76b55dc282907b89cd1",    # - MD5 checksum of the PNG file
      "pixel_size": [128, 128],                          # - Image dimensions
      "pixel_md5": "38d7e93eb9a796d0e65f8c64de8ba161"    # - MD5 checksum of the raw pixel data
    },
    "in_the_wild": {                                     # Info about the in-the-wild image:
      "file_url": "https://drive.google.com/...",        # - Google Drive URL
      "file_size": 3991569,                              # - Size of the PNG file in bytes
      "file_md5": "1dc0287e73e485efb0516a80ce9d42b4",    # - MD5 checksum of the PNG file
      "pixel_size": [2016, 1512],                        # - Image dimensions
      "pixel_md5": "86b3470c42e33235d76b979161fb2327",   # - MD5 checksum of the raw pixel data
      "face_rect": [667, 410, 1438, 1181],               # - Axis-aligned rectangle of the face region
      "face_landmarks": [...],                           # - 68 face landmarks reported by dlib
      "face_quad": [...]                                 # - Aligned quad of the face region
    }
  },
  ...
}
```


## Privacy

Similarly to the original dataset, any authors who wish to have their photographs removed from the dataset will have their wish respected. Follow the steps given on the [original repository,](https://github.com/NVlabs/ffhq-dataset) and this set will mirror any removals of public domain images.