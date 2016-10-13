# Copyright (C) 2016 Richard Hughes <richard@hughsie.com>

VENDOR=HydraBus
PROJECT_NAME=Firmware
VERSION=0.7
FIRMWARE_FILES=hydrafw.dfu
METAINFO_FILES=com.hydrabus.firmware.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
