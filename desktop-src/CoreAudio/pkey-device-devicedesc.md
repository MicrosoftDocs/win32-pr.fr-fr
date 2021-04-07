---
description: La \_ \_ propriété de l’appareil de la propriété DeviceDesc de l’appareil contient la description de l’appareil du point de terminaison (par exemple, &\# 0034 ; Haut-parleurs&\# 0034 ;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846961"
---
# <a name="pkey_device_devicedesc"></a>Périphérique de l' \_ appareil \_

La propriété de l’appareil de groupe de la propriété **\_ \_ DeviceDesc** contient la description de l’appareil du point de terminaison (par exemple, « Speakers »).

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient la description de l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> <dt>

[Propriétés de l’appareil](device-properties.md)
</dt> </dl>

 

 




