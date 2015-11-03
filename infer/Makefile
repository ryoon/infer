SHELL := /bin/bash
CWD = $(shell pwd)

ANNOTATIONS = annotations
MODELS = models
SRCDIR = src


.PHONY: clean clang java llvm checkCopyright models

all: clang java llvm checkCopyright

java:
	$(MAKE) -C $(SRCDIR) java
	$(MAKE) -C $(ANNOTATIONS)
	$(MAKE) -C $(MODELS) java

clang:
	$(MAKE) -C $(SRCDIR) clang
	$(MAKE) -C $(MODELS) clang

llvm:
	$(MAKE) -C $(SRCDIR) llvm

checkCopyright:
	$(MAKE) -C $(SRCDIR) checkCopyright

clean:
	$(MAKE) -C $(SRCDIR) clean
	$(MAKE) -C $(ANNOTATIONS) clean
	$(MAKE) -C $(MODELS) clean
