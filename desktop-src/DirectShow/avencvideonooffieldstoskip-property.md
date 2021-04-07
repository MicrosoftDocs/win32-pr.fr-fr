---
description: Spécifie le nombre de champs à ignorer pendant l’encodage.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propriété AVEncVideoNoOfFieldsToSkip (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846130"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propriété AVEncVideoNoOfFieldsToSkip

Spécifie le nombre de champs à ignorer pendant l’encodage.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Notes

Pour une vidéo progressive, définissez cette propriété sur deux fois le nombre de frames à ignorer.

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

 

 




