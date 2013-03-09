#
# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ethersend
PKG_VERSION:=2013-03-09
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://git.universe-factory.net/ethersend
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=c78b87e29df0217d6f277d58559b0d6926508948
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/ethersend
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=
  TITLE:=Minimal tool to send ethernet packets
  URL:=http://git.universe-factory.net/ethersend/
endef


define Package/ethersend/description
 Minimal tool to send ethernet packets
endef

define Build/Compile
	$(MAKE) -C $(PKG_BUILD_DIR) CC="$(TARGET_CC)"
endef

define Package/ethersend/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ethersend $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,ethersend))
