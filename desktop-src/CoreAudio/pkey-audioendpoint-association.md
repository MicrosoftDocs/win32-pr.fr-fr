---
description: La \_ \_ propriété d’association AudioEndpoint de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f7130ac82341b2da25356158d656051934b77f6006c35c1e812a4779a2e6e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698669"
---
# <a name="pkey_audioendpoint_association"></a>Association de AudioEndpoint de la \_ \_

La propriété d' **\_ \_ Association AudioEndpoint** de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio. Le fichier. inf qui installe un adaptateur audio affecte une catégorie de code confidentiel à chaque code confidentiel KS de l’adaptateur. Un code PIN KS sur un appareil d’adaptateur représente le point auquel un flux audio entre ou quitte l’appareil. Une catégorie de code confidentiel est un GUID qui spécifie le type de fonction effectuée par un code confidentiel KS. Par exemple, le fichier d’en-tête Ksmedia. h définit le microphone KSNODETYPE GUID de catégorie pin \_ pour indiquer un code confidentiel KS qui se connecte à un microphone, et KSNODETYPE \_ casque pour indiquer un code confidentiel KS qui se connecte au casque. pour plus d’informations, consultez la description des propriétés de catégorie pin dans la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie de code confidentiel KS.

## <a name="requirements"></a>Configuration requise



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

 

 




