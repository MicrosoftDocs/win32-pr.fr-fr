---
description: Spécifie les proportions de pixels du flux vidéo décodé.
ms.assetid: 07689d15-3e46-45f7-bdd5-ae51308ddbce
title: Propriété AVDecVideoPixelAspectRatio (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ce01fbe8d8e7992b35265a67f1833ae41bdde2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112042"
---
# <a name="avdecvideopixelaspectratio-property"></a>Propriété AVDecVideoPixelAspectRatio

Spécifie les proportions de pixels du flux vidéo décodé.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoPixelAspectRatio**

## <a name="remarks"></a>Notes

Les 16 bits supérieurs de la valeur contiennent la largeur, tandis que les 16 bits inférieurs contiennent la hauteur.

## <a name="requirements"></a>Spécifications



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

 

 




