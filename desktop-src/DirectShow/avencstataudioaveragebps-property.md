---
description: Retourne le nombre moyen de bits par seconde de l’audio encodé.
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: Propriété AVEncStatAudioAverageBPS (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76bcf1ca7b3ee74ae406ebd71f85988a4d13313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033536"
---
# <a name="avencstataudioaveragebps-property"></a>Propriété AVEncStatAudioAverageBPS

Retourne le nombre moyen de bits par seconde de l’audio encodé.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatAudioAverageBPS**

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

 

 




