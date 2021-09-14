---
description: Spécifie si l’application requiert des performances d’encodage en temps réel.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Propriété AVEncCommonRealTime (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a03e51da1a088603273da3d083573e5921edf7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111933"
---
# <a name="avenccommonrealtime-property"></a>Propriété AVEncCommonRealTime

Spécifie si l’application requiert des performances d’encodage en temps réel.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonRealTime**

## <a name="remarks"></a>Notes

Pour spécifier que l’encodage doit être exécuté en temps réel, affectez à cette propriété la **\_ valeur variant true**. Les codecs peuvent également retourner cette propriété en tant que fonctionnalité.

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

 

 




