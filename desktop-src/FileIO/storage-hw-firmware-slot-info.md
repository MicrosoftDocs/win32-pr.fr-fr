---
description: Cette structure contient des informations sur un emplacement sur un appareil.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Structure STORAGE_HW_FIRMWARE_SLOT_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531803"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>\_Structure d' \_ \_ informations sur l’emplacement du microprogramme du matériel de stockage \_

Cette structure contient des informations sur un emplacement sur un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. Elle doit être définie sur sizeof (stockage \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_ \_ )

</dd> <dt>

**Taille**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Numéro de l’emplacement de cet emplacement.

</dd> <dt>

**Lecture seule**
</dt> <dd>

Indique si cet emplacement est en lecture seule ou non.

</dd> <dt>

**Reserved0**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**Reserved1**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**Faisant**
</dt> <dd>

Révision du microprogramme sur cet emplacement.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Winioctl. h. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ activation du microprogramme de stockage IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**\_ \_ activation du microprogramme matériel de stockage \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**\_ \_ Téléchargement du microprogramme matériel de stockage \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_ \_ informations sur le microprogramme matériel de stockage \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_requête d' \_ \_ informations sur le microprogramme matériel de stockage \_**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




