# eucalyptus-docs-web
## Eucalyptus documentation shared web content

The following is from https://eucalyptus.atlassian.net/wiki/spaces/DOC/pages/169446253/Publishing+a+Docs+Release

## Manage Symlinks and Documentation Archive page
Responsible: Technical Writer

The symlinks and archive index.html page are managed in the eucalyptus-docs-web/eucalyptus/ directory of this repo:
https://github.com/eucalyptus/eucalyptus-docs-web

### Prerequisite
Clone the eucalyptus-docs-web repo from github:
git clone git@github.com:eucalyptus/eucalyptus-docs-web.git

### To clone the repo in SourceTree (PC version):
1. File > Clone/New.
The Clone / Add / Create Repository dialog appears.
2. On the Clone Repository tab, Source Path / URL: click the globe icon (to get to GitHub). 
The Hosted Repositories dialog appears.
3. In the top-left search, enter the repo name: eucalyptus-docs-web
The repo appears in the search results.
4. Select the repo and click OK.
The Clone / Add / Create Repository dialog appears.
5. Review the settings and click Clone.
By default a bookmark appears and SourceTree clones the repo locally on your PC.

## Update the Documentation Archive Page
The public documentation archive page is:
https://docs.eucalyptus.com/eucalyptus/

1. On your local repo, modify the index.html page to add the released Eucalyptus and Euca2ools versions 
(eucalyptus-docs-web/eucalyptus/index.html).
2. For both the Eucalyptus and Euca2ools sections, add a list item at the top of each version list with a 
relative xref link to the released docs.
3. Move the (latest version) text and link to the list item you just created.

## Update the Symlinks
Pay close attention to the hidden files called ".keep" in the 3-digit version directories. 
(Git does not actually track directories, so you have to put some sort of placeholder in empty directories 
if you want them to show up.)
Do not remove these and be sure to add these hidden files when new 3-digit version directories are created.
* When a new release is available, create symlinks so that the latest and version series (e.g., 4.4) 
directories both go to the most current released documentation.

In the eucalyptus-docs-web/eucalyptus directory:
1. Create a symlink from a version series directory to the 3-digit directory for the new release version (e.g., symlink from 4.4 → 4.4.1)
2. Create the 3-digit version directory for the new release (e.g., 4.4.1)
3. Copy the hidden .keep file from an existing directory into the directory you just created
4. Only at a feature release (.0), update the latest symlink to point to the 2-digit version series directory (e.g., symlink from latest → 4.4)
