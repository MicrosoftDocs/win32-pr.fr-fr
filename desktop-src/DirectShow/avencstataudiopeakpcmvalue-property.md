---
description: Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: Propriété AVEncStatAudioPeakPCMValue (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d75444631a63c946d4020fe91cdd3a980fc393
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108987"
---
# <a name="avencstataudiopeakpcmvalue-property"></a>Propriété AVEncStatAudioPeakPCMValue

Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatAudioPeakPCMValue**

## <a name="remarks"></a>Notes

Cette propriété est disponible une fois l’encodage terminé.

Cette propriété s’applique uniquement à l’encodage VBR (Quality-based bit rate).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




