---
description: La \_ \_ propriété d’association AudioEndpoint de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114886"
---
# <a name="pkey_audioendpoint_association"></a>Association de AudioEndpoint de la \_ \_

La propriété d' **\_ \_ Association AudioEndpoint** de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio. Le fichier. inf qui installe un adaptateur audio affecte une catégorie de code confidentiel à chaque code confidentiel KS de l’adaptateur. Un code PIN KS sur un appareil d’adaptateur représente le point auquel un flux audio entre ou quitte l’appareil. Une catégorie de code confidentiel est un GUID qui spécifie le type de fonction effectuée par un code confidentiel KS. Par exemple, le fichier d’en-tête Ksmedia. h définit le microphone KSNODETYPE GUID de catégorie pin \_ pour indiquer un code confidentiel KS qui se connecte à un microphone, et KSNODETYPE \_ casque pour indiquer un code confidentiel KS qui se connecte au casque. pour plus d’informations, consultez la description des propriétés de catégorie pin dans la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie de code confidentiel KS.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




