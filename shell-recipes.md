# Command line recipes
Useful things to do from the command line

### download an entire site to read later

    wget -mkEpnp http://example.org

stands for:

    wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.org

    --mirror – Makes (among other things) the download recursive.
    --convert-links – convert all the links (also to stuff like CSS stylesheets) to relative, so it will be suitable for offline viewing.
    --adjust-extension – Adds suitable extensions to filenames (html or css) depending on their content-type.
    --page-requisites – Download things like CSS style-sheets and images required to properly display the page offline.
    --no-parent – When recursing do not ascend to the parent directory. It useful for restricting the download to only a portion of the site.

there are also options for no clobber, in case you need to restart a download, setting the browser for restricted sites,
and for setting wait time between attempts and limiting rate for handling hostile sites.  

### run a webserver locally to read your offline website

    python -m SimpleHTTPServer
