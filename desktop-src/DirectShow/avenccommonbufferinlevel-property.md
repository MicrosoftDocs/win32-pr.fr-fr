---
description: Spécifie le niveau initial de la mémoire tampon d’encodage, en bits. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Propriété AVEncCommonBufferInLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1e2b1d5b27d405d5b2a4c69cd9503d1c4f2815356e31c9a165f52d215e806d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873379"
---
# <a name="avenccommonbufferinlevel-property"></a>Propriété AVEncCommonBufferInLevel

Spécifie le niveau initial de la mémoire tampon d’encodage, en bits. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonBufferInLevel**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Remarques

Pour la vidéo MPEG, cette propriété définit la saturation de la mémoire tampon vidéo (VBV) initiale. Il prend en charge la concaténation de flux pendant l’encodage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




