---
description: Indique le type de périphérique tablette, tel qu’un crayon, une souris ou un digitaliseur tactile.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Énumération TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 784e2393f5470f8abd966ca6dbdce3ac9d9bff734f1245ebd0ef169180c62d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820179"
---
# <a name="tablet_device_kind-enumeration"></a>\_Énumération de type d’appareil tablette \_

Indique le type de périphérique tablette, tel qu’un crayon, une souris ou un digitaliseur tactile.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_souris du périphérique tablette \_**
</dt> <dd>

La tablette est une souris. Cela comprend les pavés tactiles qui se trouvent sur de nombreux ordinateurs portables.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_stylet du périphérique tablette \_**
</dt> <dd>

La tablette utilise un crayon et un digitaliseur électromagnétiques.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_toucher du périphérique tablette \_**
</dt> <dd>

La tablette utilise un digitaliseur tactile.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITablet2 :: GetDeviceKind, méthode**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




