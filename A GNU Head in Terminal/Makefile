# Copying and distribution of this file, with or without modification,
# are permitted in any medium without royalty provided the copyright
# notice and this notice are preserved.  This file is offered as-is,
# without any warranty.
# 
# [GNU All Permissive License]


# dependency: util-say


all: xterm-256color linux


xterm-256color: gnu.xterm-256color
gnu.xterm-256color: gnu.png
	img2ponysay gnu.png | tail --lines="$$(( $$(img2ponysay gnu.png | wc -l) - 4 ))" > gnu.xterm-256color


linux: gnu.linux
gnu.linux: gnu.xterm-256color
	ponysay2img < gnu.xterm-256color gnu.png


png: gnu.png
gnu.png: gnu.xterm-256color
	ponysay2img < gnu.xterm-256color gnu.png


