# Copyright (C) 2017 Richard Hughes <richard@hughsie.com>

VENDOR=Logitech
PROJECT_NAME=Unifying
VERSION=RQR21.00_B0007
FIRMWARE_FILES=../RQR21.00_B0007.hex
METAINFO_FILES=com.logitech.Unifying.RQR21.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
