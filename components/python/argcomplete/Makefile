#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2019 Alexander Pyhalov
#

BUILD_BITS=NO_ARCH
BUILD_STYLE=setup.py

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= 	argcomplete
COMPONENT_VERSION= 	1.10.3
COMPONENT_REVISION=	2
COMPONENT_SUMMARY= 	Extensible command line tab completion for Python script arguments
COMPONENT_PROJECT_URL = https://pypi.org/project/argcomplete/
COMPONENT_SRC= 		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= 	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= \
  sha256:a37f522cf3b6a34abddfedb61c4546f60023b3799b22d1cd971eacdc0861530a
COMPONENT_ARCHIVE_URL= \
  $(call pypi_url)
COMPONENT_FMRI= library/python/argcomplete
COMPONENT_CLASSIFICATION=       Development/Python
COMPONENT_LICENSE=      Apache-2.0
COMPONENT_LICENSE_FILE= LICENSE.rst

PYTHON_VERSIONS=	2.7 3.5

TEST_TARGET=$(NO_TESTS)

include $(WS_MAKE_RULES)/common.mk

COMPONENT_POST_INSTALL_ACTION += ( cd $(PROTO_DIR)/usr/bin; \
	for file in activate-global-python-argcomplete \
		python-argcomplete-check-easy-install-script register-python-argcomplete ; do \
			mv $$file $$file-$(PYTHON_VERSION); \
	done )


# Auto-generated dependencies
REQUIRED_PACKAGES += library/python/setuptools-27
REQUIRED_PACKAGES += library/python/setuptools-35
REQUIRED_PACKAGES += runtime/python-27
REQUIRED_PACKAGES += runtime/python-35
REQUIRED_PACKAGES += SUNWcs
