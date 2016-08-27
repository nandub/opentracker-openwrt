# 
# Copyright (C) 2006-2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libowfat
PKG_VERSION:=0.30
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://www.fefe.de/libowfat
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_MD5SUM:=f0119532ea834ce9e80afe49d7d85512

include $(INCLUDE_DIR)/package.mk

define Package/libowfat
 SECTION:=libs
 CATEGORY:=Libraries
 TITLE:=GPL reimplemention of libdjb
 URL:=https://www.fefe.de/libowfat/
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
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/*.o $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libowfat))
