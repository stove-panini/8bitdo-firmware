# Copyright (C) 2016 Richard Hughes <richard@hughsie.com>

VENDOR=8Bitdo
PROJECT_NAME=FC30ARCADE
VERSION=4.01
FIRMWARE_FILES=				\
	8Bitdo_joy_firmware_V4.01.dat
METAINFO_FILES=				\
	fc30arcade.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
