---
title: iOS File App Error Code 100093 While Connecting Linux Samba Server
date: 2022-08-05 15:51:00 +08:00
---

Edit **/etc/samba/smb.conf**
Add `vfs objects = acl_xattr catia fruit streams_xattr` to *global* label then restart smbd service.