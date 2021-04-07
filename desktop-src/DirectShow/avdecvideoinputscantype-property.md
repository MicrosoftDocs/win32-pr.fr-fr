---
description: Spécifie la façon dont le flux vidéo décodé est entrelacé.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propriété AVDecVideoInputScanType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846550"
---
# <a name="avdecvideoinputscantype-property"></a>Propriété AVDecVideoInputScanType

Spécifie la façon dont le flux vidéo décodé est entrelacé.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .

## <a name="remarks"></a>Notes

Les 16 bits supérieurs de la valeur contiennent la largeur, tandis que les 16 bits inférieurs contiennent la hauteur.

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

 

