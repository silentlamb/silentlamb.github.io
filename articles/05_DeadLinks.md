Title: Pelican plugin — Dead Links
Date: 2016-10-22
Category: software
Status: published
Tags: pelican

Recently I've been cleaning up old articles when I stumbled upon a problem
with dead links. Some of the articles written 1-2 years ago were linking
to non-existing pages. This post will describe a pelican plugin to 
notify or/and deal with said issues.

<!-- PELICAN_END_SUMMARY -->

Any feedback is more than welcome!

### Requirements

Plugin should work on both Python 2.7 and 3.5. Additionally it requires 
following libraries:

- BeautifulSoup4

### Installation

Clone repository from one of the possible sources:

- Directly from <https://github.com/silentlamb/pelican-deadlinks>
- From a master branch of <https://github.com/getpelican/pelican-plugins>

Let's assume destination is `./plugins/custom/deadlinks`. Configuration file 
should be changed as follow:

    :::python

    PLUGINS_PATH = [
        # [...]
        'plugins/custom'
    ]
    PLUGINS = [
         # [...]
        'deadlinks'
    ]

Or if you happen to use pelican-plugins directly, pull recent master.

### Settings

To enable dead link checker, set the `DEADLINK_VALIDATE` option in your Pelican 
configuration file to `True`. Additionally following options might be changed:

    :::python

    DEADLINK_OPTS = {
        'archive':  True,
        'classes': ['custom-class1', 'disabled'],
        'labels':   True
    }


| Name | Description | Default value | 
| ------ | ----------- | ------------- |
| `archive` | True/False. When enabled invalid links will be replaced with proper archive.org entry. http://example.org becomes http://web.archive.org/web/*/http://example.org | True |
| `classes` | List of classes to be added to anchor element | Empty list |
| `labels` | Insert bootstrap's label after the anchor element | False |

### Licence

MIT

