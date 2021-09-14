---
description: La \_ propriété AudioEndpoint \_ JackSubType contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114861"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>\_AudioEndpoint \_ JackSubType

La **propriété \_ AudioEndpoint \_ JACKSUBTYPE** contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio. Le fichier d’en-tête Ksmedia. h définit les GUID. chaque GUID spécifie le type de connexion. Ces GUID ont également des catégories pin associées. Par exemple, le fichier d’en-tête Ksmedia. h définit l' **\_ \_ interface GUID KSNODETYPE DisplayPort** pour un port d’affichage qui se connecte au code confidentiel KS défini par le GUID **PINNAME le \_ DisplayPort \_**.

pour plus d’informations, consultez la description des propriétés de catégorie pin dans la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur **VT \_ LPWStr**.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




