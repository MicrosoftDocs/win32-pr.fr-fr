---
description: Cette structure contient des informations sur le microprogramme de l’appareil.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Structure STORAGE_HW_FIRMWARE_INFO_QUERY (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517088"
---
# <a name="storage_hw_firmware_info_query-structure"></a>\_Structure de \_ \_ requête informations sur le microprogramme matériel de stockage \_

Cette structure contient des informations sur le microprogramme de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. Elle doit être définie sur sizeof ( \_ \_ requête informations sur le microprogramme matériel de stockage \_ \_ )

</dd> <dt>

**Taille**
</dt> <dd>

Taille de cette structure sous la forme d’une mémoire tampon.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs associés à la requête. Les indicateurs suivants peuvent être définis dans ce membre.



| Indicateur                                             | Description                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| contrôleur de l' \_ \_ indicateur de demande de microprogramme matériel \_ \_ de stockage \_ | Indique que la cible de la requête autre que la main/l’objet de l’appareil lui-même. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé pour un usage futur.

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

[**\_ \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




