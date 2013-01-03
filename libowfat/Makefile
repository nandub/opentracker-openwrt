# 
# Copyright (C) 2006-2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libowfat
PKG_VERSION:=0.29
PKG_RELEASE:=1

PKG_SOURCE_URL:=http://dl.fefe.de
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_MD5SUM:=1187c6acf11429e7adb9ebe180f644bb

include $(INCLUDE_DIR)/package.mk

define Package/libowfat
 SECTION:=libs
 CATEGORY:=Libraries
 TITLE:=libowfat
 URL:=http://www.fefe.de/libowfat/
endef

define Package/libowfat/description                                                
 GPL reimplemention of libdjb
endef

define Package/libowfat/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/*.o $(1)/usr/lib/
	
endef

define Package/libowfat/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/*.h $(1)/usr/include/
	$(INSTALL_BIN) $PKG_BUILD_DIR)/*.o $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libowfat))
