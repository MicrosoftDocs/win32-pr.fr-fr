---
description: Spécifie le nombre de champs à ignorer pendant l’encodage.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propriété AVEncVideoNoOfFieldsToSkip (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 908a169b6f8ea868f7959afbd8fc90afa0b7a129b90674791990a156e67af948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342129"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propriété AVEncVideoNoOfFieldsToSkip

Spécifie le nombre de champs à ignorer pendant l’encodage.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Remarques

Pour une vidéo progressive, définissez cette propriété sur deux fois le nombre de frames à ignorer.

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

 

 




