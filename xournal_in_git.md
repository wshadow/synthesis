Howto manage Xournal files in Git
=================================

Short version 
-------------
Tell git to unzip them, before diff/merge.

Long version
------------
Add this to your ~/.gitconfig :
	[diff "gzip"]
       	textconv = gzip -cdq

Add this to your .gitattributes in the repo:
	*.xoj diff=gzip


Try git diff anything.xoj