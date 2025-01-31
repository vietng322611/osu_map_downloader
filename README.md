# osu! map downloader

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [File example](#file-example)

## About <a name = "about"></a>

An osu! beatmap downloader that uses Beatconnect.io and Nerinyan.moe mirrors to download beatmaps from links stored in a text file and zips them afterwards.

## Getting Started <a name = "getting_started"></a>

### Prerequisites

Python 3

### Installing

1) Clone the repository

```
git clone https://github.com/vietng322611/osu_map_downloader.git
```

2) Install dependencies

```
cd osu_map_downloader
pip install -r requirements.txt
```

Example 

```
python map_dl.py -f example.txt -n example.zip
```

## Usage <a name = "usage"></a>

Basic usage

```
python map_dl.py
```

Help

```
usage: map_dl.py [-h] [-f pool.txt] [-n pool.zip] [-o D:\match_pool\]

Download beatmaps from a list of links.

options:
  -h, --help            show this help message and exit
  -f pool.txt, --file pool.txt
                        a text file containing beatmap links seperated by newline
  -n pool.zip, --name pool.zip
                        the name of the zip file to be created
  -o D:\pool\, --out D:\pool\
                        the directory where downloaded beatmaps are to be saved, use this if you don't want the beatmaps to be deleted after zipping (make sure the     
                        folder exists)
```

## File example <a name = "file-example"></a>
  
Default file name is pool.txt. You can use another file using -f option.  
  
/beatmapsets/[set_id]#[diff_id] or /beatmapsets/[set_id]

```
https://osu.ppy.sh/beatmapsets/2203300#osu/4675812
https://osu.ppy.sh/beatmapsets/2287992
```

/b/[diff_id]

```
https://osu.ppy.sh/b/4675812
https://osu.ppy.sh/b/4881796
```

Only diff id (MUST BE **DIFF ID**, set id won't work)

```
4675812
4881796
```