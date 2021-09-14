---
description: Spécifie si le flux de sortie doit être structuré afin que le flux encodé ait une latence de décodage faible.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propriété AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111974"
---
# <a name="avenccommonlowlatency-property"></a>Propriété AVEncCommonLowLatency

Spécifie si le flux de sortie doit être structuré afin que le flux encodé ait une latence de décodage faible.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Notes

La latence du décodage est définie comme la quantité de données que le décodeur doit mettre en mémoire tampon. Par exemple, la définition de cette propriété sur la **\_ valeur variant true** sur un encodeur vidéo MPEG limite les types de structures GOP que l’encodeur peut utiliser.

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

 

 




