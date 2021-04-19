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
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531403"
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
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITablet2 :: GetDeviceKind, méthode**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




