#
# Copyright (C) 2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=yaml
PKG_VERSION:=0.1.2
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=http://pyyaml.org/download/libyaml/

PKG_INSTALL:=1

PKG_FIXUP:=libtool

include $(INCLUDE_DIR)/package.mk

define Package/libyaml
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=libyaml
  URL:=http://pyyaml.org/wiki/LibYAML
endef

define Package/libyaml/description
  yaml library written in c
endef

define Package/libyaml/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_DATA) $(PKG_INSTALL_DIR)/usr/lib/libyaml.so $(1)/usr/lib/
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include $(1)/usr/lib
	$(INSTALL_DATA) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include/
	$(INSTALL_DATA) $(PKG_INSTALL_DIR)/usr/lib/libyaml.{a,la} $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libyaml))
