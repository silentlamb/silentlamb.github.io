Title: Pelican plugin — Dead Link
Date: 2016-10-19
Category: software
Status: draft
Tags: pelican

Recently I've been cleaning up old articles when I stumbled upon a problem
with dead links. Some of the articles written 1-2 years ago was linking
to non-existing pages. For example, I've deleted engine project from a github 
and link is valid no more. This post will describe a pelican plugin to 
notify or/and deal with said issue.

<!-- PELICAN_END_SUMMARY -->

### Requirements

Plugin should work on both Python 2.7 and 3.5. Additionally it requires 
following libraries:

- BeautifulSoup4

### Installation

Clone repository somewhere (let's assume destination is ./plugins/custom/deadlinks) 
and edit configuration file:

    :::python

    PLUGINS_PATH = [
        # [...]
        'plugins/custom'
    ]
    PLUGINS = [
         # [...]
        'deadlinks'
    ]


### Settings

To enable dead link checker, set the `DEADLINK_VALIDATE` option in your Pelican 
configuration file to `True`. Additionally following options might be changed:

    :::python

    DEADLINK_OPTS = {
        'disable_anchors': True,
        'add_labels': True,
    }


|  Option           | Description                            |
| ----------------- | -------------------------------------- |
| add_labels        |  Add bootstrap's label with error code |
| disable_anchors   |  Add disabled class to the anchor      |


