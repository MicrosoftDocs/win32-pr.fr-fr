---
description: Retourne le nombre de trames vidéo qui ont été encodées.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriété AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109371"
---
# <a name="avencstatvideocodedframes-property"></a>Propriété AVEncStatVideoCodedFrames

Retourne le nombre de trames vidéo qui ont été encodées.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Notes

Cette propriété est disponible une fois l’encodage terminé.

La valeur de cette propriété est égale à la propriété [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) moins le nombre de frames supprimés. L’encodeur peut supprimer des frames pour rester dans les limites de la vitesse de transmission spécifiée. Elle peut également supprimer des frames à la fin du flux (consultez la propriété [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).

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

 

 




