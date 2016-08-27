# 
# Copyright (C) 2006-2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=opentracker
PKG_VERSION:=0.2.0
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/nandub/opentracker/archive
PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_MD5SUM:=3f08b948d1f8602a3b6466631278cceb

include $(INCLUDE_DIR)/package.mk

define Package/opentracker
 SECTION:=app
 CATEGORY:=Application
 TITLE:=open and free bittorrent tracker project
 URL:=http://erdgeist.org/arts/software/opentracker/
 DEPENDS:=+libowfat +zlib +libpthread
endef

define Package/opentracker/description
 opentracker is a open and free bittorrent tracker project
endef

define Package/opentracker/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/opentracker $(1)/usr/bin
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/opentracker.init $(1)/etc/init.d/opentracker	
endef

$(eval $(call BuildPackage,opentracker))
