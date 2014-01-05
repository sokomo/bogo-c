
MAKEFILE_FLAGS   :=


.PHONY: all
all: release

.PHONY: debug
debug:	MAKEFILE_FLAGS := debug
debug:	build_app


.PHONY:	release
release:	MAKEFILE_FLAGS := release
release:	build_app

.PHONY:	test
test:	debug
	$(MAKE) -C unittest $(MAKEFILE_FLAGS)

.PHONY: install
install:	MAKEFILE_FLAGS := release
install:	build_app

.PHONY: clean
clean: MAKEFILE_FLAGS := clean
clean:	build_app
	$(MAKE) -C unittest $(MAKEFILE_FLAGS)

.PHONY:	build_app
build_app:
	$(MAKE) -C utf8small $(MAKEFILE_FLAGS)
	$(MAKE) -C engine $(MAKEFILE_FLAGS)
	$(MAKE) -C excution $(MAKEFILE_FLAGS)

