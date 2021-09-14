---
description: La \_ \_ propriété de l’appareil de la propriété DeviceDesc de l’appareil contient la description de l’appareil du point de terminaison (par exemple, &\# 0034 ; Haut-parleurs&\# 0034 ;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114838"
---
# <a name="pkey_device_devicedesc"></a>Périphérique de l' \_ appareil \_

La propriété de l’appareil de groupe de la propriété **\_ \_ DeviceDesc** contient la description de l’appareil du point de terminaison (par exemple, « Speakers »).

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient la description de l’appareil.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> <dt>

[Propriétés de l’appareil](device-properties.md)
</dt> </dl>

 

 




