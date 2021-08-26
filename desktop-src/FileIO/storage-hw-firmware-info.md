---
description: 'Structure de STORAGE_HW_FIRMWARE_INFO : cette structure contient des informations sur le microprogramme de l’appareil.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Structure STORAGE_HW_FIRMWARE_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 1b9aa008e108f1282f8f61aaeacdce11eba7016632fa9643ae3db5550efb1e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047909"
---
# <a name="storage_hw_firmware_info-structure"></a>\_Structure d' \_ \_ informations sur le microprogramme matériel de stockage

Cette structure contient des informations sur le microprogramme de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. Elle doit être définie sur sizeof ( \_ \_ informations sur le microprogramme matériel de stockage \_ )

</dd> <dt>

**Taille**
</dt> <dd>

Taille de cette structure sous la forme d’une mémoire tampon incluant l’emplacement.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indique que ce microprogramme prend en charge une mise à niveau.

</dd> <dt>

**Reserved0**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**SlotCount**
</dt> <dd>

Nombre d’emplacements de microprogramme sur l’appareil. Il s’agit de la dimension du tableau d’emplacements.

> [!Note]  
> Certains appareils peuvent stocker plus d’une image de microprogramme, s’ils possèdent plus d’un emplacement de microprogramme.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Emplacement du microprogramme contenant l’image de microprogramme actuellement active/en cours d’exécution.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

Emplacement du microprogramme en attente d’activation.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indique que le microprogramme s’applique à la fois à l’appareil et au contrôleur/adaptateur, par exemple, SSD NVMe.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Alignement de la charge utile de l’image, en nombre d’octets. La taille de PAGE maximale est \_ . La taille de transfert est un multiple de cette taille. Certains protocoles nécessitent au moins la taille du secteur. Lorsque cette valeur est définie sur 0, cela signifie que cette valeur n’est pas valide.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

La taille maximale de la charge utile d’image est utilisée pour une seule commande.

</dd> <dt>

**Horaire**
</dt> <dd>

Contient les informations relatives à l’emplacement de chaque emplacement sur l’appareil, de type informations sur l' [**\_ \_ \_ emplacement \_ du microprogramme de stockage matériel**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                        |
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

[**\_requête d' \_ \_ informations sur le microprogramme matériel de stockage \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**\_ \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




