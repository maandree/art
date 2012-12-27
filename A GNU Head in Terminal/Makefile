# Copying and distribution of this file, with or without modification,
# are permitted in any medium without royalty provided the copyright
# notice and this notice are preserved.  This file is offered as-is,
# without any warranty.
# 
# [GNU All Permissive License]


# dependency: util-say


XTERM = gnu.xterm-256color
LINUX = gnu.linux
PNG = gnu.png

all: xterm-256color linux


xterm-256color: $(XTERM)
$(XTERM): $(PNG)
	img2ponysay $(PNG) | tail --lines="$$(( $$(img2ponysay $(PNG) | wc -l) - 4 ))" > $(XTERM)


linux: $(LINUX)
$(LINUX): $(XTERM)
	ponysay2ttyponysay < $(XTERM) > $(LINUX)


png: $(PNG)
$(PNG): $(XTERM)
	ponysay2img $(PNG) < $(XTERM)


