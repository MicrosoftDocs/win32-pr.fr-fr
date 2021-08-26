---
description: La \_ propriété AudioEndpoint \_ JackSubType contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053729"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>\_AudioEndpoint \_ JackSubType

La **propriété \_ AudioEndpoint \_ JACKSUBTYPE** contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio. Le fichier d’en-tête Ksmedia. h définit les GUID. chaque GUID spécifie le type de connexion. Ces GUID ont également des catégories pin associées. Par exemple, le fichier d’en-tête Ksmedia. h définit l' **\_ \_ interface GUID KSNODETYPE DisplayPort** pour un port d’affichage qui se connecte au code confidentiel KS défini par le GUID **PINNAME le \_ DisplayPort \_**.

pour plus d’informations, consultez la description des propriétés de catégorie pin dans la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur **VT \_ LPWStr**.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie.

## <a name="requirements"></a>Configuration requise



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

 

 




